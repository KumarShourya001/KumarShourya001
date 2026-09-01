<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-light.svg">
  <img alt="Kumar Shourya — software engineering, full-stack, applied ML" src="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-light.svg" width="100%">
</picture>

I care about the part that comes after the notebook — the API, the frontend, the container, the thing a stranger can actually open. Most of what I build ends up deployed somewhere. Right now that means a job queue that uses MongoDB as its own broker, and multimodal retrieval over a 71,000-item catalog.

<sub>B.Tech CSE at NIT Patna, CGPA 8.49 &nbsp;·&nbsp; Patna, India &nbsp;·&nbsp; <a href="mailto:kshourya2005@gmail.com">kshourya2005@gmail.com</a></sub>

## Selected work

### Distributed job queue

Jobs are submitted over an HTTP API, persisted in MongoDB, claimed and executed by independent worker processes, and streamed live to a React dashboard over WebSockets.

- **MongoDB is the broker** — no Redis, no RabbitMQ. A single atomic `findOneAndUpdate` moves a job from `pending` to `claimed`, so exactly one worker wins it no matter how many are running.
- **Failure handling** — a failed job increments `attempts` and returns to `pending`, then dead-letters after three. A sweeper runs every 5s and reclaims anything a crashed worker left stranded in `claimed` for more than 30 seconds.
- **Live dashboard** — every write to the collection fires a change stream event, broadcast over WebSockets, so state transitions appear as they happen rather than on a poll.
- **API** — `POST /jobs` validates with Zod and returns `202 Accepted` with the job id. The API records intent; it never runs the work.
- **Deploy** — two Docker images from one source tree, different entrypoints for server and worker.

<sub>Node.js &nbsp;·&nbsp; Express &nbsp;·&nbsp; MongoDB &nbsp;·&nbsp; Mongoose &nbsp;·&nbsp; WebSockets &nbsp;·&nbsp; React &nbsp;·&nbsp; Docker</sub>

[Source](https://github.com/KumarShourya001/Distributred_Job_Queue)

### Fashion recommender

Multimodal search over H&M's catalog — 71,664 articles with images, drawn from a dataset of 31M transactions. Search by photo, by description, or by both at once.

- **Why FashionCLIP** — generic CLIP scored every garment between 0.93 and 0.95, so ranking was close to arbitrary and a purple hoodie returned olive cardigans. Swapping in a fashion-fine-tuned CLIP fixed it with the rest of the pipeline untouched, which isolated the embedding model as the real quality lever.
- **Retrieval** — 512-dim embeddings in a FAISS `IndexFlatIP` over L2-normalised vectors, so inner product is cosine similarity. Image and text queries hit the same index, since CLIP puts both in a shared space.
- **Combined queries** — upload a jacket, add *"but in black"*: the normalised image and text vectors are averaged and re-normalised so the phrase steers the image result. MMR reranking stops one query returning a row of near-duplicates.
- **Outfit building** — visual neighbours within a category, plus items actually bought together, mined from transaction baskets and restricted to *different* categories so they complement rather than duplicate.
- **Benchmark** — MAP@12 ≈ 0.021 on the Kaggle H&M task across 1.37M customers, roughly double a popularity-only baseline.

<sub>PyTorch &nbsp;·&nbsp; FashionCLIP &nbsp;·&nbsp; FAISS &nbsp;·&nbsp; Gradio &nbsp;·&nbsp; Hugging Face</sub>

[**Try it**](https://huggingface.co/spaces/KrShourya/hm-fashion-recommender) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/fashion-recommender)

## Other things I've made

- **Vaidya.AI** — an edge-first clinical scribe. faster-whisper and Ollama turn a consultation into a structured note plus FHIR R4B resources, and every inference runs on the machine, so the audio never leaves it. &nbsp;[Live demo](https://vaidya-web.onrender.com) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/VAIDYA.AI)

- **KisanSaathi** — joins pesticide application records with community health reports on a shared spatial–temporal key, so an exposure spike is visible before it becomes a crisis. Offline-first PWA, voice capture in Hindi, Marathi and English. &nbsp;[Source](https://github.com/KumarShourya001/KisanSaathi)

- **DQN Atari** — DeepMind's Deep Q-Network rebuilt from the 2013 and 2015 papers. Experience replay, target network, frame stacking, epsilon-greedy decay, all from scratch; the agents learn from raw pixels. &nbsp;[Source](https://github.com/KumarShourya001/dqn-atari)

- **Hand-tracked flower** — real-time hand landmarks driving a procedurally rendered flower, petals opening with finger spread. &nbsp;[Try it](https://huggingface.co/spaces/KrShourya/hand-flower) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/flower_handtacker)

- **Cancer cell detection** — a CNN over roughly 1,100 CT scan images, using augmentation and transfer learning against a dataset far too small to train from scratch. &nbsp;[Source](https://github.com/KumarShourya001/cancer_cell_detction)

## Stack

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/stack-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/stack-light.svg">
  <img alt="Stack — Languages: Python, C++, TypeScript, JavaScript, Java, SQL. Frontend: React, Vite, Tailwind, PWA / offline-first. Backend: FastAPI, Node.js, Express, MongoDB, PostgreSQL, Docker. ML: PyTorch, TensorFlow, Keras, scikit-learn, OpenCV, FAISS, Transformers. Tooling: Git, Linux, GitHub Actions, Ollama, Vercel, Neon." src="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/stack-light.svg" width="100%">
</picture>

## Contributions

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/output/github-snake.svg">
  <img alt="A snake eating my GitHub contribution graph" src="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/output/github-snake.svg" width="100%">
</picture>

## Elsewhere

[LinkedIn](https://linkedin.com/in/kumar-shourya) &nbsp;·&nbsp; [Hugging Face](https://huggingface.co/KrShourya) &nbsp;·&nbsp; [Codeforces](https://codeforces.com/profile/Kumar_Shourya) &nbsp;·&nbsp; [LeetCode](https://leetcode.com/u/KShourya/) &nbsp;·&nbsp; [Email](mailto:kshourya2005@gmail.com)

<sub>Open to SDE and ML internships.</sub>
