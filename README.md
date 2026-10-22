# Single-Cycle MIPS Processor

A 32-bit single-cycle MIPS processor written in SystemVerilog for my computer architecture course.

## Design

- 32-bit full adder and ALU, with ALU control
- 4-to-1 and 2-to-1 multiplexers
- Register file (32 x 32-bit), sign extender, instruction and data memory
- Main decoder and datapath for R-type, `lw`, `sw`, `beq` and `j` instructions

## Testing

Each part has a testbench (`*_tb.sv`) and was simulated in ModelSim. The 32-bit full adder passes all 10 test cases (`sim_fa_results.txt`). In the full processor run (`sim_mips_results.txt`) the program counter steps through the first instructions, but most values stay unknown (`x`), so the processor simulation still needs fixing.

## How to run

Open Intel Quartus and run `create_mips_project.tcl`, or compile the `.sv` files in ModelSim and run `mips_processor_tb`.
