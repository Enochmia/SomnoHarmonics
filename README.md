# SomnoHarmonics

> **A lightweight, AI-free procedural soundscape engine powered by classical counterpoint and real-time sleep-onset tracking.**  
> **Korean version of [README.md](https://github.com/Enochmia/SomnoHarmonics/blob/main/README_KR.md)**  

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Language](https://img.shields.io/badge/Language-Python%20%7C%20C%2FC%2B%2B-blue.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Cross--Platform-lightgrey.svg)]()

---

## Term Project Proposal

* **Course:** Open Source Software
* **Project Name:** SomnoHarmonics
* **Software License:** MIT License
* **Languages & Environment:** Python, C/C++

---

### 1. Project Overview & Background (Motivation)

In modern society, high-quality sleep is an essential foundation for physical restoration and cognitive performance. However, an increasing number of individuals suffer from delayed sleep onset and degraded sleep quality due to chronic stress and sensory overload. Consequently, research on non-pharmacological sleep quality improvement using auditory stimuli has gained significant momentum.

According to neuroscientific research, auditory stimuli with specific statistical profiles stabilize the sensory threshold of the cerebral cortex, induce brainwave entrainment toward the delta (0.5–4 Hz) and theta (4–8 Hz) frequency bands, and promote entry into slow-wave sleep.

The **SomnoHarmonics** project aims to build a lightweight, open-source soundscape engine capable of generating infinite, calming melodies with cello and keyboard-like textures in real time. Rather than relying on heavy AI/deep learning models, it operates purely on the strict voice-leading rules of classical counterpoint and mathematical stochastic models ($1/f$ flicker noise, Markov chains). Furthermore, it integrates an adaptive sleep-tracking controller that monitors ambient and user acoustics in real time, gradually attenuating playback volume once deep sleep onset is detected.

---

### 2. Core Features & System Architecture

```text
[ Microscopic Audio / Sensors ]
       │ (RMS / Silence Detection)
       ▼
┌───────────────────────────┐      ┌─────────────────────────────┐
│  Smart Sleep Fade-out     │      │   Counterpoint Melody Core  │
│  - Short-Time Energy RMS  │      │   - Fux's Species Rules     │
│  - Adaptive Volume Curve  │      │   - 1/f Stochastic Pitch    │
└─────────────┬─────────────┘      └──────────────┬──────────────┘
              │                                   │
              ▼                                   ▼
┌────────────────────────────────────────────────────────────────┐
│                   Spatial Ambient Mixer                        │
│   - Minimalist Layering (Rain, Wind, Warm Organ Pad)           │
│   - Stereo Panning & Low-Pass Filtering                        │
└───────────────────────────────┬────────────────────────────────┘
                                │
                                ▼
                       [ Audio Output ]
```

#### A. Rule-based Counterpoint Melody Engine
* Translates Johann Joseph Fux’s first- and second-species counterpoint rules into code-level constraints.
* Eliminates abrupt or dissonant melodic leaps, enforcing stepwise motion and natural resolutions to sustain psychoacoustic calm.
* Maps a $1/f$ pink noise distribution to pitch and duration selection probabilities, delivering an evolving yet soothing melody that never feels repetitive or intrusive.

#### B. Spatial Ambient Mixer
* Multi-tracks minimalist ambient soundscapes (rainfall, gentle breeze, warm organ pads).
* Parameterizes the auditory environment through stereo panning and low-pass filter cutoff frequencies, allowing users to tailor their optimal immersive space.

#### C. Smart Sleep Fade-out Engine
* Analyzes the short-time energy (RMS) of local microphone inputs to distinguish steady background noise from user breathing patterns and quiet resting states.
* Once sleep onset is inferred from sustained quietude and lack of interaction, it gently fades out the audio stream over a 10–15 minute window to prevent sleep fragmentation.
* *Future Roadmap:* Extend the module to ingest physiological telemetry (e.g., heart rate and sleep-stage metrics from smartwatches/rings) for enhanced detection accuracy.

---

### 3. Development Schedule & Milestones

To ensure high implementation fidelity and maintain academic quality within tight course timelines, this project adopts a fast-track milestone structure targeting **over 85–90% core functional completion within Weeks 1–2**.

| Week | Period | Key Tasks & Milestones | Cumulative Progress |
| :---: | :---: | :--- | :---: |
| **Week 1** | 11/02 – 11/08 | • Review literature on psychoacoustics and sleep entrainment.<br>• Implement mathematical constraints for counterpoint harmonic rules.<br>• Establish baseline Python MIDI and audio synthesis pipeline. | **50%** |
| **Week 2** | 11/09 – 11/15 | • Integrate procedural melody engine with ambient mixer.<br>• Connect microphone audio energy RMS tracking with auto-fadeout.<br>• Build CLI runtime interface with interactive parameters.<br>• Author comprehensive `README.md` (architecture, demo GIF, references).<br>• Declare MIT License and tag release candidate. | **85%** |
| **Week 3** | 11/16 – 11/22 | • Conduct end-to-end benchmarking and memory-leak verification.<br>• Prepare demonstration scenarios and repository presentation assets. | **95%** |
| **Week 4** | 11/23 – 12/01 | • Edge-case exception handling and final code refactoring. | **100%** |

---

### 4. Technical Distinction & Open Source Value

* **Distinctive Interdisciplinary Scope:** Among historical open-source term projects, combining the formal mathematics of classical music theory with sleep neuroscience is unprecedented, providing clear novelty.
* **Ultra-Lightweight & Dependency-Free Design:** Eliminates heavy neural network runtimes (`PyTorch`, `TensorFlow`), ensuring instantaneous startup, low energy consumption, and viability on resource-constrained embedded systems or single-board computers.
* **Modular Middleware Architecture:** Designed not merely as a standalone utility, but as a reusable open-source library (`import somno_harmonics`) that indie game creators and digital health developers can seamlessly integrate into relaxation apps and interactive soundscapes.
