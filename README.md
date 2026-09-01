<h1 align="center">Issam Sayyaf</h1>

<p align="center">
  <b>Edge AI &amp; Sensor Algorithms Engineer</b> · TDK InvenSense (Movea SAS), Grenoble<br>
  <sub>I turn raw sensor streams into models that run in kilobytes.</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/C%2FC%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/TFLite%20Micro-FF6F00?style=flat-square&logo=tensorflow&logoColor=white">
  <img src="https://img.shields.io/badge/CMSIS--NN%2FDSP-0091BD?style=flat-square&logo=arm&logoColor=white">
  <img src="https://img.shields.io/badge/Zephyr-7B2CBF?style=flat-square&logo=zephyrprojectrtos&logoColor=white">
  <img src="https://img.shields.io/badge/Yocto-1E4F8A?style=flat-square&logo=yocto&logoColor=white">
  <img src="https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white">
  <img src="https://img.shields.io/badge/nRF-00A9CE?style=flat-square&logo=nordicsemiconductor&logoColor=white">
</p>

---

### What I work on

I design DSP front-ends and small deep learning models for time-series sensor data:
IMU, microphone, ultrasonic ToF, pressure, magnetometer. The models ship on MCUs
and embedded Linux, not on servers. Every design choice is a budget choice.

```mermaid
flowchart LR
  A["Sensor<br/>IMU · mic · ToF"] --> B["DSP front-end<br/>filter · window · FFT"]
  B --> C["Feature / embedding<br/>fixed point"]
  C --> D["Tiny model<br/>CNN · TCN · LSTM · Transformer"]
  D --> E["int8 deploy<br/>TFLM · CMSIS-NN"]
  E --> F["MCU / edge Linux<br/>kB RAM · mW power"]
```

### Design rules I follow

- **Budget first.** Flash, RAM (tensor arena included), latency per window, and mA before architecture.
- **int8 by default.** Float is a debug mode, not a product.
- **Move work into the front-end.** A good feature is cheaper than four extra layers.
- **Measure on target.** Cycle counts on the device, not FLOPs on a slide.
- **Streaming, not batches.** Ring buffers, fixed windows, bounded worst-case time.

### Selected work

| Project | What it does | Footprint |
|---|---|---|
| [`repo-name`](#) | Anomaly detection for multi-sensor positioning (IMU / 5G / GNSS) | `— kB flash` · `— kB RAM` · `— ms/window` |
| [`repo-name`](#) | Real-time IMU activity / gesture pipeline on Cortex-M | `— kB flash` · `— kB RAM` · `— ms/window` |
| [`repo-name`](#) | Audio front-end and keyword model for MCU class devices | `— kB flash` · `— kB RAM` · `— ms/window` |
| [`repo-name`](#) | Yocto BSP with secure boot (TF-A, OP-TEE, dm-verity) and SWUpdate OTA | — |

<sub>Numbers are measured on target, not estimated.</sub>

### Research

- **PhD**, Université Gustave Eiffel — GEOLOC Lab, Nantes (2026).
  AI-based anomaly detection for resilient multi-sensor positioning.
- **MSc**, Università della Calabria — 110/110 cum laude.
- 10+ IEEE papers on sensor fusion, anomaly detection, and time-series deep learning.
  → [Google Scholar](#) · [ORCID](#)

### Now

- Sensor algorithms and edge AI at TDK InvenSense.
- Writing a unified, modality-independent framework for positioning anomaly detection.
- Reading and notes on TDK sensor families: SmartMotion IMU, SmartSound mic, SmartSonic ToF, Hall / TMR.

<p align="center">
  <a href="#">LinkedIn</a> ·
  <a href="#">Scholar</a> ·
  <a href="mailto:you@example.com">Email</a>
</p>
