# Python Block with Message Passing Flowgraph

## Overview

This GNU Radio flowgraph demonstrates how message passing works in conjunction with an Embedded Python Block. Unlike traditional stream-based processing, message passing allows discrete data (messages) to be sent asynchronously between blocks.

The purpose of this flowgraph is to illustrate how GNU Radio handles non-stream data communication and how custom Python logic can send, receive, and process messages.

---

## Flowgraph Structure

### Signal / Message Source

* A **message-generating block** (such as a Message Strobe or similar) produces discrete messages.
* These messages are not part of a continuous sample stream but are instead sent as independent data packets.

---

### Message Passing System

#### Message Connections

* Blocks are connected using **message ports** instead of stream connections.
* Messages are passed asynchronously between blocks.

This allows for event-driven processing rather than continuous signal flow.

---

### Custom Processing

#### Embedded Python Block

* The **Embedded Python Block** receives messages through its input message port.
* Inside the block, Python code processes incoming messages.

Typical operations include:

* Parsing message contents
* Triggering actions based on message values
* Generating and sending new messages

The block may also output messages to other blocks.

---

### Output / Visualization

* Messages may be printed, logged, or converted into signals for visualization.
* Some implementations may use debug blocks to display message contents.

---

## Key Parameters

* **Message Type** : Defines the structure of the message (e.g., PMT format)
* **Message Rate** : Controls how frequently messages are generated
* **Python Logic** : Determines how messages are processed and responded to

---

## How to Run

1. Open the `.grc` file in GNU Radio Companion.
2. Inspect the message connections (dashed lines between blocks).
3. Open the Embedded Python Block to review message handling code.
4. Click  **Run** .
5. Observe message activity through debug output or connected blocks.

---

## Expected Results

* Messages will be generated and passed between blocks asynchronously.
* The Embedded Python Block will process incoming messages and may produce new ones.
* Output behavior depends on the implemented Python logic.

---

## Key Takeaways

* GNU Radio supports both stream processing and message-based communication.
* Message passing is useful for control signals, events, and metadata exchange.
* Embedded Python Blocks provide flexibility for handling custom message logic.

---

## Notes

* Message passing uses PMT (Polymorphic Types), which may require specific handling in Python.
* Debugging is often done using message debug blocks or print statements.
* This approach is commonly used in more complex SDR systems for control and coordination tasks.

---

## AI Usage Disclosure

* This README was generated in part using ChatGPT with contents reviewed and approved by the contributors.

---

