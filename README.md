# fpga-floating-point-multiplier
High-performance 32-bit floating point multiplier on Artix-7 FPGA (Vedic, Booth, Array, Wallace, Braun) with power/area/speed comparison.

## 📖 Overview
This project implements a 32-bit IEEE 754 Floating Point Multiplier on the Xilinx Artix-7 FPGA.  
Five different multiplier architectures were designed and analyzed in Verilog to explore trade-offs in area, power, and speed.

## Architectures Implemented
- Vedic Multiplier
- Booth Multiplier
- Array Multiplier
- Wallace Tree Multiplier
- Braun Multiplier

Each architecture was synthesized using Xilinx Vivado and tested with Verilog testbenches.

##Comparative Analysis
The designs were evaluated on the *Artix-7 (xc7a100t-1csg324)* FPGA.  
Metrics considered:
- LUT utilization (%)
- Power consumption (mW)
- Memory utilization (%)
- Maximum frequency (speed)

| Architecture   | LUT Utilization | Power (mW) | Memory (KB) | Max Freq (MHz) | Remark                                         |
|----------------|-----------------|------------|-------------|----------------|------------------------------------------------|
| Vedic          | 41%             | 1.4        | 1.43        | 100            | Speed Critical but overall Balanced            |
| Booth          | 3.7%            | 1.5        | 1.07        | 100            | Speed and Area Efficient                       |
| Array          | 5.61%           | 2.5        | 2.14        | 100            | Area Efficient                                 |
| Wallace Tree   | 5.88%           | 2          | 3.93        | 100            | Consumes very low power                        |
| Braunn         | 3.86%           | 1.43       | 1.43        | 100            | Area Efficient                                 |

## Tools Used
- Verilog HDL
- Xilinx Vivado 2023.1
- Artix-7 (Nexys A7-100T) FPGA Board
