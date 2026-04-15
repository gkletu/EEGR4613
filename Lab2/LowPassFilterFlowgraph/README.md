# Low Pass Filter Flowgraph

## Overview

This GNU Radio flowgraph demonstrates the application of a **low-pass filter** to a signal containing multiple frequency components. The filter allows low-frequency components to pass while attenuating higher-frequency content.

The purpose of this flowgraph is to visualize how filtering affects a signal in both the time and frequency domains, and to reinforce the concept of frequency-based signal separation.

---

## Flowgraph Structure

### Signal Generation

#### Composite Signal

* A **Signal Source** (or multiple sources combined) generates a signal containing both low- and high-frequency components.
* This allows clear observation of how the filter selectively removes certain frequencies.

---

### Filtering

#### Low Pass Filter

* A **Low Pass Filter** block processes the input signal.
* The filter removes frequency components above a specified cutoff frequency.

Key characteristics:

* Passband: Frequencies below the cutoff
* Stopband: Frequencies above the cutoff
* Transition region: Area between passband and stopband

---

### Visualization

#### QT GUI Time Sink

* Displays the signal before and/or after filtering.
* Shows how the waveform becomes smoother after high-frequency components are removed.

#### QT GUI Frequency Sink

* Displays the frequency spectrum.
* Clearly shows attenuation of frequencies above the cutoff.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Determines frequency resolution
* **Cutoff Frequency** : Defines which frequencies are preserved
* **Transition Width** : Controls how sharply filtering occurs
* **Gain** : Affects output signal amplitude

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Verify filter parameters (cutoff frequency, transition width).
3. Click  **Run** .
4. Observe both time-domain and frequency-domain outputs.

---

## Expected Results

* High-frequency components will be significantly reduced or removed.
* The time-domain waveform will appear smoother.
* The frequency spectrum will show energy concentrated below the cutoff frequency.

---

## Key Takeaways

* Low-pass filtering is essential for noise reduction and signal conditioning.
* Frequency-domain visualization provides clear insight into filter performance.
* Proper parameter selection is critical for achieving desired filtering behavior.

---

## Notes

* A very low cutoff frequency may remove important parts of the signal.
* A wide transition band results in less sharp filtering.
* This flowgraph is commonly used in communication systems and signal preprocessing.

---

## AI Usage Disclosure

* This README was generated in part using ChatGPT with contents reviewed and approved by the contributors.

---
