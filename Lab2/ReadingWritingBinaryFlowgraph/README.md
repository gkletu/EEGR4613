# File Source and Binary Storage Flowgraph (Part 1 & Part 2)

## Overview

This GNU Radio project demonstrates how data can be read from and written to files, focusing on handling  **binary data streams** . The system is developed in two stages:

* **Part 1:** Reading data from a file using a File Source
* **Part 2:** Storing and managing binary data using file sinks and processing blocks

The purpose of this project is to illustrate how GNU Radio interacts with external data sources and how signal data can be preserved for later use.

---

# Part 1: File Source (Reading Data)

## Structure

### File Input

#### File Source Block

* A **File Source** block reads pre-existing data from a file.
* The data is treated as a continuous stream of samples.

This allows GNU Radio to process stored signals as if they were being generated in real time.

---

### Signal Processing / Visualization

#### Processing Blocks (if included)

* Additional blocks may manipulate or pass through the data.

#### QT GUI Time Sink / Frequency Sink

* Displays the signal read from the file.
* Allows visualization of stored data behavior.

---

## Expected Results (Part 1)

* Data from the file is successfully read and displayed.
* The signal behaves consistently with how it was originally stored.
* The system demonstrates offline signal playback.

---

## Key Takeaways (Part 1)

* GNU Radio can read signal data from external files.
* Stored data can be reused for analysis and testing.
* File sources enable repeatable experiments without live signal generation.

---

# Part 2: Storing Binary Data

## Structure

### Signal Generation / Input

* A signal (from a source or processed stream) is used as input.

---

### Data Storage

#### File Sink Block

* A **File Sink** block writes data to a binary file.
* The output is stored as raw sample data.

This allows signals to be saved for later playback or analysis.

---

### Optional Processing

* Data may be modified before being stored.
* Ensures that stored signals reflect processed results.

---

## Expected Results (Part 2)

* Signal data is successfully written to a binary file.
* The stored file can be reused in a File Source (Part 1).
* Data integrity is maintained between storage and playback.

---

## Key Takeaways (Part 2)

* GNU Radio can store signal data for offline use.
* Binary files provide an efficient format for saving raw samples.
* File-based workflows are essential for testing and debugging DSP systems.

---

# Overall System Workflow

Together, Part 1 and Part 2 form a complete data pipeline:

1. Generate or process a signal
2. Store it using a File Sink
3. Reload it later using a File Source
4. Analyze or visualize the data

This demonstrates a full  **data acquisition and playback cycle** .

---

# Comparison of Parts

| Feature   | Part 1 (File Source) | Part 2 (File Sink)  |
| --------- | -------------------- | ------------------- |
| Function  | Reads data from file | Writes data to file |
| Role      | Playback / analysis  | Storage / recording |
| Data Flow | File → GNU Radio    | GNU Radio → File   |
| Use Case  | Reusing signals      | Saving signals      |

---

# How to Run

### Part 1

1. Open `fileSource.grc`
2. Ensure the file path is correct
3. Click **Run**
4. Observe signal output

### Part 2

1. Open `storingBinaryFiles.grc`
2. Set output file path
3. Click **Run**
4. Verify file is created

---

# Key Takeaways

* GNU Radio supports both **data acquisition** and  **data playback** .
* File-based processing is critical for repeatable experiments.
* Combining File Source and File Sink enables full control over signal data.

---

# Notes

* File paths must be correct for successful operation.
* Data type (e.g., float, complex) must match between source and sink.
* Incorrect formatting may result in corrupted or unreadable data.

---
