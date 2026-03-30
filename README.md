# ECG Signal Processing using MATLAB Simulink

## 📌 Overview

This project implements an **ECG (Electrocardiogram) Signal Processing System** using MATLAB Simulink. The model simulates an ECG signal, adds noise, filters it, detects heartbeats, and calculates heart rate in BPM (beats per minute).

This project demonstrates fundamental concepts of:

* Signal processing
* Noise filtering
* Peak detection
* Biomedical signal analysis

---

## 🎯 Objectives

* Generate a simulated ECG signal
* Add noise to mimic real-world conditions
* Filter the noisy ECG signal using a bandpass filter
* Detect heartbeats (R-peaks)
* Compute heart rate (BPM)

---

## 🛠️ Tools & Technologies

* MATLAB
* Simulink
* DSP System Toolbox

---

## 🧩 System Architecture

The system consists of the following stages:

1. **Signal Generation**

   * Sine Wave (simulated ECG)
   * Band-Limited White Noise

2. **Signal Mixing**

   * Add block combines ECG + noise

3. **Signal Conditioning**

   * Zero Order Hold (for discrete processing)
   * Bandpass Filter (removes unwanted frequencies)

4. **Signal Processing**

   * Absolute (Abs block)
   * Compare to Constant (thresholding)
   * Detect Rise Positive (heartbeat detection)

5. **Heart Rate Calculation**

   * Counter (Add + Unit Delay)
   * Gain block (conversion to BPM)

---

## 🔄 Block Diagram Flow

```
Signal Generator → Noise → Add → Zero Order Hold → Bandpass Filter
                                                     ↓
                                                    Abs
                                                     ↓
                                           Compare to Constant
                                                     ↓
                                           Detect Rise Positive
                                                     ↓
                                              Counter System
                                                     ↓
                                                  Gain (×6)
                                                     ↓
                                                  Display
```

---

## ⚙️ Key Parameters

| Component        | Parameter | Value      |
| ---------------- | --------- | ---------- |
| Signal Generator | Frequency | 1 Hz       |
| Noise            | Power     | 0.1        |
| Sample Time      |           | 0.001      |
| Bandpass Filter  | Passband  | ~0.5–40 Hz |
| Threshold        | Constant  | 0.6        |
| Gain             |           | 6          |

---

## 📊 Output

The system provides:

* Filtered ECG waveform
* Heartbeat detection pulses
* Heart Rate in BPM (Display block)

Expected result:

* ~60 BPM for a 1 Hz signal

---

## 📸 Results

Include screenshots of:

* Simulink block diagram
* Raw ECG signal
* Noisy ECG signal
* Filtered ECG signal
* Heartbeat detection pulses
* BPM output

---

## 🚀 How to Run

1. Open MATLAB
2. Launch Simulink (`simulink` command)
3. Open the project file (`.slx`)
4. Click **Run**
5. View outputs in Scope and Display blocks

---

## 📈 Applications

* Medical signal analysis
* Heart rate monitoring systems
* Wearable health devices
* Biomedical research

---

## 📚 Learning Outcomes

* Understanding ECG signal characteristics
* Designing digital filters in Simulink
* Implementing peak detection logic
* Working with discrete-time systems

---

## 🤝 Contribution

Feel free to fork this repository and improve the model by:

* Using real ECG datasets
* Improving filtering techniques
* Implementing advanced peak detection algorithms

---

## 📄 License

This project is open-source and free to use for educational purposes.

---

## 💡 Author

**[Amogh Kamath]**

---

⭐ If you found this project helpful, consider giving it a star!
