# UART-


This repository contains a simple **UART (Universal Asynchronous Receiver/Transmitter)** design written in Verilog, along with a testbench for simulation.  
The project demonstrates serial communication at the RTL level, including **baud rate generation, transmission, and reception**.

## 📂 Project Structure

├── uart_top.v # Top-level wrapper for TX + RX

├── uarttx.v # UART Transmitter module

├── uartrx.v # UART Receiver module

├── uart_tb.v # Testbench for verification



## ⚙️ Features

- Parameterized design:
  - `clk_freq` → System clock frequency (Hz)
  - `baud_rate` → UART baud rate (bps)
- **UART Transmitter**
  - Generates baud clock
  - Sends 8 data bits with start & stop framing
  - Asserts `donetx` when transmission completes
- **UART Receiver**
  - Detects start bit
  - Samples 8 data bits (LSB first)
  - Asserts `donerx` when reception completes
- Fully synthesizable RTL
- Testbench included for TX and RX

🚀 **Future Improvements**
Optional parity bit support

