# Signal Transmission Simulator 📡

A comprehensive interactive simulator for encoding and modulation techniques, developed to visualize concepts from **Data and Computer Communications**. This tool allows users to generate signals, apply various transmission schemes, and analyze the results through waveforms, step-by-step execution tables, and theoretical explanations.

## 🌐 Live Demo

🚀 **The app is now live!**  
You can try the simulator directly in your browser here:

👉 **[Signal Transmission Simulator – Live App](https://signal-transmission-simulator.streamlit.app)**

> 💡 **For the best experience:** resize your browser page to **80% zoom**.  
> The layout and plots are optimized for this scale.

## 🎓 Academic Context

This simulator was developed as a course assignment for:

- **[Principles of Computer Communications (BLG 337E)](https://ninova.itu.edu.tr/en/public.dersler.ders.aspx?dil=en&kategori=faculty-of-computer-and-informatics&dersId=5507)**
- Computer Engineering Faculty — [Istanbul Technical University](https://itu.edu.tr/en/homepage)

> **Reference Material:** > All algorithms in this simulator follow the definitions and conventions provided in:  
> **[Data and Computer Communications (10th ed.)](http://williamstallings.com/DataComm/)** by William Stallings.

## ✨ Features

The application supports four major modes of transmission simulation:

### 1. Digital → Digital (Line Coding)

Converts a digital bitstream into digital signal voltage levels.

- **Basic Schemes:** NRZ-L, NRZI, Bipolar-AMI, Pseudoternary, Manchester, Differential Manchester.
- **Scrambling Techniques:** B8ZS, HDB3 (used to fix synchronization issues in AMI).
- **Comparison Mode:** Visual comparison of the same bit sequence across multiple line coding schemes.

### 2. Digital → Analog (Modulation)

Modulates a digital bitstream onto an analog carrier signal.

- **Amplitude:** ASK (Amplitude Shift Keying).
- **Frequency:** BFSK (Binary FSK), MFSK (Multiple FSK).
- **Phase:** BPSK (Binary PSK), DPSK (Differential PSK), QPSK (Quadrature PSK).
- **Quadrature:** QAM (Quadrature Amplitude Modulation) including 4-QAM and 16-QAM configurations.
- **Constellations:** Visualizes 16-QAM and QPSK constellation diagrams.

### 3. Analog → Digital (Digitization)

Converts continuous analog waveforms (Sine, Triangle, Square) into digital data.

- **PCM (Pulse Code Modulation):** Includes sampling (PAM), quantization, and encoding. Visualizes the quantization error and staircase function.
- **DM (Delta Modulation):** Visualizes the "staircase" approximation and slope overload/granular noise effects.
- **Line Coding Integration:** The resulting digital data is automatically line-coded for transmission simulation.

### 4. Analog → Analog (Modulation)

Modulates an analog message signal onto a higher-frequency carrier.

- **Techniques:** AM (Amplitude Modulation), FM (Frequency Modulation), PM (Phase Modulation).
- **Visualizations:** Message signal, modulated carrier, spectrum (FFT) intuition, and ideal demodulated signal overlay.
- **Theory:** Interactive display of modulation indices ($n_a$, $\beta$, etc.) and bandwidth estimations (Carson's Rule).

## 🚀 Installation & Usage

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/itu-itis23-mahmoud21/signal-transmission-simulator.git](https://github.com/itu-itis23-mahmoud21/signal-transmission-simulator.git)
    cd signal-transmission-simulator
    ```

2.  **Install dependencies:**
    It is recommended to use a virtual environment.

    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the application:**

    ```bash
    streamlit run comm_sim/app.py
    ```

4.  **Explore:**
    Open your browser to the URL provided (usually `http://localhost:8501`). Use the sidebar to select a mode, configure parameters (frequency, amplitude, bit-rate), and click **"Run simulation"**.

## 📂 Project Structure

```text
├── comm_sim/               # Main Application Source Code
│   ├── GPT_optimized/      # GPT-refactored module variants
│   ├── gemini_optimized/   # Gemini-refactored module variants
│   ├── tests/              # Unit tests for transmission modules
│   ├── app.py              # Main Streamlit Dashboard entry point
│   ├── a2a.py              # Analog-to-Analog (AM/FM/PM) Logic
│   ├── a2d.py              # Analog-to-Digital (PCM/Delta) Logic
│   ├── d2a.py              # Digital-to-Analog (ASK/FSK/PSK) Logic
│   ├── d2d.py              # Digital-to-Digital (Line Coding) Logic
│   └── utils.py            # Signal processing & plotting utilities
├── .devcontainer/          # Development container configuration
├── Report.pdf              # Project Report
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

## 👥 Authors

Created by:

- [**Mohamed Ahmed Abdelsattar Mahmoud**](https://github.com/itu-itis23-mahmoud21)
- [**Racha Baddredine**](https://github.com/racha-badreddine)

---

_Developed at Istanbul Technical University, 2025._
