# NVIDIA MPV Portable Config

A portable, NVIDIA-focused **MPV configuration** designed for high-quality video playback, accurate color reproduction, HDR processing, and GPU-accelerated rendering on Windows PCs equipped with NVIDIA GPUs.

The configuration is optimized for modern NVIDIA GeForce GPUs and is intended for users who want a **high-quality media playback experience without installing or modifying system-wide MPV configuration files**.

---

## ✨ Features

* 🎬 High-quality video playback
* 🟢 NVIDIA GPU hardware decoding
* ⚡ NVDEC hardware acceleration
* 🎨 High-quality color reproduction
* 🌈 HDR10 playback
* 🔄 HDR → SDR tone mapping
* 🖥️ Vulkan GPU rendering
* 🚀 NVIDIA GPU acceleration
* 🧠 GPU-based video processing
* 🔍 High-quality image scaling
* 🎞️ 4K / 60 FPS playback
* 🔊 High-quality audio passthrough
* 🎯 Display synchronization
* 🧩 Portable configuration
* 💾 No system-wide MPV configuration required
* 🖥️ Optimized for NVIDIA GeForce RTX GPUs

---

## 🎯 Project Goal

The goal of this project is to provide a **ready-to-use MPV configuration for NVIDIA GPUs** that prioritizes:

1. **Video quality**
2. **Color accuracy**
3. **HDR reproduction**
4. **Smooth playback**
5. **GPU acceleration**
6. **Efficient hardware decoding**
7. **Consistent rendering**

This configuration is intended primarily for users who care about **image quality and color reproduction**, rather than simply minimizing GPU usage.

---

## 🖥️ Supported NVIDIA GPUs

The configuration is designed for modern NVIDIA GPUs, including:

* GeForce RTX 20 Series
* GeForce RTX 30 Series
* GeForce RTX 40 Series
* GeForce RTX 50 Series

It may also work with older NVIDIA GPUs depending on their supported NVDEC capabilities and driver support.

### Recommended

For the best experience:

* NVIDIA GeForce RTX GPU
* Updated NVIDIA graphics driver
* Windows 10 / Windows 11
* Vulkan-capable GPU
* HDR-capable display for HDR playback

---

## 🎨 Color & Image Quality

This configuration focuses heavily on the video rendering pipeline.

The goal is to preserve the source video's intended image characteristics while providing high-quality GPU processing.

Depending on the selected configuration, the pipeline can include:

* Accurate color management
* ICC display profile support
* HDR10 processing
* BT.2020 handling
* PQ transfer characteristics
* HDR → SDR tone mapping
* High-quality chroma processing
* GPU-based scaling
* GPU shader processing
* Full-resolution rendering

### Color Management

When color management is enabled, MPV can use the display's ICC profile to help produce more accurate colors.

This is particularly useful for users with:

* Calibrated displays
* Wide-gamut monitors
* HDR monitors
* Professional displays
* High-quality IPS/OLED panels

---

## 🌈 HDR Support

The configuration is designed for modern HDR content, including:

* HDR10
* BT.2020
* PQ / ST 2084

It can also be configured for **HDR → SDR tone mapping** when playing HDR content on an SDR display.

This allows HDR content to remain watchable without requiring an HDR monitor.

> HDR quality ultimately depends on the display, NVIDIA driver configuration, MPV settings, and the source material.

---

## ⚡ NVIDIA Hardware Decoding

The configuration uses NVIDIA's hardware video decoding capabilities where supported.

Hardware decoding moves supported video decoding workloads from the CPU to the NVIDIA GPU.

This can significantly reduce CPU utilization when playing demanding formats such as:

* H.264 / AVC
* H.265 / HEVC
* VP9
* AV1

Actual codec support depends on the NVIDIA GPU generation and driver.

---

## 🖥️ Vulkan Rendering

The configuration uses MPV's GPU rendering pipeline with Vulkan where supported.

Vulkan provides a modern graphics API that can be used for:

* Video rendering
* Scaling
* Shaders
* HDR processing
* Color management
* GPU-based video filters

The NVIDIA GPU handles the majority of the rendering workload.

---

## 🎞️ 4K / 60 FPS Playback

The configuration is designed with high-resolution media in mind.

Recommended workloads include:

* 1080p
* 1440p
* 4K UHD
* 4K HDR
* 60 FPS content
* High-bitrate video

Performance will depend on the NVIDIA GPU, CPU, display refresh rate, video codec, bitrate, and enabled processing.

---

## 📁 Portable Configuration

One of the main purposes of this project is portability.

The configuration can be kept together with MPV instead of being installed into the user's system configuration directory.

Example:

```text
mpv-portable-config/
│
├── portable_config/
│   ├── mpv.conf
│   ├── input.conf
│   ├── profiles.conf
│   ├── shaders/
│   └── scripts/
│
└── README.md
```

This makes it easier to:

