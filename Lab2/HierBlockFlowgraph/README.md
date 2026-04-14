# Hierarchical Block Flowgraph

## Overview

This GNU Radio flowgraph demonstrates the use of a  **Hierarchical Block** , which allows multiple blocks to be grouped together into a single reusable module. Hierarchical blocks help simplify complex flowgraphs and promote modular design.

The purpose of this flowgraph is to show how smaller DSP components can be encapsulated into a higher-level block, making systems easier to manage, reuse, and scale.

---

## Flowgraph Structure

### Hierarchical Block

#### Custom Hierarchical Block

* A **Hierarchical Block** is created by grouping multiple internal blocks into a single unit.
* This block has defined  **input and output ports** , just like any standard GNU Radio block.

Inside the hierarchical block, typical operations may include:

* Signal generation or transformation
* Filtering or scaling
* Data conversion

The internal complexity is hidden from the main flowgraph.

---

### Top-Level Flowgraph

* The hierarchical block is used as a standard block within the main flowgraph.
* It connects to other components such as:
  * Signal sources
  * Processing blocks
  * Visualization sinks

This demonstrates how complex systems can be built using modular components.

---

### Visualization

#### QT GUI Time Sink

* The output of the hierarchical block is displayed using a  **QT GUI Time Sink** .
* This allows observation of the processed signal without needing to inspect internal details.

---

## Key Parameters

* **Input/Output Ports** : Define how data enters and exits the hierarchical block
* **Internal Parameters** : Configured within the hierarchical block itself
* **Sample Rate (`samp_rate`)** : Must remain consistent across internal and external blocks

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Open the hierarchical block to inspect its internal structure (optional).
3. Verify connections in the top-level flowgraph.
4. Click  **Run** .
5. Observe the output in the QT GUI Time Sink.

---

## Expected Results

* The output reflects the combined operations of all blocks inside the hierarchical block.
* Changes made inside the hierarchical block will directly affect the output signal.
* The top-level flowgraph remains clean and simplified.

---

## Key Takeaways

* Hierarchical blocks enable modular and reusable design in GNU Radio.
* Complex systems can be simplified by encapsulating functionality.
* This approach improves readability and scalability of flowgraphs.

---

## Notes

* Changes inside a hierarchical block require saving and updating the parent flowgraph.
* All internal connections must be correctly mapped to external ports.
* This technique is commonly used in large SDR systems and production-level designs.

---
