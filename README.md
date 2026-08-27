> # MiniAudioDSP Lab 🎧
>
> 博客链接：:link: https://kono3bpencil4301.github.io/kono3bpencil4301AudioLab.github.io 

一个基于 C++ 的数字音频处理与合成器开发实验项目。

本项目尝试不依赖高级音频框架，从底层理解计算机如何存储、处理并生成声音，通过实现数字合成器的核心模块，探索：

- C++ 工程开发
- 数字信号处理（DSP）
- 音频工程
- 电子音乐制作
- 声音设计


---

# 📖 Project Introduction

声音是物理世界中的连续信号，而计算机只能处理离散的数据。

那么：

> 空气中的振动，究竟如何转换为计算机中的数字？

> 一个合成器，又是如何通过数学模型创造声音？

MiniAudioDSP Lab 希望通过 C++ 从零构建一个数字合成器系统，逐步探索声音从物理振动，模拟信号，数字采样，DSP算法到声音输出的完整过程。

本项目尝试从底层实现：

- PCM 数据处理

- WAV 文件生成
- 数字振荡器-
- 音频滤波器 
- 合成算法
-  MIDI 控制 
- 实时音频处理

# 🎯Project Motivation

作为一个电子音乐爱好者，我长期关注：

- 合成器（Synthesizer）
- 音色设计（Sound Design）
- 数字音频技术（Digital Audio）


在学习编程过程中，我逐渐发现：

很多软件开发停留在应用层，而音频工程连接了：

- 数学
- 信号处理
- 编程语言
- 硬件接口
- 艺术创作

因此，我希望通过 C++ 从底层重新理解声音。让这个项目不仅仅是制作一个合成器，而是希望建立一个**从数学模型到声音创造之间的完整技术链路。**

# 🧠 Core Concept


一个数字合成器本质上是：

数学模型→ 数字信号→ DSP算法→声音输出

例如：正弦函数的表达式为

$$
x(t)=A\sin(2\pi ft)
$$

可以成为：

数字振荡器（Digital Oscillator）


傅里叶分析：

可以解释：

> 为什么复杂声音可以由多个简单波形组成。


滤波器：

可以改变：

> 声音中的频率结构。


因此，电子音乐中的音色，本质上也是数字信号处理的结果。


---

# 🚀 Development Roadmap

## Phase 1：Digital Audio Foundation

状态：

✅ Completed


目标：

理解计算机如何存储声音。


内容：

- PCM（Pulse Code Modulation）
- Sample Rate
- Bit Depth
- Channel Layout
- Audio Frame
- WAV / RIFF Format
- Little Endian


成果：

- 手写 WAV 文件生成器
- C++ PCM 数据写入


文章：

- 《让 C++ 发出第一声：从 PCM 样本到手写 WAV 文件》


---

## Phase 2：Digital Oscillator

状态：

🚧 Developing


目标：

实现最基础的声音发生器。


内容：

- Sine Oscillator
- Square Oscillator
- Saw Oscillator
- Triangle Oscillator
- Phase Accumulator
- Anti-Aliasing


核心：

通过数学函数生成数字波形。


示例：


Frequency

↓

Phase

↓

Waveform

↓

PCM Sample



---

## Phase 3：Additive Synthesis

状态：

📌 Planned


目标：

理解声音频谱结构。


内容：

- Fourier Series
- Harmonics
- Partial
- FFT
- Spectrum Analysis


核心思想：

复杂声音可以表示为：


Fundamental Frequency

Harmonics

Amplitude Relationship



最终实现：

- 多振荡器叠加
- 基于频谱的音色生成


---

## Phase 4：Subtractive Synthesis

状态：

📌 Planned


目标：

实现经典模拟合成器工作流程。


内容：

- Low Pass Filter
- High Pass Filter
- Band Pass Filter
- Resonance
- Envelope Generator


模拟：

经典 Analog Synth：


Oscillator

↓

Filter

↓

Amplifier

↓

Output



---

## Phase 5：FM / PM Synthesis

状态：

📌 Planned


