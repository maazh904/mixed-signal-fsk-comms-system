
# Mixed-Signal FSK Communication System

**Status:** In Development | November 2026 – Present

## Project Overview

This project aims to develop an ESP32-based mixed-signal communication system capable of transmitting and receiving binary information using Frequency Shift Keying (FSK).

An AD9833 Direct Digital Synthesis (DDS) module will generate analog carrier signals, while a custom MCP6022-based receiver will condition incoming waveforms for sampling by the ESP32's ADC.

Digital signal processing algorithms, including Goertzel-based frequency detection, will be implemented to recover transmitted data.

## System Architecture

The planned system consists of:

1. **FSK Transmitter:** ESP32-controlled AD9833 DDS module generating frequency-modulated signals.
2. **Analog Receiver:** Op-amp-based signal conditioning, amplification, biasing, and filtering.
3. **Embedded DSP:** ESP32 ADC sampling and frequency-domain signal detection.
4. **User Interface:** OLED display, rotary encoder, and push buttons.
5. **Hardware Validation:** Digilent Analog Discovery 3 for waveform measurements and debugging.

## Hardware Components

| Component | Function |
|---|---|
| ESP32 LOLIN32 Lite | Embedded control and digital signal processing |
| AD9833 | Programmable analog waveform generation |
| MCP6022 | Analog signal conditioning and amplification |
| MCP4131 | Programmable signal attenuation |
| OLED Display | System interface and status display |
| Rotary Encoder | Parameter adjustment |
| Analog Discovery 3 | Oscilloscope measurements and debugging |

## Development Roadmap

- [ ] Milestone 1: Verify AD9833 waveform generation
- [ ] Milestone 2: Implement binary FSK transmission
- [ ] Milestone 3: Design and test the analog receiver
- [ ] Milestone 4: Implement ESP32 ADC sampling
- [ ] Milestone 5: Develop Goertzel-based demodulation
- [ ] Milestone 6: Implement message transmission and synchronization
- [ ] Milestone 7: Integrate programmable attenuation and user interface
- [ ] Milestone 8: Design, fabricate, and validate a custom PCB

## Current Progress

Initial KiCad schematic development has begun, including:

- Creation of a custom LOLIN32 Lite schematic symbol.
- Representation of the AD9833 module's external connections.
- Initial SPI signal, power, and ground wiring.
- Electrical Rules Checking (ERC) to identify and resolve connectivity issues.

**Note:** The existing schematic is preliminary and originated from an earlier DDS function-generator design. Pin assignments and physical header numbering still require verification. No FSK transmission or analog receiver testing has been completed yet.

## Planned Validation

The completed prototype will be evaluated through:

- Carrier-frequency measurements
- Analog receiver gain and filtering tests
- Successful binary-data recovery
- Bit-error-rate (BER) measurements
- Hardware performance under different signal conditions

## Development Notes

Project documentation, schematics, firmware, calculations, and experimental results will be uploaded as milestones are completed.

Each milestone will include relevant design files, implementation details, testing procedures, experimental results, and engineering observations.
