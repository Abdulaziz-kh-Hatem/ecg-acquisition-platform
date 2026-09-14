# ECG Signal Acquisition Hardware

Welcome to the hardware repository for my ECG signal acquisition circuit. I designed this analog front-end (AFE) circuit during my undergraduate studies in Biomedical Engineering at the University of Science and Technology (UST) in Aden, Yemen.

## Project Overview

The goal of this project was to build a low-cost, reliable circuit to capture the electrical activity of the heart (ECG) using standard electronic components. I wanted to see clear QRS complexes on an oscilloscope before sending the data to a microcontroller for processing. 

This hardware circuit was the foundation for my later machine learning project, where I classified PVC arrhythmias on an ESP32.

## Hardware Design

The circuit is built on a breadboard and uses the following main components:
- **Instrumentation Amplifier (AD620):** Used to amplify the very small microvolt signals from the heart while rejecting common-mode noise like 50 Hz powerline interference.
- **Operational Amplifiers (TL072 / LM741):** Used to build active filters.
- **Filters:** I designed a band-pass filter to keep only the useful ECG frequencies and remove baseline wander (low frequencies) and high-frequency noise.

## Hardware Testing and Results

To prove the circuit works, I tested it on myself and used a Hantek digital oscilloscope to view the output. The results were very good. The ECG signal is clear, and you can easily identify the P wave, QRS complex, and T wave.

Here is a picture of the complete hardware setup:

![Hardware Setup](assets/hardware_setup.jpeg)

Here are close-up photos of the oscilloscope screen showing the clean ECG signal:

![Oscilloscope ECG Signal 1](assets/oscilloscope_ecg_1.jpeg)

![Oscilloscope ECG Signal 2](assets/oscilloscope_ecg_2.jpeg)

### Video Demonstration
I also recorded a short video showing the ECG signal updating in real-time on the oscilloscope. You can download and watch it here:
- [Download ECG Hardware Demo Video (12 MB)](assets/ecg_demo.mp4)

## Why This Matters

Building this circuit taught me a lot about practical electronics, signal noise, and real-world biomedical engineering. By getting a clean signal in hardware first, it made the software processing and machine learning steps much easier later on.

## Contact

If you have any questions about the circuit design or want to collaborate, feel free to contact me:
- **Email:** [a.kh.hatem@gmail.com](mailto:a.kh.hatem@gmail.com)
- **LinkedIn:** [Abdulaziz Hatem](https://linkedin.com/in/abdulazizhatem)
