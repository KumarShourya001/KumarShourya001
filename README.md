<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=210&section=header&text=Kumar%20Shourya&fontSize=62&fontColor=ffffff&animation=fadeIn&fontAlignY=34&desc=Software%20Engineering%20%C2%B7%20Full-Stack%20%C2%B7%20Applied%20ML&descAlignY=54&descSize=17" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&pause=1200&color=58A6FF&center=true&vCenter=true&width=680&lines=Building+edge-first+AI+systems;Multimodal+retrieval+and+deep+RL;FastAPI+%2B+React+%2B+everything+in+between;Solving+C%2B%2B+problems+on+Codeforces" alt="Typing SVG" />

<br/><br/>

<a href="https://github.com/KumarShourya001"><img src="https://komarev.com/ghpvc/?username=KumarShourya001&style=for-the-badge&color=58A6FF&labelColor=0d1117&label=PROFILE+VIEWS" /></a>
<a href="https://github.com/KumarShourya001?tab=followers"><img src="https://img.shields.io/github/followers/KumarShourya001?style=for-the-badge&color=58A6FF&labelColor=0d1117&label=FOLLOWERS" /></a>
<a href="https://nitp.ac.in"><img src="https://img.shields.io/badge/NIT_PATNA-CSE_'28-58A6FF?style=for-the-badge&labelColor=0d1117" /></a>

</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

## &nbsp;&nbsp;About

```yaml
name:      Kumar Shourya
education: B.Tech CSE, NIT Patna  (CGPA 8.49)
focus:     [ software engineering, full-stack development, applied ML ]
learning:  [ system design, competitive programming ]
building:  edge-first AI systems + multimodal retrieval
reach_me:  kshourya2005@gmail.com
```

> Most of what I build ends up deployed somewhere. I care about the part after the notebook — the API, the frontend, the container, the thing a stranger can actually open.

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

## &nbsp;&nbsp;Tech Stack

<table>
<tr>
<td width="140" valign="middle"><b>Languages</b></td>
<td><img src="https://skillicons.dev/icons?i=python,cpp,java,js,html,css&theme=dark" /></td>
</tr>
<tr>
<td width="140" valign="middle"><b>Frontend</b></td>
<td><img src="https://skillicons.dev/icons?i=react,vite,tailwind&theme=dark" /></td>
</tr>
<tr>
<td width="140" valign="middle"><b>Backend &amp; Data</b></td>
<td><img src="https://skillicons.dev/icons?i=fastapi,postgres,sqlite,docker&theme=dark" /></td>
</tr>
<tr>
<td width="140" valign="middle"><b>ML</b></td>
<td><img src="https://skillicons.dev/icons?i=pytorch,tensorflow,opencv,sklearn&theme=dark" /></td>
</tr>
<tr>
<td width="140" valign="middle"><b>Tooling</b></td>
<td><img src="https://skillicons.dev/icons?i=git,github,linux,vscode&theme=dark" /></td>
</tr>
</table>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

## &nbsp;&nbsp;Featured Work

<table>
<tr>
<td colspan="2" valign="top">

### &nbsp;Vaidya.AI &nbsp;·&nbsp; Edge-First Clinical Scribe

Records a doctor-patient consultation, transcribes it locally, and turns it into a structured clinical note plus **FHIR R4B** resources. All inference runs on the machine — audio never leaves it.

|  |  |
|---|---|
| **Local pipeline** | faster-whisper for speech, Ollama for generation. Switchable per request between `llama3.2:3b` (~8s) and `qwen2.5:7b` (better clinical read) |
| **Browser fallback** | No GPU on the host? whisper-tiny runs in-browser via transformers.js, a 1.5B model via WebGPU. The privacy claim holds on the web too |
| **Patient portfolio** | Conditions, allergies, medications and appointments behind auth — plus an emergency card readable *without* sign-in |
| **Grounded assistant** | Chatbot scoped to one patient's record. Refuses to recommend or alter medication, escalates on emergency symptoms |
| **Deploy** | Split: React/Vite frontend, containerised FastAPI backend, Postgres or SQLite |

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Whisper-412991?style=flat-square&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/Ollama-0d1117?style=flat-square&logo=ollama&logoColor=white" />
<img src="https://img.shields.io/badge/FHIR_R4B-E4002B?style=flat-square" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />

&nbsp;

