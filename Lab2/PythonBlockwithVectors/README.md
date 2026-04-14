# Python Block with Vectors Flowgraph

## Overview

This GNU Radio flowgraph demonstrates how to use a custom Embedded Python Block to process vectorized data. It combines multiple input streams into a vector, applies user-defined processing in Python, and then outputs the modified data for visualization.

The purpose of this flowgraph is to show how GNU Radio can be extended with custom logic while working with structured (vector) data formats.

---

## Flowgraph Structure

### Signal Generation

* Multiple **Signal Source** blocks generate input signals.
* These signals serve as independent data streams entering the system.

---

### Stream to Vector Conversion

#### Streams to Vector

* A **Streams to Vector** block groups the input streams into a single vector.
* Each vector contains one sample from each input stream.

---

### Custom Processing

#### Embedded Python Block

* The vectorized data is passed into an  **Embedded Python Block** .
* This block allows user-defined processing using Python code.

Typical operations may include:

* Scaling or modifying values
* Combining elements of the vector
* Applying custom algorithms

The flexibility of this block makes it a powerful tool for implementing non-standard DSP operations.

---

### Output Processing

#### Vector to Stream / Visualization

* The processed vector is either:
  * Converted back into a stream using  **Vector to Stream** , or
  * Sent directly to a visualization block

#### QT GUI Time Sink

* Displays the processed signal in real time.
* Allows comparison between input and modified output.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Determines processing speed
* **Vector Length** : Must match the number of input streams
* **Python Logic** : Defines how the data is manipulated

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Double-click the Embedded Python Block to review or modify the code.
3. Ensure vector sizes and input counts match.
4. Click  **Run** .
5. Observe the output in the QT GUI Time Sink.

---

## Expected Results

* The output signal will reflect the transformation defined in the Python block.
* Changes to the Python code should immediately affect the output behavior.
* If multiple signals are combined, the output may show a composite waveform.

---

## Key Takeaways

* GNU Radio supports custom DSP logic through Embedded Python Blocks.
* Vectorized data allows batch-style processing of multiple signals at once.
* Proper alignment of vector sizes and inputs is critical for correct operation.

---

## Notes

* Errors in the Python block (e.g., mismatched dimensions) may prevent execution.
* Debugging can be done by printing values or simplifying the processing logic.
* This flowgraph is useful for prototyping advanced or custom DSP algorithms.

---
