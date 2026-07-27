![SystemVerilog](https://img.shields.io/badge/SystemVerilog-Language-blue)
![UVM](https://img.shields.io/badge/UVM-Verification-green)
![APB](https://img.shields.io/badge/APB-Protocol-red)
![SVA](https://img.shields.io/badge/SVA-Assertions-orange)
![Functional Coverage](https://img.shields.io/badge/Functional-Coverage-yellow)
![QuestaSim](https://img.shields.io/badge/QuestaSim-Simulator-blue)

# APB IP Core Verification

## Project Overview

This project focuses on the functional verification of an AMBA APB (Advanced Peripheral Bus) IP Core using **SystemVerilog**, **UVM**, and **SystemVerilog Assertions (SVA)**.

The verification environment was developed using the Universal Verification Methodology (UVM) to validate APB protocol compliance, finite state machine (FSM) behavior, read/write transactions, wait-state handling, and communication between the APB master and multiple slaves.

---

# Project Description

Verified the APB finite state machine consisting of the following protocol states:

- **Idle** (PSEL = 0, PENABLE = 0)
- **Setup** (PSEL = 1, PENABLE = 0)
- **Access** (PSEL = 1, PENABLE = 1)

The project also verified:

- Master to Same Slave communication
- Master to Different Slave communication
- Wait-state insertion using the **PREADY** signal
- APB protocol timing and control signal behavior

---

# Responsibilities

- Architected a reusable **UVM-based verification environment**.
- Defined the **Verification Plan** and **Feature Extraction Sheet**.
- Developed directed and constrained-random testcases for:
  - Write operations with and without wait states
  - Read operations with and without wait states
  - Same slave communication
  - Different slave communication
  - Back-to-back read/write transfers
- Implemented multiple data and address generation modes:
  - Random
  - User Pattern
  - Constant
  - Increment
  - Decrement
- Generated **Functional Coverage** and **Code Coverage** for RTL verification sign-off.
- Developed **SystemVerilog Assertions (SVA)** for:
  - Reset verification
  - Read transactions
  - Write transactions
  - Setup state
  - Access state
  - APB protocol timing

---

# UVM Verification Environment

The verification environment consists of:

- Sequence Item
- Sequencer
- Driver
- Monitor
- Agent
- Scoreboard
- Coverage Collector
- Environment
- Test
- Virtual Interface

---

# Features Verified

### APB FSM

- Idle State
- Setup State
- Access State
- State Transitions

### Transactions

- Single Read
- Single Write
- Back-to-Back Read
- Back-to-Back Write
- Mixed Read/Write

### Slave Communication

- Same Slave Communication
- Different Slave Communication

### Wait-State Handling

- PREADY Low
- PREADY High
- Extended Access Cycle

### Assertions

- Reset Checks
- Read Timing
- Write Timing
- Setup Phase
- Access Phase
- Protocol Compliance

---

# Verification Methodology

- UVM
- SystemVerilog
- SystemVerilog Assertions (SVA)
- Constrained Random Verification
- Functional Coverage
- Code Coverage
- Coverage-Driven Verification
- Regression Testing

---

# Tools Used

- SystemVerilog
- UVM
- QuestaSim
- Linux
- Git

---

# Simulation Flow

1. Compile RTL and Testbench
2. Run UVM Testcases
3. Execute Regression Suite
4. Analyze Waveforms
5. Debug Failures
6. Generate Coverage Reports
7. Complete Verification Sign-off

---

# Repository Structure

```text
APB_UVM_Verification/
│
├── rtl/
├── tb/
├── sequence_item/
├── sequences/
├── sequencer/
├── driver/
├── monitor/
├── agent/
├── scoreboard/
├── coverage/
├── assertions/
├── tests/
├── docs/
├── waveforms/
└── README.md
```

---

# Key Highlights

- Reusable UVM Verification Environment
- Directed and Constrained-Random Testing
- APB Protocol Verification
- Functional & Code Coverage
- Assertion-Based Verification (SVA)
- Waveform Debugging
- Regression Testing

---

# Contact

**Guru Naveen Reddy Siddu**

📧 Email: gurunaveenreddys@gmail.com

🔗 LinkedIn:  
https://www.linkedin.com/in/siddu-guru-naveen-reddy-93b597282

💻 GitHub:  
https://github.com/Sn9490