目标：

探索现代数字合成技术。


内容：

- Frequency Modulation
- Phase Modulation
- Carrier Wave
- Modulator Wave
- Yamaha DX7 Algorithm


研究：

如何通过波形之间的调制创造复杂音色。


---

## Phase 6：MIDI System

状态：

📌 Planned


目标：

让合成器从实验程序变成可演奏乐器。


内容：

- MIDI Message
- Note Event
- Velocity
- Pitch Bend
- Controller


实现：


Keyboard

↓

MIDI Event

↓

Synth Engine

↓

Audio Output



---

## Phase 7：Realtime Audio Engine

状态：

📌 Planned


目标：

实现实时声音生成。


内容：

- Audio Callback
- Buffer
- Latency
- Threading
- Audio Driver
- Real-time Processing


最终目标：

实现实时演奏。


---

# 🛠️ Technology Stack


## Programming Language

- C++17


## Build System

- CMake


## Audio Technology

- PCM
- WAV / RIFF
- MIDI
- DSP Algorithm


## Mathematics

- Fourier Transform
- Signal Processing
- Linear Algebra
- Numerical Computing


## Development Tools

- Git
- Audacity
- Python (Audio Analysis)


---

# 📂 Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── Gmeek.yml                 # Gmeek 博客构建与 GitHub Pages 部署工作流
├── backup/
│   └── 让 C++ 发出第一声：从 PCM 样本到手写 WAV 文件.md
│                                      # 博客文章的 Markdown 备份
├── docs/                              # Gmeek 生成的静态博客与 GitHub Pages 发布内容
│   ├── post/                          # 文章 HTML 页面
│   ├── index.html                     # 博客首页
│   ├── postList.json                  # 文章列表数据
│   ├── rss.xml                        # RSS 订阅源
│   └── tag.html                       # 标签页面
├── mini_audio_lab_src/                # MiniAudioDSP Lab 实验源码与学习笔记
│   └── Lesson_01/
│       ├── note/
│       │   └── 让 C++ 发出第一声：从 PCM 样本到手写 WAV 文件.md
│       ├── wav_and_pcm.cpp            # PCM 正弦波生成与 WAV 文件写入实现
│       └── wav_and_pcm.h              # WAV 数据结构与相关接口声明
├── blogBase.json                      # Gmeek 生成的博客数据
├── config.json                        # Gmeek 博客配置
└── README.md                          # 项目说明文档
```

---

# 📚 Technical Articles


## Audio DSP Series


### 01. 让 C++ 发出第一声

从 PCM 样本到手写 WAV 文件

内容：

- 数字音频基础
- PCM
- WAV格式
- 二进制文件写入
- 正弦波生成


---

### 02. 从傅里叶到加法合成

声音为什么可以被拆解


内容：

- Fourier Transform
- Harmonics
- Spectrum


---

### 03. 数字振荡器

如何使用数学创造声音


内容：

- Phase Accumulator
- Waveform Generation
- Oscillator Design


---

### 04. ADSR Envelope

让声音拥有生命


内容：

- Attack
- Decay
- Sustain
- Release


---

### 05. Digital Filter

塑造声音的频率结构


内容：

- Filter Design
- EQ
- Resonance


---

# 📊 Current Progress


## Completed

✅ WAV Writer

✅ PCM Generator

✅ Sine Wave Oscillator

✅ Basic Audio Data Processing


## Developing

🚧 Multiple Oscillator System

🚧 Additive Synth Engine

🚧 DSP Module Architecture


## Future

📌 Real-time Synthesizer

📌 MIDI Controller Support

📌 Complete Software Synthesizer


---

# 🌌 Long-Term Vision


未来三年，希望逐步完成一个完整的 C++ 数字合成器框架。


最终目标：

不是简单复刻商业合成器，而是通过工程实践深入理解：

- 数字信号处理
- 音频软件架构
- 声音生成机制


希望通过这个项目建立：


Mathematics

↓

Signal Processing

↓

Programming

↓

Electronic Music


之间的连接。


---

# License

MIT License
