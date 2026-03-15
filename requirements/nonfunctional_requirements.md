# Non-functional Requirements

- NFR001:
The system shall maintain a nominal steady-state velocity of 2.0 m/s (±5%).

- NFR002:
Once user/rider enters input through key pad then it shall be process in less than a second. If all conditions are satisfied, elevator shall initiate motion in < 500ms.

- NFR003:
The Door Actuation System shall achieve full egress width within 2.5s of receiving the Door_Open command.

- NFR004:
The Door Actuation System shall achieve full egress width within 3.5s of receiving the Door_Close command. 
*Note: To avoid hazards and to ensure safety during closing sequence, the performance is intentionally lowered.*

- NFR004:
Vertical Jerk shall be limited to ≤ 1.5 m/s³ to ensure rider comfort.

- NFR005:
System boot and safety-integrity self-tests shall complete in < 10s.

- NFR006:
If obstruction is detected during Door Close sequence then system shall react and revert to Door Open in less than 200ms.

- NFR007:
The system shall be designed for 100,000 cycles before requiring mechanical maintenance.

- NFR008:
The controller shall maintain specified performance within a temperature range of -10°C to +50°C.

- NFR009:
The car shall stop within ±5mm of the floor landing to prevent tripping hazards.