* Move the configuration between PCs
* Keep MPV settings separate from the system
* Maintain a dedicated NVIDIA configuration
* Back up the entire setup
* Use the configuration from portable MPV installations
* Experiment without modifying the normal MPV configuration

---

## 🚀 Installation

### 1. Download MPV

Download a Windows build of MPV.

### 2. Download this repository

Clone the repository:

```bash
git clone https://github.com/Pavan-Kotian/mpv-portable-config.git
```

Or download the repository as a ZIP file.

### 3. Place the configuration

Copy the contents of `portable_config` into the appropriate portable MPV configuration directory.

The final structure should resemble:

```text
mpv/
├── mpv.exe
├── mpv.com
├── portable_config/
│   ├── mpv.conf
│   ├── input.conf
│   ├── profiles.conf
│   └── ...
```

### 4. Launch MPV

Start MPV normally and verify the configuration is being loaded.

---

## 🔎 Verify NVIDIA GPU Usage

While playing a video, open MPV's statistics with:

```text
Shift + I
```

Depending on the MPV version and configuration, the statistics can provide information about:

* Decoder
* Video output
* Rendering
* Dropped frames
* Display synchronization
* GPU processing

You can also verify GPU activity using **Windows Task Manager → Performance → GPU**.

---

## ⚙️ Configuration Philosophy

This project does **not** attempt to maximize every available MPV option.

Instead, the configuration is designed around a balanced rendering pipeline:

```text
Video File
    ↓
Demuxer
    ↓
FFmpeg Decoder
    ↓
NVIDIA Hardware Decoding / NVDEC
    ↓
GPU Video Processing
    ↓
Color Management
    ↓
HDR / Tone Mapping
    ↓
Scaling / Shaders
    ↓
Vulkan Renderer
    ↓
Display
```

The objective is to maintain a high-quality image while keeping the playback pipeline stable.

---

## 🎨 Recommended Use Cases

This configuration is particularly suitable for:

* 🎬 Movies
* 📺 TV shows
* 🎞️ Anime
* 🌈 HDR10 content
* 🖥️ 4K UHD video
* 🎥 High-bitrate Blu-ray/WEB-DL content
* 🎮 Game cinematics
* 🖼️ Users with calibrated or wide-gamut displays

---

## ⚠️ Important Notes

### GPU Requirements

Some advanced rendering options can significantly increase GPU utilization.

A configuration that works well on an RTX 4050 may not provide the same performance on an older GPU.

### HDR

HDR playback requires an HDR-capable display for native HDR output.

HDR → SDR tone mapping should be used when the target display does not support HDR.

### Color Accuracy

No software configuration can compensate for an inaccurate or poorly calibrated display.

The final image depends on:

* Source mastering
* Display characteristics
* ICC profile
* Windows HDR settings
* NVIDIA driver settings
* MPV color management
* Viewing environment

### Drivers

Using a current NVIDIA graphics driver is recommended.

---

## 🧪 Testing

The configuration should ideally be tested with different types of content:

| Content            | Recommended Test      |
| ------------------ | --------------------- |
| 1080p H.264        | CPU/GPU efficiency    |
| 1080p HEVC         | Hardware decoding     |
| 4K HEVC            | High-bitrate playback |
| 4K 60 FPS          | Frame synchronization |
| HDR10 HEVC         | HDR pipeline          |
| AV1                | Modern NVDEC support  |
| HDR → SDR          | Tone mapping          |
| Wide-gamut content | Color management      |

---

## 📌 Project Scope

This repository is specifically focused on:

**NVIDIA GPU + MPV + High-quality video playback + Color**

It is not intended to be a universal MPV configuration for every GPU vendor.

The configuration prioritizes NVIDIA hardware and NVIDIA-supported video acceleration.

---

## 🤝 Contributions

Suggestions, improvements, testing results, and bug reports are welcome.

If you discover:

* Playback problems
* GPU compatibility issues
* HDR problems
* Color-management issues
* Frame drops
* Rendering artifacts
* Configuration conflicts

please open an issue with your:

* NVIDIA GPU model
* NVIDIA driver version
* Windows version
* MPV version
* Video codec
* Video resolution
* HDR/SDR status
* Relevant MPV log

---

## 📜 License

This project is licensed under the MIT License.

Copyright © 2026 Pavan Kotian

You are free to use, modify, and redistribute this configuration,
provided that the original copyright notice and license are retained.

This license applies only to the original configuration files,
scripts, shaders, and documentation contained in this repository.

Third-party software, libraries, shaders, scripts, and other included
components remain subject to their respective licenses.
---

## ⭐ Support the Project

If this configuration improves your MPV experience, consider giving the repository a ⭐ Star.

It helps the project reach other NVIDIA users looking for a high-quality portable MPV setup.

---

### NVIDIA • MPV • Vulkan • NVDEC • HDR • Color Management • 4K
