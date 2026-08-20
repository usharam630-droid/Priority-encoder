# 4-to-2 Priority Encoder using Verilog

## Project Description

A 4-to-2 Priority Encoder is a combinational logic circuit that converts four input lines into a 2-bit binary output. Unlike a standard encoder, a priority encoder assigns priority to the inputs. If more than one input is HIGH simultaneously, the encoder generates the binary code corresponding to the highest-priority active input.

In this design, the priority order is:

**D3 > D2 > D1 > D0**

This project implements a 4-to-2 Priority Encoder using Verilog HDL and verifies its operation with a comprehensive testbench.

---

## Truth Table

| D3 | D2 | D1 | D0 | Y1 | Y0 |
|----|----|----|----|----|----|
| 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 0 | 1 | 0 | 0 | 1 |
| 0 | 1 | 0 | 0 | 1 | 0 |
| 1 | 0 | 0 | 0 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 1 | 1 |

---

## Priority Order

```
Highest Priority → D3
                  D2
                  D1
Lowest Priority → D0
```

---

## Files

- `priority_encoder4x2.v` – Verilog design
- `priority_encoder4x2_tb.v` – Testbench
- `output.txt` – Expected simulation output
- `README.md` – Project documentation

---

## Software Used

- Icarus Verilog
- ModelSim
- Xilinx Vivado

---

## How to Run

Compile:

```bash
iverilog priority_encoder4x2.v priority_encoder4x2_tb.v
```

Run:

```bash
vvp a.out
```

---

## Expected Output

```
D3 D2 D1 D0 | Y1 Y0
0  0  0  0 | 0  0
0  0  0  1 | 0  0
0  0  1  0 | 0  1
0  1  0  0 | 1  0
1  0  0  0 | 1  1
0  1  1  0 | 1  0
1  1  0  0 | 1  1
1  1  1  1 | 1  1
```

---

## Applications

- Interrupt Controllers
- Processor Scheduling
- Bus Arbitration
- Keyboard Encoding
- Digital Communication Systems

---

