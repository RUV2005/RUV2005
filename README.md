<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f6feb,100:58a6ff&height=180&section=header&text=Danmo&fontSize=56&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Accessibility%20Developer%20%C2%B7%20On-device%20AI%20%C2%B7%20Mobile%20%26%20Desktop%20Systems&descAlignY=58&descSize=16" width="100%">

<p align="center">
  <a href="mailto:danmo6321@gmail.com"><img src="https://img.shields.io/badge/Email-danmo6321%40gmail.com-0078D4?style=flat&logo=microsoft-outlook&logoColor=white" alt="Email"></a>
  <a href="https://guangji.online"><img src="https://img.shields.io/badge/Website-guangji.online-58A6FF?style=flat&logo=googlechrome&logoColor=white" alt="Website"></a>
  <img src="https://img.shields.io/badge/Focus-Accessibility%20%2F%20Assistive%20Tech-2ea44f?style=flat" alt="Focus">
  <img src="https://img.shields.io/badge/Based%20in-Xi'an%2C%20China-8957e5?style=flat" alt="Location">
</p>

<p align="right"><b>Language:</b> English | <a href="#中文版">中文</a></p>

## 🧑‍💻 About Me

I am an **accessibility-first developer**. I build tools for blind and low-vision users — and, more importantly, I build them *with* blind and low-vision users: a real user community on Xiaohongshu and WeChat tests my builds, files issues and argues about details with me. That feedback loop is my actual development method.

My work lives at the intersection of three things:

- **Assistive products** — browsers, OCR readers and navigation aids designed for screen-reader and voice-first workflows from day one
- **On-device AI** — vision and language models that run locally (TensorFlow Lite, llama.cpp / GGUF), because assistive tools must work offline and must never upload what a user is looking at
- **Systems underneath** — Linux, Docker, and hands-on enterprise server hardware (rack servers, RAID, BMC remote management), so the products above rest on skills I have actually practiced

> A visually impaired user once described what she wanted from image description in five words: *"I just want to know what's in the picture."* That sentence is the spec for most of what I build.

---

## 🚀 Featured Projects

### 🌐 Intelnet Browser （明镜浏览器） — *main project*

