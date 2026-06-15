![SystemVerilog](https://img.shields.io/badge/SystemVerilog-Language-blue)
![UVM](https://img.shields.io/badge/UVM-Verification-green)
![APB](https://img.shields.io/badge/APB-Protocol-red)
![SVA](https://img.shields.io/badge/SVA-Assertions-orange)
![Functional_Coverage](https://img.shields.io/badge/Functional-Coverage-yellow)
![QuestaSim](https://img.shields.io/badge/QuestaSim-Simulator-blue)

# APB_UVM_Verification

## Overview

This project implements a complete UVM-based verification environment for the Advanced Peripheral Bus (APB) protocol. The verification environment validates APB finite state machine (FSM) behavior, protocol compliance, timing requirements, and transaction correctness using SystemVerilog, UVM, assertions, scoreboarding, and functional coverage.

---

## APB Protocol States Verified

The APB finite state machine consists of the following states:

### Idle State

* PSEL = 0
* PENABLE = 0

### Setup State

* PSEL = 1
* PENABLE = 0

### Access State

* PSEL = 1
* PENABLE = 1

All state transitions were verified according to the APB protocol specification.

---

## Features Verified

### FSM Verification

* Idle → Setup Transition
* Setup → Access Transition
* Access → Idle Transition
* Access → Setup Transition (Back-to-Back Transfers)

### Transaction Verification

* Single Write Transactions
* Single Read Transactions
* Consecutive Write Transactions
* Consecutive Read Transactions
* Mixed Read/Write Transactions

### Communication Verification

* Same-Slave Communication
* Cross-Slave Communication
* Multiple Slave Selection Scenarios

### Wait-State Verification

* PREADY Low Conditions
* PREADY High Conditions
* Extended Access Phase Handling

### Protocol Compliance Checks

* PSEL Stability
* PENABLE Timing
* Address Stability
* Data Stability
* Transfer Completion Conditions

---

## Verification Methodology

The design was verified using Universal Verification Methodology (UVM).

### Verification Techniques Used

* UVM-Based Verification
* Constrained Random Verification
* Directed Testing
* Functional Coverage
* Code Coverage
* Assertion-Based Verification (SVA)
* Coverage-Driven Verification
* Scoreboarding
* Regression Testing

---

## UVM Architecture

The verification environment consists of the following UVM components:

### Sequence Item

* Transaction-level packet generation

### Sequencer

* Controls transaction flow

### Driver

* Drives APB transactions to DUT

### Monitor

* Captures DUT activity

### Agent

* Encapsulates driver, monitor, and sequencer

### Scoreboard

* Compares expected and actual DUT behavior

### Coverage Collector

* Collects functional coverage metrics

### Environment

* Integrates all verification components

### Test Cases

* Directed Tests
* Constrained Random Tests

---

## Assertions Implemented

SystemVerilog Assertions (SVA) were implemented to verify protocol correctness.

### Assertion Checks

* Reset Behavior Validation
* Idle-to-Setup Transition Checks
* Setup-to-Access Transition Checks
* Read Transaction Timing Checks
* Write Transaction Timing Checks
* PREADY Wait-State Validation
* Protocol Stability Checks
* Signal Timing Compliance Checks

---

## Functional Coverage

Coverage models were developed to ensure comprehensive protocol verification.

### Coverage Points

* FSM State Coverage
* Read Transactions
* Write Transactions
* Slave Selection Coverage
* Wait-State Coverage
* Back-to-Back Transfer Coverage
* Cross Coverage of Protocol Scenarios

### Coverage Results

* Functional Coverage: 95%
* Code Coverage: 90%+

---

## Regression Testing

Regression suites were executed to verify protocol stability and functionality under various scenarios.

### Regression Includes

* Directed Testcases
* Randomized Testcases
* Corner Case Scenarios
* Wait-State Scenarios
* Back-to-Back Transactions
* Multi-Slave Communication

---

## Results

* Successfully verified APB protocol functionality.
* Achieved 95% functional coverage.
* Achieved 90%+ code coverage.
* Validated protocol compliance through assertions.
* Verified same-slave and cross-slave communication.
* Debugged and resolved protocol violations using waveform analysis and regression testing.

---

## Tools Used

* SystemVerilog
* UVM
* QuestaSim
* Linux
* Git

---

## Simulation Flow

1. Compile RTL and Verification Environment.
2. Run UVM Testcases.
3. Execute Regression Suite.
4. Generate Waveforms.
5. Analyze Coverage Reports.
6. Debug Assertion Failures.
7. Achieve Coverage Closure.

---

## Repository Structure

```text
APB_UVM_Verification
│
├── rtl/
├── tb/
├── sequences/
├── driver/
├── monitor/
├── scoreboard/
├── coverage/
├── assertions/
├── tests/
├── docs/
├── waveforms/
└── README.md
```

---

## Waveforms

Simulation waveform screenshots are available in the `waveforms/` directory.

---

## Verification Architecture

UVM architecture diagrams are available in the `docs/` directory.

---

## Contact

Guru Naveen Reddy Siddu

Email: [gurunaveenreddys@gmail.com](mailto:gurunaveenreddys@gmail.com)

LinkedIn:
https://www.linkedin.com/in/siddu-guru-naveen-reddy-93b597282

GitHub:
https://github.com/Sn9490
