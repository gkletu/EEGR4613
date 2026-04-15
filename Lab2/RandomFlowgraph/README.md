# Random Signal Flowgraph

## Overview

This GNU Radio flowgraph demonstrates the generation and visualization of a random signal. Unlike deterministic signals (such as sine waves), random signals vary unpredictably and are commonly used in simulations, noise modeling, and testing communication systems.

The purpose of this flowgraph is to illustrate how GNU Radio can generate stochastic data and how it appears in the time domain.

---

## Flowgraph Structure

### Signal Generation

#### Random Source

* A **Random Source** block generates a stream of random values.
* These values may follow a uniform or specified distribution depending on configuration.

This block serves as the primary signal source for the flowgraph.

---

### Throttling

#### Throttle Block

* A **Throttle** block regulates the sample flow rate.
* This ensures the system runs at a manageable speed when no external hardware clock is present.

---

### Visualization

#### QT GUI Time Sink

* The signal is displayed using a  **QT GUI Time Sink** .
* This allows real-time observation of how the random signal fluctuates over time.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Controls how quickly random samples are generated
* **Amplitude Range** : Defines the possible values of the random output
* **Data Type** : Determines whether the output is integer, float, etc.

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Check the Random Source configuration.
3. Click  **Run** .
4. Observe the output in the QT GUI Time Sink window.

---

## Expected Results

* The displayed waveform will appear irregular and non-repeating.
* There will be no predictable pattern, unlike periodic signals.
* The amplitude will fluctuate within the configured range.

---

## Key Takeaways

* Random signals are useful for modeling noise and testing systems.
* GNU Radio provides built-in blocks for generating stochastic data.
* Visualization helps distinguish between deterministic and random signals.

---

## Notes

* Different random distributions (if configured) will change the statistical behavior of the signal.
* Increasing the sample rate results in faster fluctuations in the display.
* This flowgraph is useful for understanding noise in real-world communication systems.

---

## AI Usage Disclosure

* This README was generated in part using ChatGPT with contents reviewed and approved by the contributors.

---
