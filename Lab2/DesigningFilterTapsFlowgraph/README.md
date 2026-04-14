# Low Pass Filter Taps Flowgraph

## Overview

This GNU Radio flowgraph demonstrates the design and application of a **low-pass filter** using filter taps. A low-pass filter allows low-frequency components of a signal to pass through while attenuating higher-frequency components.

The purpose of this flowgraph is to show how filter taps define the behavior of a filter and how they affect the output signal in the time domain.

---

## Flowgraph Structure

### Signal Generation

* A **Signal Source** generates an input signal, typically containing multiple frequency components.
* This allows observation of how different frequencies are affected by the filter.

---

### Filter Design

#### Low Pass Filter (FIR Filter)

* A **Low Pass Filter** block is used to process the signal.
* The filter is defined by a set of **taps** (coefficients), which determine how the input signal is modified.

Key aspects of the filter:

* Passband: Frequencies that are preserved
* Stopband: Frequencies that are attenuated
* Transition band: Region between passband and stopband

---

### Visualization

#### QT GUI Time Sink

* Displays the filtered signal in the time domain.
* Allows comparison between input and output behavior.

#### (Optional) Frequency Sink

* If included, shows how high-frequency components are removed after filtering.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Determines signal resolution
* **Cutoff Frequency** : Defines the boundary between passed and attenuated frequencies
* **Transition Width** : Controls how sharply the filter transitions
* **Filter Taps** : Coefficients that implement the filter response

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Review the low-pass filter parameters (cutoff frequency, transition width).
3. Click  **Run** .
4. Observe the output in the QT GUI Time Sink (and Frequency Sink if available).

---

## Expected Results

* High-frequency components of the input signal will be reduced or removed.
* The output signal will appear smoother compared to the input.
* In the frequency domain, only frequencies below the cutoff will remain prominent.

---

## Key Takeaways

* Filter taps define the behavior of FIR filters in GNU Radio.
* Low-pass filters are essential for noise reduction and signal conditioning.
* Proper selection of cutoff frequency and transition width is critical for desired performance.

---

## Notes

* A very sharp transition requires more taps, increasing computational cost.
* Poor parameter selection may result in signal distortion or insufficient filtering.
* This flowgraph is foundational for more advanced filtering and communication systems.

---
