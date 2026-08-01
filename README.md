<div align="center">

# 🔗 APB IP Core Verification

### AMBA APB Protocol | Class-Based UVM Verification Environment

![SystemVerilog](https://img.shields.io/badge/HVL-SystemVerilog-1E88E5?style=for-the-badge)
![UVM](https://img.shields.io/badge/Methodology-UVM-FF6F00?style=for-the-badge)
![QuestaSim](https://img.shields.io/badge/Tool-QuestaSim-005A9C?style=for-the-badge)
![SVA](https://img.shields.io/badge/Assertions-SVA-8E2DE2?style=for-the-badge)

</div>

---

## 📖 Overview

This project verifies an **APB (Advanced Peripheral Bus)** protocol IP using a class-based **UVM** testbench. The verification focuses on the APB Finite State Machine (FSM) behavior, master-to-slave communication across single and multiple slaves, and correct handling of the `PREADY` handshake signal.

## 🔄 APB FSM States Verified

| State | Signals | Description |
|---|---|---|
| **Idle** | `psel = 0`, `penable = 0` | Bus is idle, no active transfer |
| **Setup** | `psel = 1`, `penable = 0` | Address/control phase begins |
| **Access** | `psel = 1`, `penable = 1` | Data transfer phase; may extend via `pready` |

Special attention was given to understanding the importance of the **`PREADY`** signal in extending the Access phase for slaves that require wait states.

## 🏗️ Verification Environment

Architected a **class-based UVM verification environment** with a full verification plan / feature extraction sheet defining test scope before implementation.

```
uvm_test
 └── uvm_env
      ├── master_agent (active)
      │    ├── sequencer
      │    ├── driver
      │    └── monitor
      ├── slave_agent(s) (active/passive)
      ├── scoreboard
      └── coverage collector
```

### Test Scenarios Covered
- ✅ Write operation — with and without wait states
- ✅ Read operation — with and without wait states
- ✅ Communication with the same slave (repeated transfers)
- ✅ Communication across different slaves
- ✅ Data/address patterns: **random, user-defined pattern, constant, increment, decrement**
- ✅ Back-to-back write and read operations (20 transactions)

## 🛡️ Assertions (SVA)

Assertions were written to check protocol compliance for:
- Reset behavior
- Write operation timing
- Read operation timing
- Setup → Access state transitions

## ✅ Verification Results

| Metric | Result |
|---|---|
| Functional Coverage | Achieved for all defined scenarios |
| Code Coverage | Collected and closed |
| Verification Sign-off | ✅ Achieved |
| Simulation Tool | QuestaSim |

## 🛠️ Tools & Technologies

- **HVL:** SystemVerilog
- **Methodology:** UVM (Universal Verification Methodology)
- **Simulator:** QuestaSim
- **Version Control:** Git

## 📂 Repository Structure

```
├── rtl/             # APB RTL design files
├── tb/              # UVM testbench (agents, sequences, scoreboard, env, tests)
├── assertions/       # SVA assertion modules
├── sim/              # Simulation scripts
├── docs/             # Verification plan / feature extraction sheet, coverage reports
└── README.md
```
<!-- Update this structure to match your actual repo layout -->

## 🚀 How to Run

```bash
# Example QuestaSim flow — update commands to match your scripts
vlib work
vlog -f filelist.f
vsim -c work.tb_top -do "run -all"
```
<!-- Replace with your actual simulation commands / Makefile targets -->

## 👤 Author

**Guru Naveen Reddy** — ASIC Design Verification Engineer
[LinkedIn](https://www.linkedin.com/in/siddu-guru-naveen-reddy-93b597282) · [GitHub](https://github.com/Sn9490) · gurunaveenreddys@gmail.com
