<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-light.svg">
  <img alt="Kumar Shourya — software engineering, full-stack, applied ML" src="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-light.svg" width="100%">
</picture>

I care about the part that comes after the notebook — the API, the frontend, the container, the thing a stranger can actually open. Most of what I build ends up deployed somewhere.

<sub>B.Tech CSE at NIT Patna, CGPA 8.49 &nbsp;·&nbsp; Patna, India &nbsp;·&nbsp; <a href="mailto:kshourya2005@gmail.com">kshourya2005@gmail.com</a></sub>

## Selected work

### Distributed job queue

Jobs go in over HTTP, persist in MongoDB, get claimed by independent workers, and stream live to a React dashboard.

- **MongoDB is the broker** — no Redis, no RabbitMQ. One atomic `findOneAndUpdate` claims a job, so exactly one worker wins it however many are running.
- **Failure handling** — failed jobs retry, then dead-letter after three attempts. A sweeper reclaims anything a crashed worker left stranded for 30 seconds.
- **Live updates** — change streams push every state transition over WebSockets, so the dashboard never polls.

<sub>Node.js &nbsp;·&nbsp; Express &nbsp;·&nbsp; MongoDB &nbsp;·&nbsp; WebSockets &nbsp;·&nbsp; React &nbsp;·&nbsp; Docker</sub>

[Source](https://github.com/KumarShourya001/Distributred_Job_Queue)

### Fashion recommender

Multimodal search over H&M's catalog — 71,664 articles with images, from a dataset of 31M transactions. Search by photo, by text, or both at once.

- **Why FashionCLIP** — generic CLIP scored every garment between 0.93 and 0.95, so ranking was near-arbitrary. A fashion-tuned CLIP fixed it with the rest of the pipeline untouched, isolating the embedding model as the real lever.
- **Retrieval** — 512-dim embeddings in a FAISS `IndexFlatIP`; image and text queries hit the same index. Averaging both vectors lets *"but in black"* steer an image result, and MMR reranking kills near-duplicate rows.
- **Benchmark** — MAP@12 ≈ 0.021 on the Kaggle H&M task across 1.37M customers, roughly double a popularity-only baseline.

<sub>PyTorch &nbsp;·&nbsp; FashionCLIP &nbsp;·&nbsp; FAISS &nbsp;·&nbsp; Gradio</sub>

[**Try it**](https://huggingface.co/spaces/KrShourya/hm-fashion-recommender) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/fashion-recommender)

## Other things I've made

- **Vaidya.AI** — an edge-first clinical scribe. faster-whisper and Ollama turn a consultation into a structured note plus FHIR R4B resources, all on-machine, so the audio never leaves it. &nbsp;[Live demo](https://vaidya-web.onrender.com) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/VAIDYA.AI)

- **KisanSaathi** — joins pesticide records with community health reports on a shared spatial–temporal key, surfacing exposure spikes early. Offline-first PWA, voice capture in Hindi, Marathi and English. &nbsp;[Source](https://github.com/KumarShourya001/KisanSaathi)

- **DQN Atari** — DeepMind's Deep Q-Network rebuilt from the 2013 and 2015 papers, learning Atari from raw pixels. &nbsp;[Source](https://github.com/KumarShourya001/dqn-atari)

- **Hand-tracked flower** — real-time hand landmarks driving a procedurally rendered flower. &nbsp;[Try it](https://huggingface.co/spaces/KrShourya/hand-flower) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/flower_handtacker)

- **Cancer cell detection** — a CNN over roughly 1,100 CT scan images, with augmentation and transfer learning against a small dataset. &nbsp;[Source](https://github.com/KumarShourya001/cancer_cell_detction)

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
