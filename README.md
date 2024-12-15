# Real-Time DSP

This repository provides a sophisticated implementation of a Digital Signal Processor (DSP) leveraging the STM32F4 Discovery Board. The project integrates the onboard MEMS microphone and audio codec for real-time audio capture, processing, and playback. Key functionalities include PDM-to-PCM transformation, audio filtering, and efficient data handling via DMA and I2S.

---

## Key Features

- **Audio Capture**: Uses the onboard MEMS microphone to collect PDM-format audio signals.
- **Audio Playback**: Leverages the integrated audio codec for high-quality sound output.
- **Signal Conversion**: Incorporates middleware for real-time PDM-to-PCM transformation with minimal latency.
- **Real-Time Processing**: Employs I2S and DMA for continuous, low-latency audio handling.
- **Audio Filtering**: Applies digital filters to refine sound quality by mitigating noise and enhancing clarity.

---

## Prerequisites

### Hardware Requirements
- STM32F4 Discovery Board
- USB cable for power and debugging

### Software Requirements
- [STM32CubeMX](https://www.st.com/en/development-tools/stm32cubemx.html) for peripheral configuration
- Keil MDK-ARM
- STM32 HAL Drivers and STM32CubeF4 Middleware for PDM-to-PCM conversion

---

## Installation and Configuration

### Step 1: Clone the Repository
Clone the project files

### Step 2: Import and Configure the Project
1. Open the project in Keil MDK-ARM.
2. Configure the system clock and peripheral settings in `SystemClock_Config` to meet sampling frequency and processing requirements.
3. Verify and adjust DMA, I2S, and GPIO configurations to match your hardware setup.

### Step 3: Build and Deploy
Compile the project and flash the firmware to the STM32F4 Discovery Board using the appropriate debugger interface.

---

## Usage Instructions

1. Connect the STM32F4 Discovery Board to your system via USB.
2. The onboard MEMS microphone captures audio in PDM format, which is converted to PCM using middleware.
3. Processed PCM audio is filtered and transmitted to the audio codec for playback.

---

## Technical Details

### Peripheral Overview
- **I2S Interface**: Configured for duplex communication between the MEMS microphone and audio codec.
- **DMA Controller**: Manages high-efficiency data transfers with minimal CPU intervention.

### Audio Processing Pipeline
- **PDM-to-PCM Conversion**: Transforms raw PDM input into PCM samples using STM32Cube middleware.
- **Digital Filtering**: Implements configurable filters to improve signal clarity and reduce noise artifacts.


---

## Contributing

Contributions are welcomed to enhance functionality or improve documentation. Please fork the repository, make modifications, and submit a pull request with a detailed description of your changes.

---

## License

This project is licensed under the MIT License. For more details, refer to the [LICENSE](LICENSE) file included in this repository.

---
[Helpful Resources](https://github.com/Hasnaoui-Youssef/STM32_DSP_Project_Resources)
