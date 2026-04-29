## Project Overview
This file uses osmoSDR with the Hack RF One software defined radio to provide real-time visualizaation of the RF spectrum and time-domain signals. Specifically, it is tuned for the 299.917 MHz transmission signal of a garage door opener allowing the user to capture and display the spectrum of the device, the digitial-modulated carrier, and the demodulated bit sequence.

### Key Features
- Wideband Scanning: this project features a frequency slider that allows to tune to the desired RF signal with a range of 200-500 MHz
- Multi-Domain Analysis: this project features plots that allow the user to view signals in both the Frequency (FFT) and Time domain simultaneously
- ASK Demodulation: this project includes a Complex-to-Magnitude block to visualize the envelope of the ASK/OOK signal allowing the user to view the transmitted bit sequence

## Signal Processing Chain
The logic of the flowgraph is as follows:

1. OsmoSDR Source: Captures raw I/Q samples at a sampling rate of 2.0 Msps

2. Frequency Visualization: Raw data is passed into a QT GUI Frequency Sink to display the spectral density

3. Digital-Modulated Signal Visualization: Raw complex data is passed to a QT GUI Time Sink to display the ASK signal

4. Envelope Detection Visualization: raw data is passed through a complex to magnitude block which removes the carrier revealing the digital pulse sequence displayed on another QT GUI Time Sink

## How to Use
1. Install dependencies: Ensure that you have gnuradio and gr-osmosdr installed on your system

2. Open GRC: Launch GNU radio and open the .grc file

3. Execute: Click the play button on the top bar to start the program

4. Visualize: Plots will be displayed for the user with a slider at the top to adjust target frequency