[![Repo](https://img.shields.io/badge/GitHub-RUV2005%2Fintelnet--browser-181717?logo=github)](https://github.com/RUV2005/intelnet-browser)
![C++](https://img.shields.io/badge/C%2B%2B-Qt%20WebEngine-00599C?logo=cplusplus)
![License](https://img.shields.io/badge/License-GPLv3-blue)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows)

A desktop browser designed from the start for screen-reader and low-vision users. Accessibility here is the architecture, not a plugin.

- **Local image description** — Qwen2-VL-2B-Instruct in GGUF form (llama.cpp runtime), fully on-device. The image never leaves the computer.
- **Reading pipeline** — page simplification, element translation and reading order tuned for assistive navigation
- **Distribution** — installers served from Cloudflare R2, site and docs at [guangji.online](https://guangji.online)
- **License** — GPLv3, deliberately: assistive tooling built on public work should stay public

```mermaid
graph LR
    A[WebEngine Page] --> B[Accessibility Tree<br/>+ Reading Pipeline]
    B --> C[Image Nodes]
    C --> D[llama.cpp Runtime]
    D --> E[Qwen2-VL-2B GGUF<br/>local inference]
    E --> F[Spoken Description<br/>via Screen Reader / TTS]
    B --> G[Simplified Reading View]
```

### 👁️ [guide](https://github.com/RUV2005/guide) — spatial awareness for blind users

![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?logo=kotlin)
![TFLite](https://img.shields.io/badge/TensorFlow%20Lite-on--device-FF6F00?logo=tensorflow)

Real-time object detection on Android that answers two questions for a blind user: *what is around me, and in which direction?*

- On-device detection (TensorFlow Lite), no network dependency outdoors
- Direction-aware feedback: results are mapped to clock-face directions and delivered by voice + vibration patterns
- Designed for one-handed, eyes-free operation

### 📖 [mingmou](https://github.com/RUV2005/mingmou) — OCR reading assistant

![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?logo=kotlin)
![MLKit](https://img.shields.io/badge/ML%20Kit-OCR-FF6F00?logo=google)

Reading assistant for low-vision users, built for classrooms and paper books.

- Hybrid recognition: cloud OCR when online, on-device OCR when not
- External camera support: an ESP32-CAM streams over its own access point, so the phone can stay in a pocket while the camera sits on the book
- Voice-first UI throughout

### 🎵 [Kalimba](https://github.com/RUV2005/Kalimba) — accessible music practice

![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?logo=kotlin)

A kalimba practice app whose entire interface can be operated by voice and gesture alone — practice, tuning feedback and progress tracking without looking at the screen.

---

## 🧰 Technical Toolbox

<p align="center">
  <img src="https://skillicons.dev/icons?i=kotlin,swift,cpp,qt,cs,python,ts,js&perline=8" alt="Languages and frameworks"><br>
  <img src="https://skillicons.dev/icons?i=docker,linux,git,github,cloudflare,androidstudio,xcode,vscode&perline=8" alt="Platforms and tools">
</p>

| Domain | What I actually work with | Evidence |
|---|---|---|
| Android | Kotlin, CameraX, TensorFlow Lite, accessibility services | guide, mingmou, Kalimba |
| iOS / macOS | Swift, SwiftUI, Speech framework, sideload CI pipelines | caption tooling, SwiftUI apps |
| Desktop | C++ / Qt WebEngine, C# / WPF | Intelnet Browser, Windows utilities |
| On-device AI | llama.cpp / GGUF, TFLite, model quantization trade-offs | local image description in production |
| Systems & Ops | Linux, Docker, server hardware, RAID, BMC remote management | hands-on with enterprise rack servers (hardware, install, troubleshooting) |
| Hardware | PCB design (KiCad, learning in public), ESP32, board-level repair | caption glasses prototype |

---

## 📊 Development Analytics

<div align="center">

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=RUV2005&show_icons=true&theme=react&hide_border=true)](https://github.com/anuraghazra/github-readme-stats)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=RUV2005&layout=compact&theme=react&hide_border=true)](https://github.com/anuraghazra/github-readme-stats)

[![Contribution Graph](https://github-readme-activity-graph.vercel.app/graph?username=RUV2005&theme=react-dark&hide_border=true&area=true)](https://github.com/ashutosh00710/github-readme-activity-graph)

</div>

---

## 🧭 Current Trajectory

| Direction | Status |
|---|---|
| Intelnet Browser: local image description | ✅ shipped, iterating with user feedback |
| Intelnet Browser: captions for any video, generated in the browser itself | 🔨 in development |
| Real-time caption glasses (phone-side speech-to-text + custom PCB hardware) | 🔨 prototyping |
| Kubernetes & cloud-native ops | 🌱 learning on my laptop (WSL + k3d + VMs) |
| PCB design, KiCad → first self-designed power board | 🌱 learning |

---

## 📣 Contact

- **Email:** danmo6321@gmail.com
- **Site:** [guangji.online](https://guangji.online)
- **Issues & ideas:** the fastest way to reach me about any project is opening an issue in its repo

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58a6ff,50:1f6feb,100:0d1117&height=110&section=footer" width="100%">

---

<div id="中文版">

## 中文版

你好，我是 Danmo，一名以无障碍为先的开发者。

我给视障用户做工具，而且是和他们一起做：小红书和微信上有真实的视障用户社群在测我的版本、提 issue、跟我争细节。这个反馈闭环就是我的开发方法。

### 主要项目

- **明镜浏览器（intelnet-browser）**：主线项目。为读屏和低视力用户从架构层设计的桌面浏览器，核心是完全本地运行的图片描述（Qwen2-VL GGUF 模型，图片不出设备），GPLv3 开源，官网 guangji.online。
- **guide**：给盲人用的实时物体识别，回答“周围有什么、在哪个方向”，语音加震动反馈，全程本地推理。
- **mingmou（明眸）**：给低视力用户的 OCR 阅读助手，读课件、黑板和纸书，可接 ESP32-CAM 外置摄像头。
- **Kalimba**：全语音界面的卡林巴练习应用。

### 技术面

Android（Kotlin）、iOS（Swift / SwiftUI）、桌面端（C++ / Qt、C# / WPF）、端侧 AI（TensorFlow Lite、llama.cpp / GGUF）、Linux 与服务器运维（有企业级机架服务器的拆装、装机与排障实操），目前在自学 PCB 设计和 Kubernetes，给自研的实时字幕眼镜做硬件原型。

### 联系

danmo6321@gmail.com ｜ [guangji.online](https://guangji.online)

</div>
