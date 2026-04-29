# Python Block with Stream Tags Flowgraph

## Overview

This GNU Radio flowgraph demonstrates how to use stream tags in combination with an Embedded Python Block. Stream tags are metadata attached to specific samples in a data stream, allowing additional information to be passed alongside the signal.

The purpose of this flowgraph is to illustrate how tagged data can be accessed and processed within a custom Python block, enabling more advanced and context-aware signal processing.

---

## Flowgraph Structure

### Signal Generation

* A **Signal Source** (or similar input block) generates the primary signal.
* This signal forms the base data stream to which tags may be applied.

---

### Stream Tagging

#### Tag Generation / Tag Injection

* Tags are inserted into the data stream using a tag-generating block or configuration.
* Each tag typically includes:
  * **Key** (identifier)
  * **Value** (associated data)
  * **Offset** (position in the stream)

These tags travel alongside the signal through the flowgraph.

---

### Custom Processing

#### Embedded Python Block

* The tagged stream is passed into an  **Embedded Python Block** .
* Inside this block, both the signal data and associated tags can be accessed.

Typical operations include:

* Reading tag values at specific sample indices
* Modifying signal behavior based on tag information
* Generating new tags or altering existing ones

This allows for dynamic, metadata-driven processing.

---

### Visualization

#### QT GUI Time Sink

* Displays the processed signal in real time.
* While tags are not directly visible in the time sink, their effects on the signal may be observed.

---

## Key Parameters

* **Sample Rate (`samp_rate`)** : Controls processing speed
* **Tag Key/Value** : Defines the meaning and data stored in each tag
* **Tag Offset** : Specifies where in the stream the tag is applied
* **Python Logic** : Determines how tags influence signal processing

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Inspect how tags are created or inserted in the flowgraph.
3. Open the Embedded Python Block to review how tags are handled.
4. Click  **Run** .
5. Observe the signal behavior in the QT GUI Time Sink.

---

## Expected Results

* The signal will behave differently depending on the presence and values of tags.
* Specific events (e.g., amplitude changes, gating, or annotations) may occur at tagged positions.
* The Python block should successfully read and respond to tag data.

---

## Key Takeaways

* Stream tags provide a way to attach metadata to signal samples.
* Embedded Python Blocks can access and act on this metadata.
* Tags enable more intelligent and event-driven DSP systems.

---

## Notes

* Tags must be correctly formatted (key, value, offset) to be recognized.
* Misaligned offsets can cause tags to appear at unintended positions.
* Debugging tag behavior may require printing tag information inside the Python block.

---

## AI Usage Disclosure

* This README was generated in part using ChatGPT with contents reviewed and approved by the contributors.

---
