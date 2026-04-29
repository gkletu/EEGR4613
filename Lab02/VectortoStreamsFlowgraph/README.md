# Vector to Streams Flowgraph

## Overview

This GNU Radio flowgraph demonstrates the process of converting between multiple data streams and vectorized data formats. Specifically, it combines two input signals into a vector, then converts that vector back into both a single stream and multiple parallel streams for analysis.

The purpose of this flowgraph is to help visualize and understand how GNU Radio handles data grouping and separation using vector-based blocks.

---

## Flowgraph Structure

### Signal Generation

* Two **Signal Source** blocks generate independent signals.
* These act as the initial input streams to the system.

### Stream to Vector Conversion

* A **Streams to Vector** block combines the two incoming streams into a single vector.
* This groups samples from both signals into one structured data unit.

### Vector Processing Paths

The vector output is split into two paths:

#### Path 1: Vector to Stream

* A **Vector to Stream** block converts the vector back into a single continuous stream.
* This demonstrates how vectorized data can be flattened.

#### Path 2: Vector to Streams

* A **Vector to Streams** block separates the vector back into two independent streams.
* This effectively reconstructs the original parallel signals.

---

## Visualization

Three **QT GUI Time Sink** blocks are used to observe signals:

* **Time Sink 1:** Output of Vector to Stream (combined signal)
* **Time Sink 2:** First output of Vector to Streams
* **Time Sink 3:** Second output of Vector to Streams

These displays allow comparison between:

* Original signals
* Combined vector stream
* Reconstructed individual streams

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Controls how frequently samples are generated and processed
* Signal properties (frequency, amplitude) are defined in each Signal Source block

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Ensure all blocks are properly connected.
3. Click  **Run** .
4. Observe the outputs in the QT GUI Time Sink windows.

---

## Expected Results

* The **Vector to Stream** output shows a combined/interleaved version of both signals.
* The **Vector to Streams** outputs should resemble the original input signals.
* This confirms that vectorization and de-vectorization preserve signal integrity when configured correctly.

---

## Key Takeaways

* GNU Radio can efficiently group multiple streams into vectors for processing.
* Vector-based operations are useful for block-based or batch processing.
* Data can be cleanly reconstructed back into streams without loss.

---

## Notes

* The ordering of inputs into the Streams to Vector block affects how data is reconstructed.
* Mismatched vector sizes or incorrect configuration can lead to distorted outputs.
* This flowgraph is useful for understanding more advanced DSP operations that rely on vectorized data.

---

## AI Usage Disclosure

* This README was generated in part using ChatGPT with contents reviewed and approved by the contributors.

---
