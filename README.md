# APB_UVM_Verification
 Verified the APB FSM Which Consist of Idle(psel=0, penalble=0), Setup(psel=1, penalble=0) and Access(psel=1, penalble=1) state and done master to same slave and different Slave communication and understaood the importance of Pready signal. 

---

## Features Verified
- APB FSM Transitions
  - Idle
  - Setup
  - Access

- Write Operations
- Read Operations
- Wait State Handling
- Back-to-Back Transactions
- Same Slave and Different Slave Communication

---

## Verification Methodology
- UVM-Based Testbench
- Constrained Random Verification
- Functional Coverage
- Assertion-Based Verification
- Scoreboarding
- Regression Testing

---

## UVM Components
- Sequencer
- Driver
- Monitor
- Agent
- Scoreboard
- Coverage Collector
- Environment
- Testcases

---

## Assertions Implemented
- Reset Checks
- Setup to Access Transition
- Read/Write Timing Checks
- Protocol Stability Checks

---

## Coverage Achieved
- Functional Coverage: 95%
- Code Coverage: 90%+

---

## Tools Used
- QuestaSim
- SystemVerilog
- UVM
- Linux

---

## Simulation Flow
1. Compile RTL and Testbench
2. Run UVM Testcases
3. Generate Waveforms
4. Analyze Functional Coverage
5. Debug Assertion Failures

---

## Waveform Screenshots
Waveforms are available in the `waveforms/` directory.

---

## Verification Architecture
Architecture diagrams are available in the `docs/` directory.
```
