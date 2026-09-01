<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-light.svg">
  <img alt="Kumar Shourya — software engineering, full-stack, applied ML" src="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/main/assets/hero-light.svg" width="100%">
</picture>

I care about the part that comes after the notebook — the API, the frontend, the container, the thing a stranger can actually open. Most of what I build ends up deployed somewhere. Right now that means an edge-first clinical scribe, an early-warning system for rural India, and a job queue that uses MongoDB as its own broker.

<sub>B.Tech CSE at NIT Patna, CGPA 8.49 &nbsp;·&nbsp; Patna, India &nbsp;·&nbsp; <a href="mailto:kshourya2005@gmail.com">kshourya2005@gmail.com</a></sub>

## Selected work

### Vaidya.AI — an edge-first clinical scribe

Records a doctor–patient consultation, transcribes it locally, and turns it into a structured clinical note plus **FHIR R4B** resources. Every inference runs on the machine. The audio never leaves it.

- **Local pipeline** — faster-whisper for speech, Ollama for generation. Switchable per request between `llama3.2:3b` (about 8s) and `qwen2.5:7b`, which reads clinical language better.
- **Browser fallback** — no GPU on the host? whisper-tiny runs in-browser through transformers.js, with a 1.5B model on WebGPU. The privacy claim survives the move to the web.
- **Patient portfolio** — conditions, allergies, medications and appointments behind auth, plus an emergency card that stays readable *without* signing in.
- **Grounded assistant** — a chatbot scoped to one patient's record. It refuses to recommend or alter medication, and escalates on emergency symptoms.
- **Deploy** — React/Vite frontend, containerised FastAPI backend, Postgres or SQLite.

<sub>FastAPI &nbsp;·&nbsp; React &nbsp;·&nbsp; faster-whisper &nbsp;·&nbsp; Ollama &nbsp;·&nbsp; FHIR R4B &nbsp;·&nbsp; Docker</sub>

[**Live demo**](https://vaidya-web.onrender.com) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/VAIDYA.AI)

<table>
<tr>
<td width="58%" valign="top">

### KisanSaathi

A pesticide application record and a dermal symptom report mean little apart. Joined on a shared spatial–temporal key, they become an early warning — and neither a health system nor an agriculture system can raise that flag alone.

Built around Yavatmal district, Maharashtra, after the 2017 organophosphate poisoning cluster. Offline-first — records survive a force-kill and sync idempotently — with voice capture in Hindi, Marathi and English.

<sub>React 19 &nbsp;·&nbsp; TypeScript &nbsp;·&nbsp; Dexie/IndexedDB &nbsp;·&nbsp; Neon Postgres &nbsp;·&nbsp; PGlite &nbsp;·&nbsp; Vercel</sub>

[Source](https://github.com/KumarShourya001/KisanSaathi)

</td>
<td width="42%" valign="top">

### Distributed job queue

MongoDB *is* the queue — no Redis, no RabbitMQ. A single atomic `findOneAndUpdate` is what stops two workers claiming the same job.

Retries with a dead-letter after three attempts, a sweeper that reclaims jobs stranded by a crashed worker, and change streams pushing every state transition to a React dashboard over WebSockets.

<sub>Node.js &nbsp;·&nbsp; Express &nbsp;·&nbsp; MongoDB &nbsp;·&nbsp; WebSockets &nbsp;·&nbsp; Docker</sub>

[Source](https://github.com/KumarShourya001/Distributred_Job_Queue)

</td>
</tr>
<tr>
<td width="58%" valign="top">

### Fashion recommender

Multimodal retrieval over H&M's catalog — 71K articles, 15M transactions. Joint image–text embeddings from FashionCLIP, FAISS for sub-second search, MMR reranking so the results don't collapse into twelve identical white shirts.

**MAP@12 ≈ 0.021** on the Kaggle benchmark.

<sub>PyTorch &nbsp;·&nbsp; FashionCLIP &nbsp;·&nbsp; FAISS &nbsp;·&nbsp; Gradio</sub>

[**Try it**](https://huggingface.co/spaces/KrShourya/hm-fashion-recommender) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/fashion-recommender)

</td>
<td width="42%" valign="top">

### DQN Atari

DeepMind's Deep Q-Network rebuilt from the 2013 and 2015 papers. The agents learn Pong, Breakout and Space Invaders from raw pixels.

Training loop written from scratch: experience replay, a target network on periodic sync, frame stacking, epsilon-greedy decay.

<sub>TensorFlow &nbsp;·&nbsp; Gym &nbsp;·&nbsp; NumPy</sub>

[Source](https://github.com/KumarShourya001/dqn-atari)

</td>
</tr>
<tr>
<td width="58%" valign="top">

### Hand-tracked flower

Real-time hand landmark tracking driving a procedurally rendered flower. The petals open with finger spread, and a neon glow shader sits on top.

<sub>MediaPipe &nbsp;·&nbsp; OpenCV</sub>

[**Try it**](https://huggingface.co/spaces/KrShourya/hand-flower) &nbsp;·&nbsp; [Source](https://github.com/KumarShourya001/flower_handtacker)

</td>
<td width="42%" valign="top">

### Cancer cell detection

A CNN classifier over roughly 1,100 CT scan images, using augmentation and transfer learning to fight a dataset far too small to train from scratch.

<sub>Keras &nbsp;·&nbsp; OpenCV</sub>

[Source](https://github.com/KumarShourya001/cancer_cell_detction)

</td>
</tr>
</table>

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
