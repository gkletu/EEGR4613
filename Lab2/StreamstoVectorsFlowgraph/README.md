# Streams to Vectors Flowgraph

## Overview

This GNU Radio flowgraph demonstrates how multiple independent data streams can be combined into a single vectorized data structure. The goal of this exercise is to understand how GNU Radio groups parallel streams into vectors for more efficient or structured processing.

This is a foundational concept used in many DSP applications, including FFT processing and block-based signal operations.

---

## Flowgraph Structure

### Signal Generation

* Two **Signal Source** blocks generate separate input signals.
* These signals act as independent data streams entering the system.

---

### Stream Combination

#### Streams to Vector

* A **Streams to Vector** block combines the two input streams into a single vector.
* Each output item now contains samples from both input streams grouped together.

This block is the core component of the flowgraph and demonstrates how parallel streams can be synchronized into a structured format.

---

### Vector Output Processing

* The vector output is sent to a **QT GUI Time Sink** (or similar visualization block).
* This allows observation of how the grouped data behaves compared to individual streams.

Depending on configuration, the visualization may show:

* Interleaved signal behavior
* Structured grouping of samples across time

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Determines how frequently samples are processed
* **Vector Length** : Defines how many elements are grouped together per output item
* Signal Source settings (frequency, amplitude) define the characteristics of each stream

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Verify all connections between blocks.
3. Click  **Run** .
4. Observe the output in the QT GUI Time Sink.

---

## Expected Results

* The output will reflect a **vectorized combination** of both input signals.
* Instead of two separate waveforms, the data is grouped into a single structured stream.
* This demonstrates how GNU Radio organizes parallel data into vectors for further processing.

---

## Key Takeaways

* Multiple streams can be combined into a single vector using  **Streams to Vector** .
* Vectorization is essential for operations like FFTs and batch processing.
* Proper synchronization of input streams is important for correct vector formation.

---

## Notes

* The order of inputs into the Streams to Vector block determines element placement in the vector.
* Vector size must match the number of input streams (or desired grouping structure).
* This flowgraph pairs naturally with a **Vector to Streams** setup to demonstrate full data conversion cycles.

---
