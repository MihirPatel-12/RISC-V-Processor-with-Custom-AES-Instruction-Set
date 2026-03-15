markdown
# RISC-V Processor with Custom AES Instruction Set

## About the Project
This project presents the design and implementation of a single-cycle RISC-V processor integrated with a hardware Advanced Encryption Standard (AES) cryptographic accelerator [1]. Traditional software-based AES implementations on general-purpose processors often suffer from high latency and significant computational overhead [2]. To address this, this processor is implemented in Verilog HDL and extends the base RISC-V architecture with custom AES instructions [1, 3]. By executing cryptographic operations directly in dedicated hardware, this design significantly improves encryption performance and reduces execution cycles, making it highly efficient for resource-constrained embedded systems and IoT devices requiring hardware-accelerated security [4, 5].

## Key Features
*   **Base RISC-V Architecture:** Follows a single-cycle execution flow where every instruction completes in one clock cycle [6]. It supports the standard RV32I instruction formats, including R-type, I-type, S-type, B-type, U-type, and J-type instructions to handle arithmetic, logical, memory, and control operations [7, 8].
*   **Custom AES Instructions:** Extends the standard instruction set with custom instructions tailored specifically for cryptographic operations, allowing a single instruction to replace complex software execution steps [1, 9].
*   **Dedicated Hardware Acceleration:** Integrates dedicated sequential hardware modules for all core AES-128 operations: SubBytes, ShiftRows, MixColumns, and AddRoundKey [1, 9]. It also includes a Key Expansion unit capable of generating 11 128-bit round keys [10].
*   **Performance Optimization:** Solves the issues of high latency and high computational overhead found in traditional software-based encryption by reducing the number of clock cycles required to complete an encryption round [2, 4, 6].

## Tech Stack
*   **Hardware Description Language:** Verilog HDL [1]
