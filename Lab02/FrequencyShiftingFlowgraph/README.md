# Frequency Shifting Flowgraph

## Overview

This GNU Radio flowgraph demonstrates **frequency shifting** (also known as frequency translation), where a signal is shifted in frequency by mixing it with another signal. This is a fundamental operation in communication systems, used in modulation, demodulation, and tuning.

The purpose of this flowgraph is to show how multiplying a signal by a sinusoid changes its frequency content.

---

## Flowgraph Structure

### Signal Generation

#### Input Signal

* A **Signal Source** generates the original signal at a given frequency.
* This represents the baseband or initial signal.

#### Local Oscillator (LO)

* A second **Signal Source** acts as a local oscillator.
* This signal determines how much the input signal will be shifted in frequency.

---

### Frequency Translation

#### Multiply Block

* A **Multiply** block combines the input signal and the local oscillator.
* This operation results in frequency components that are shifted.

Mathematically, multiplying two sinusoids produces:

* A sum frequency component
* A difference frequency component

---

### Visualization

#### QT GUI Frequency Sink

* Displays the frequency spectrum of the signal.
* Allows clear observation of the frequency shift.

#### QT GUI Time Sink (optional)

* Shows how the waveform changes in the time domain.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Determines frequency resolution
* **Input Signal Frequency** : Original signal frequency
* **LO Frequency** : Amount of frequency shift applied
* **Amplitude** : Affects signal strength

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Set the input signal and LO frequencies.
3. Click  **Run** .
4. Observe the output in the frequency sink.

---

## Expected Results

* The original signal frequency will be shifted by the LO frequency.
* Two new frequency components will appear:
  * One at the sum of the frequencies
  * One at the difference of the frequencies
* The frequency sink will clearly show this shift.

---

## Key Takeaways

* Frequency shifting is achieved through signal multiplication.
* This operation is essential in modulation and receiver design.
* The frequency domain provides the clearest view of this effect.

---

## Notes

* If only one shifted component is desired, filtering may be required to remove the մյուս component.
* Incorrect parameter selection may cause aliasing if frequencies exceed the Nyquist limit.
* This concept is widely used in RF systems and SDR applications.

---

## AI Usage Disclosure

* This README was generated in part using ChatGPT with contents reviewed and approved by the contributors.

---
