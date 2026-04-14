# Sine Wave Generation Flowgraph

## Overview

This GNU Radio flowgraph demonstrates how to generate and visualize a basic sine wave signal. It serves as an introduction to signal generation, parameter control, and real-time visualization within GNU Radio.

This type of flowgraph is fundamental in understanding how continuous signals are represented and processed in digital signal processing systems.

---

## Flowgraph Structure

### Signal Generation

#### Signal Source

* A **Signal Source** block generates a sine wave.
* This is the core component of the flowgraph.

The signal is defined by adjustable parameters such as frequency, amplitude, and sample rate.

---

### Throttling

#### Throttle Block

* A **Throttle** block is used to control the flow of samples.
* This prevents the system from consuming excessive CPU resources when no hardware (like an SDR) is present.

---

### Visualization

#### QT GUI Time Sink

* The output of the signal is displayed using a  **QT GUI Time Sink** .
* This allows real-time observation of the waveform in the time domain.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Determines how many samples are generated per second
* **Frequency** : Controls how fast the sine wave oscillates
* **Amplitude** : Sets the height (strength) of the signal

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Verify parameter values (sample rate, frequency, amplitude).
3. Click  **Run** .
4. Observe the sine wave in the QT GUI Time Sink window.

---

## Expected Results

* A smooth sinusoidal waveform should appear in the time sink.
* Increasing frequency results in more cycles within the same time window.
* Increasing amplitude increases the vertical size of the waveform.

---

## Key Takeaways

* GNU Radio can generate basic signals using built-in source blocks.
* The **Throttle** block is important when no hardware timing source is present.
* Visualization tools like QT GUI sinks are essential for analyzing signals.

---

## Notes

* If the waveform appears distorted, check the sample rate relative to the signal frequency.
* Extremely high frequencies compared to the sample rate may cause aliasing effects.
* This flowgraph serves as a building block for more advanced DSP systems.

---
