# Sample Rate Change Flowgraph

## Overview

This GNU Radio flowgraph demonstrates how to change the **sample rate** of a signal using interpolation and/or decimation. Sample rate conversion is a fundamental operation in digital signal processing, used when interfacing systems with different sampling requirements.

The purpose of this flowgraph is to illustrate how altering the sample rate affects signal representation in both the time and frequency domains.

---

## Flowgraph Structure

### Signal Generation

#### Input Signal

* A **Signal Source** generates a test signal at a given sample rate.
* This signal serves as the baseline for observing changes after rate conversion.

---

### Sample Rate Conversion

#### Interpolation / Decimation Block

* A block such as  **Rational Resampler** ,  **Interpolator** , or **Decimator** is used to modify the sample rate.

Two main operations:

* **Interpolation** : Increases the sample rate by inserting additional samples
* **Decimation** : Decreases the sample rate by removing samples

These operations maintain the signal’s information while changing how it is sampled.

---

### Visualization

#### QT GUI Time Sink

* Displays how the signal waveform changes with different sampling densities.

#### QT GUI Frequency Sink

* Shows how the frequency spectrum is affected by sample rate changes.

---

## Key Parameters

* **Input Sample Rate (`samp_rate`)** : Original sampling frequency
* **Interpolation Factor** : Multiplier for increasing sample rate
* **Decimation Factor** : Divider for reducing sample rate
* **Resulting Sample Rate** : Determined by interpolation/decimation ratio

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Set interpolation and/or decimation factors.
3. Click  **Run** .
4. Observe changes in the time and frequency sinks.

---

## Expected Results

* Increasing the sample rate results in a smoother waveform representation.
* Decreasing the sample rate reduces resolution and may distort the signal.
* The frequency spectrum will adjust according to the new sampling rate.

---

## Key Takeaways

* Sample rate conversion is essential for compatibility between systems.
* Interpolation and decimation allow flexible signal resampling.
* Improper rate changes can introduce aliasing or distortion.

---

## Notes

* Anti-aliasing filtering is often required before decimation.
* Large interpolation factors increase computational cost.
* This concept is widely used in communication systems and audio processing.

---

## AI Usage Disclosure

* This README was generated in part using ChatGPT with contents reviewed and approved by the contributors.

---
