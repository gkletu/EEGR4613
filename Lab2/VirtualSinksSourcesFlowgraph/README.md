# Virtual Sources and Sinks Flowgraph

## Overview

This GNU Radio flowgraph demonstrates the use of  **Virtual Sources and Virtual Sinks** , which allow signals to be passed between different parts of a flowgraph without direct physical connections (wires). These blocks help simplify complex designs by reducing visual clutter and improving organization.

The purpose of this flowgraph is to show how signals can be logically routed across a system while maintaining clarity and modularity.

---

## Flowgraph Structure

### Signal Generation

#### Signal Source

* A **Signal Source** generates the input signal.
* This signal serves as the initial data stream.

---

### Virtual Routing

#### Virtual Sink

* A **Virtual Sink** block receives the signal from the source.
* It acts as a labeled endpoint for the signal.

#### Virtual Source

* A **Virtual Source** block retrieves the signal using the same identifier.
* This allows the signal to reappear elsewhere in the flowgraph without a direct connection.

---

### Signal Distribution

* The virtual source can feed multiple blocks simultaneously.
* This enables flexible signal routing and reuse.

---

### Visualization

#### QT GUI Time Sink

* Displays the signal after it has been routed through virtual connections.
* Confirms that signal integrity is preserved.

---

## Key Parameters

* **Stream ID / Name** : Must match between Virtual Sink and Virtual Source
* **Sample Rate (`samp_rate`)** : Must remain consistent throughout the flowgraph

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Ensure that Virtual Sink and Virtual Source names match.
3. Click  **Run** .
4. Observe the signal in the QT GUI Time Sink.

---

## Expected Results

* The signal will appear unchanged after passing through virtual connections.
* The system will behave as if the blocks were directly connected.
* The flowgraph layout will remain clean and organized.

---

## Key Takeaways

* Virtual Sources and Sinks improve readability in complex flowgraphs.
* They allow signals to be reused without additional wiring.
* This technique supports modular and scalable system design.

---

## Notes

* Mismatched stream IDs will prevent signal transfer.
* Virtual connections do not alter the signal itself.
* This approach is especially useful in large SDR systems with many interconnected components.

---
