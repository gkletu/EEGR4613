# Embedded Python Block Flowgraph

## Overview

This GNU Radio flowgraph demonstrates the use of an **Embedded Python Block** for custom signal processing within a standard stream-based system. Unlike previous examples that used vectors, tags, or messages, this flowgraph focuses on applying Python logic directly to a continuous data stream.

The purpose of this flowgraph is to highlight how user-defined Python code can be integrated into a typical DSP pipeline to modify or analyze signals in real time.

---

## Flowgraph Structure

### Signal Generation

* A **Signal Source** (or similar input block) generates the input signal.
* This provides a continuous stream of data for processing.

---

### Custom Processing

#### Embedded Python Block

* The signal is passed into an  **Embedded Python Block** .
* This block allows custom Python code to process each incoming sample in real time.

Typical operations may include:

* Scaling or offsetting the signal
* Applying nonlinear transformations
* Implementing simple filters or conditional logic

The processing is performed on a per-sample basis, making it suitable for real-time applications.

---

### Visualization

#### QT GUI Time Sink

* The output of the Python block is displayed using a  **QT GUI Time Sink** .
* This allows direct comparison between expected and actual signal behavior.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Controls how fast samples are processed
* **Python Logic** : Defines how each sample is modified
* **Input Signal Parameters** : Frequency, amplitude, and waveform type

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Double-click the Embedded Python Block to review or edit the code.
3. Verify all connections in the flowgraph.
4. Click  **Run** .
5. Observe the output in the QT GUI Time Sink.

---

## Expected Results

* The output signal will reflect the transformation defined in the Python code.
* Changes to the Python block should immediately alter the waveform.
* The system processes data continuously in real time.

---

## Key Takeaways

* Embedded Python Blocks allow flexible, custom DSP operations.
* Stream-based processing applies transformations sample-by-sample.
* This approach is useful for prototyping and extending GNU Radio functionality.

---

## Notes

* Inefficient Python code may slow down real-time performance.
* Debugging can be done using print statements or simplified logic.
* This flowgraph provides a foundation for more advanced custom processing techniques.

---
