# Chat Application Flowgraph (Part 1 & Part 2)

## Overview

This GNU Radio project demonstrates a **chat-style communication system** implemented using message passing. The system evolves across two stages:

* **Part 1:** Basic message transmission and processing
* **Part 2:** Enhanced functionality with more advanced message handling and system behavior

The purpose of this project is to illustrate how GNU Radio can be used for asynchronous, event-driven applications beyond traditional signal processing.

---

# Part 1: Basic Chat System

## Structure

### Message Input

* A message-generating block (e.g., Message Strobe or GUI input) creates messages.
* These messages simulate user-generated chat input.

### Message Passing

* Messages are transmitted between blocks using  **message ports** .
* Communication is asynchronous and independent of continuous data streams.

### Processing

#### Embedded Python Block

* Processes incoming messages.
* May perform simple operations such as:
  * Formatting messages
  * Passing messages through unchanged
  * Basic transformations

### Output

#### Message Debug / Display Block

* Displays messages as they are received.
* Acts as the receiver in the chat system.

---

## Expected Results (Part 1)

* Messages are generated and passed successfully between blocks.
* Output displays the transmitted messages.
* The system demonstrates basic message flow within GNU Radio.

---

## Key Takeaways (Part 1)

* GNU Radio supports message-based communication in addition to streams.
* Message passing enables asynchronous system behavior.
* Embedded Python Blocks allow flexible message handling.

---

# Part 2: Enhanced Chat System

## Improvements Over Part 1

Part 2 builds upon the basic system by introducing more advanced message handling and system functionality. Enhancements may include:

* More complex message processing in the Python block
* Conditional logic or message formatting
* Improved structure for message flow
* Additional message routing or interaction

---

## Structure

### Enhanced Processing

#### Embedded Python Block

* Implements more advanced logic compared to Part 1.
* May include:
  * Conditional responses
  * Message filtering
  * Custom formatting or tagging of messages

### Expanded Message Flow

* Additional message connections or processing stages may be included.
* The system becomes more interactive and dynamic.

---

## Expected Results (Part 2)

* Messages are processed with additional logic before being displayed.
* Output reflects transformations or conditions applied in the Python block.
* The system behaves more like a functional communication application.

---

## Key Takeaways (Part 2)

* Message passing systems can be expanded to include complex logic.
* Embedded Python Blocks enable application-level functionality.
* GNU Radio can support interactive systems beyond DSP pipelines.

---

# Overall Comparison

| Feature          | Part 1             | Part 2                       |
| ---------------- | ------------------ | ---------------------------- |
| Message Handling | Basic pass-through | Enhanced processing          |
| Complexity       | Introductory       | Intermediate                 |
| Python Logic     | Minimal            | More advanced                |
| System Behavior  | Static             | More dynamic and interactive |

---

# How to Run

1. Open either `.grc` file in GNU Radio Companion.
2. Inspect message connections (dashed lines).
3. Review the Embedded Python Block for message logic.
4. Click  **Run** .
5. Observe message output in the debug/display block.

---

# Key Takeaways

* GNU Radio supports both **stream processing** and  **message-based systems** .
* Message passing enables asynchronous, event-driven applications.
* Systems can be progressively enhanced by adding logic and structure.

---

# Notes

* Message data is handled using PMT (Polymorphic Types).
* Debug blocks are useful for verifying correct message flow.
* This project demonstrates how GNU Radio can be extended into application-level systems.

---
