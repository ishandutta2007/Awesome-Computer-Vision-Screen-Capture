# Awesome-Computer-Vision-Screen-Capture

# Top Computer Vision & Screen Capture Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Screen Capture, UI Automation & Vision-Based Agent Perception*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Computer Vision & Screen Capture**. These tools enable automation platforms and AI agents to perceive screen state, identify UI elements, and execute actions—from high-performance capture libraries to vision-based RPA engines.

**Examples** include UiPath Computer Vision, Automation Anywhere, Blue Prism, WorkFusion, Kofax RPA, Microsoft Power Automate Desktop, Nintex, Pega Robotic Automation, ABBYY Vantage, and Appian RPA (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, high-FPS screen capture, and vision-based UI automation—ideal for RPA developers, AI agent engineers, and organizations seeking transparent, vendor-independent automation infrastructure.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[UiPath Computer Vision](https://www.uipath.com/)**  
  **Enterprise RPA platform with AI-powered computer vision** for UI element detection. Enables automation of virtual desktops, Citrix environments, and remote applications without traditional selectors.

- **[Automation Anywhere](https://www.automationanywhere.com/)**  
  **Cloud-native RPA platform** with **A2019** and **Automation 360**. Features **IQ Bot** for document processing and **Bot Insight** for analytics.

- **[Blue Prism](https://www.blueprism.com/)**  
  **Enterprise RPA platform** (SS&C) with **digital workforce** management, **process intelligence**, and **intelligent automation** capabilities.

- **[Microsoft Power Automate Desktop](https://powerautomate.microsoft.com/)**  
  **Free desktop automation** for Windows—**included with Windows 10/11** . Features **UI automation**, **web automation**, **Excel/Outlook integration**, and **AI Builder**.

- **[Kofax RPA](https://www.kofax.com/)**  
  **Enterprise RPA and cognitive automation** with **document intelligence** and **process orchestration** .

- **[WorkFusion](https://www.workfusion.com/)**  
  **Intelligent automation** for financial services—**AML, KYC, and customer onboarding** .

- **[Nintex](https://www.nintex.com/)**  
  **Process automation platform** with **workflow, forms, RPA, and document generation** .

- **[Pega Robotic Automation](https://www.pega.com/)**  
  **RPA integrated with Pega's decisioning and workflow platform** .

- **[ABBYY Vantage](https://www.abbyy.com/)**  
  **Document AI platform** with **pre-trained AI skills** for document processing and data extraction.

- **[Appian RPA](https://www.appian.com/)**  
  **Low-code automation with RPA capabilities** integrated into the Appian platform.

## Open-Source GitHub Projects

- **[DXcam](https://github.com/ra1nty/DXcam)**  
  **A Python high-performance screen capture library for Windows using Desktop Duplication API** (MIT) . **The most important open-source screen capture library for computer-use agents**—**802 GitHub stars** and actively maintained through 2026  . **Capable of 240Hz+ capturing**—**benchmarked at 239.19 average FPS vs. python-mss at 75.87 and D3DShot at 118.36**  . **Captures Direct3D exclusive full-screen applications without interrupting, even during alt+tab**  . **Dual backends**: **dxgi** (default Desktop Duplication) and **winrt** (Windows Graphics Capture)—use **dxgi for most workloads, winrt if cursor rendering is needed**  . **Automatic handling of scaled/stretched resolution**  . **Seamless integration with NumPy, OpenCV, and PyTorch**  . **`grab()` returns a numpy array**; **`copy=False` or `camera.grab_view()` for zero-copy views**  . **Screen capture mode** spins up a thread that polls newly rendered frames into an **in-memory ring buffer** with **`get_latest_frame()` blocking until new frame available**  . **Target FPS pacing** via **Windows high-resolution timer** (±1ms accuracy vs. Python's 16ms)  . **`video_mode=True`** fills buffer at target FPS using last frame when no new frame rendered  . **The reference implementation for agent screen perception** .

- **[RapidShot](https://pypi.org/project/rapidshot/)**  
  **The DXcam successor with rewritten capture path, colour pipeline, and GPU interop** (open-source)  . **Benchmarked at 80.3 frames/s vs. DXcam's 68.1** in a YOLO11n inference pipeline—**up to 20% more frames, pixels up to 9% younger, and up to a third less CPU per frame**  . **GPU-resident frames**—skips the CPU round-trip entirely for consumers that feed a model  . **Colour conversion is essentially free** with the optional native extension: **BGRA→RGB in 0.31 ms and BGRA→GRAY in 0.26 ms per 1080p frame**  . **`timeout_ms` is the key differentiator**: default **10ms waits for compositor to present** (15.7% CPU), vs. **0ms polling** (68.6% CPU, only 2.4% hit rate vs. 100% at 10ms)  . **The most efficient open-source screen capture for ML pipelines** .

- **[BetterCam](https://github.com/dyddnrdld/BetterCam)**  
  **World's Fastest high-performance Python screen capture library for Windows using Desktop Duplication API** (open-source)  . **Born from DXCam**—focuses on **240Hz+ capturing** and **Direct3D exclusive full-screen capture**  . **Nvidia GPU variant** available for hardware-accelerated capture  . **Benchmarks**: BetterCam at **123.667 FPS** vs. DXCam at **39 FPS** in target FPS tests  . **The performance-focused DXcam fork** .

- **[DXcamPIL](https://github.com/hite4044/DXcamPIL)**  
  **DXcam with PIL support**—**only needs PIL and comtypes to run** (open-source)  . **Reduced dependency footprint**—**90+ FPS** performance vs. DXcam's full feature set  . **The lightweight DXcam variant** for environments where installing OpenCV is impractical .

- **[OAGI](https://pypi.org/project/oagi-core/)**  
  **Python SDK for OAGI API—vision-based task automation** (open-source)  . **The most complete open-source vision-based automation SDK** . **Features**: **`single_step()`** for screenshot analysis and recommended actions, **`ShortTask.auto_mode()`** for automated task execution with screenshot capture and action execution, **PyAutoGUI integration** for mouse/keyboard control, **ScreenshotMaker** for image capture, and **image compression** for token efficiency  . **Async support** for non-blocking operations  . **The reference implementation for vision-based RPA** .

- **[Screenwise Framework](https://pypi.org/project/t-screenwise/)**  
  **Python framework for screen element detection and interaction using computer vision and machine learning** (open-source)  . **Features**: **screenshot capture and analysis**, **ML-based element detection**, **coordinate-based interaction**, **OCR capabilities**, **debug and capture modes**, and **cross-platform support**  . **Operating modes**: **CAPTURE** (live interaction with screen elements) and **DEBUG** (visualization without actual interaction)  . **OCR spatial analysis** via `get_nearest_boxes()`—find nearest elements in all directions with overlap consideration  . **The most feature-complete open-source UI element detection framework** .

- **[Chivel](https://socket.dev/pypi/package/chivel/overview/0.8.1)**  
  **Computer vision, OCR, and input automation toolkit** (open-source)  . **The most concise API for screen automation**—**`find_image()` for template matching**, **`find_text()` for OCR search**, **`find_any()` and **`find_all()`** for multi-term searches, **`expect_any()` and **`expect_all()`** for polling waits  . **Mouse and keyboard APIs** for interaction  . **The most accessible open-source toolkit for vision-based automation** .

- **[rustcam](https://socket.dev/pypi/package/rustcam/overview/0.1.2)**  
  **Rust-based screen capture** (open-source)  . **Benchmarked at 157 FPS in `flip_demo` and 146 FPS in `mover.py`** vs. DXcam at **129/125 FPS** and BetterCam at **157/146 FPS**  . **Pulls every frame Desktop Duplication hands over** (~196 FPS on a 180Hz panel)  . **The Rust-native alternative** for capture pipelines that need maximum throughput .

### Additional Strong Open-Source Options

- **[python-mss](https://github.com/BoboTiG/python-mss)** — Cross-platform screenshot library (MIT) . **The standard cross-platform capture library**—**75.87 FPS on Windows vs. DXcam's 239.19**  . **Best for**: cross-platform applications where DXcam's Windows-only limitation is unacceptable .
- **[D3DShot](https://github.com/SerpentAI/D3DShot)** — Windows screenshot library (MIT) . **118.36 FPS**—**the DXcam predecessor** with Desktop Duplication API  .
- **[PyAutoGUI](https://github.com/asweigart/pyautogui)** — Cross-platform GUI automation (BSD-3-Clause) . **The standard for mouse/keyboard control**—**OAGI uses PyAutoGUI for action execution**  .
- **[OpenCV](https://github.com/opencv/opencv)** — Computer vision library (Apache-2.0) . **The foundation for template matching and image processing** in screen automation .
- **[PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)** — Multilingual OCR (Apache-2.0) . **The OCR engine behind ThinkDrop Vision Service**  .
- **[MiniCPM-V](https://github.com/OpenBMB/MiniCPM-V)** — Vision-language model (open-source) . **The VLM behind ThinkDrop Vision Service**  .
- Community **n8n** workflows for screen capture automation and vision-based alerting.

**Frameworks for building custom systems**: Combine **DXcam** or **RapidShot** for high-FPS screen capture with **Chivel** or **Screenwise** for UI element detection, **OAGI** for vision-based task automation, and **PyAutoGUI** for action execution—creating a fully open-source, computer-use agent perception stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Computer vision and screen capture tools must respect privacy, consent requirements, and applicable wiretapping laws. **Never capture screens without authorization** .
- **Open-source screen capture is mature and production-ready.** DXcam is the most widely adopted library for agent screen perception with 802 GitHub stars and 239 FPS capture  . RapidShot improves on DXcam with GPU-resident frames and efficient `timeout_ms` pacing  . **These are genuine alternatives to commercial screen capture** .
- **DXcam vs. RapidShot: the trade-off is frames vs. CPU.** DXcam polling (`AcquireNextFrame(0)`) reaches **134 FPS at 66% CPU** . RapidShot's default **10ms timeout waits for compositor to present**—**118.9 FPS at 15.7% CPU**  . **The frame rate barely moves; the CPU moves by more than four times** . **Use RapidShot if capture is one stage of a pipeline that needs its cores** .
- **Capture library choice depends on your stack.** DXcam for **maximum compatibility and broad adoption** . RapidShot for **GPU-resident frames and efficient CPU usage** . BetterCam for **Nvidia GPU acceleration** . DXcamPIL for **minimal dependencies** . rustcam for **Rust-native pipelines**  .
- **Vision-based automation is the emerging category.** OAGI provides **single-step analysis** and **automated task execution** via screenshot capture and PyAutoGUI  . Screenwise provides **ML-based element detection** with OCR spatial analysis  . Chivel provides **the most concise API** for template matching and OCR search  . **These tools enable AI agents to perceive and act on any UI** .
- Self-hosted open-source solutions require proper GPU provisioning for VLMs, screen capture permissions, and ongoing maintenance. **Screen capture is privacy-sensitive**—implement appropriate access controls and audit logging .

---

**Made for RPA developers, AI agent engineers, and organizations building transparent automation solutions.**  
Let's make Computer Vision & Screen Capture more open, data-driven, and agent-native.