[![Demo](https://img.shields.io/badge/▶%20Live%20Demo-46E3B7?style=for-the-badge&logoColor=black&labelColor=0d1117)](https://vaidya-web.onrender.com)
[![Repo](https://img.shields.io/badge/Source-0d1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KumarShourya001/VAIDYA.AI)

</td>
</tr>

<tr>
<td width="50%" valign="top">

### &nbsp;Fashion Recommender

Multimodal retrieval over H&M's catalog — **71K articles, 15M transactions**. Joint image-text embeddings via FashionCLIP, FAISS for sub-second search, MMR reranking so results don't collapse into twelve identical white shirts.

**MAP@12 ≈ 0.021** on the Kaggle benchmark.

<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" />
<img src="https://img.shields.io/badge/Gradio-FF7C00?style=flat-square&logo=gradio&logoColor=white" />

&nbsp;

[![Demo](https://img.shields.io/badge/▶%20Try%20It-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black&labelColor=0d1117)](https://huggingface.co/spaces/KrShourya/hm-fashion-recommender)
[![Repo](https://img.shields.io/badge/Source-0d1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KumarShourya001/fashion-recommender)

</td>
<td width="50%" valign="top">

### &nbsp;DQN Atari

DeepMind's Deep Q-Network rebuilt from the 2013 and 2015 papers. Agents learn Pong, Breakout and Space Invaders from **raw pixels**.

Training loop written from scratch — experience replay, target network with periodic sync, frame stacking, epsilon-greedy decay.

<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" />
<img src="https://img.shields.io/badge/Gym-0081A5?style=flat-square&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />

&nbsp;

[![Repo](https://img.shields.io/badge/Source-0d1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KumarShourya001/dqn-atari)

</td>
</tr>

<tr>
<td width="50%" valign="top">

### &nbsp;Cancer Cell Detection

CNN classifier over **~1,100 CT scan images**. Augmentation and transfer learning to fight a dataset far too small for training from scratch.

<img src="https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white" />
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />

&nbsp;

[![Repo](https://img.shields.io/badge/Source-0d1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KumarShourya001/cancer_cell_detction)

</td>
<td width="50%" valign="top">

### &nbsp;Hand-Tracked Flower

Real-time hand landmark tracking driving a procedurally rendered flower — petals respond to finger spread, neon glow shader on top.

<img src="https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=google&logoColor=white" />
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />

&nbsp;

[![Demo](https://img.shields.io/badge/▶%20Try%20It-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black&labelColor=0d1117)](https://huggingface.co/spaces/KrShourya/hand-flower)
[![Repo](https://img.shields.io/badge/Source-0d1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KumarShourya001/flower_handtacker)

</td>
</tr>
</table>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

## &nbsp;&nbsp;Currently

<table>
<tr>
<td width="33%" align="center"><b>Building</b><br/><sub>Full-stack projects with<br/>FastAPI + React</sub></td>
<td width="33%" align="center"><b>Learning</b><br/><sub>Low-level design,<br/>system architecture</sub></td>
<td width="33%" align="center"><b>Grinding</b><br/><sub>DSA in C++ on<br/>Codeforces &amp; LeetCode</sub></td>
</tr>
</table>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

<div align="center">

## &nbsp;&nbsp;Activity

<img width="58%" src="https://streak-stats.demolab.com?user=KumarShourya001&theme=tokyonight&hide_border=true&background=0d1117&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF" />

<br/><br/>

<img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=KumarShourya001&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=58A6FF&line=58A6FF&point=ffffff&area=true" />

</div>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

<div align="center">

### Contribution Snake

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/output/github-snake.svg" />
  <img alt="snake animation" src="https://raw.githubusercontent.com/KumarShourya001/KumarShourya001/output/github-snake.svg" />
</picture>

</div>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" />

<div align="center">

## &nbsp;&nbsp;Connect

<a href="https://linkedin.com/in/kumar-shourya"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:kshourya2005@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://huggingface.co/KrShourya"><img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" /></a>
<a href="https://codeforces.com/profile/Kumar_Shourya"><img src="https://img.shields.io/badge/Codeforces-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white" /></a>
<a href="https://leetcode.com/u/KShourya/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" /></a>

<br/><br/>

<i>Open to SDE and ML internship opportunities.</i>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer" width="100%" />

</div>
