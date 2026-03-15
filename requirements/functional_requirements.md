
# Functional Requirements

- FR001:
At power up, system shall inhibit any motion until
1. Brake lock feedback is received.
2. Car Door closed AND locked feedback is received.
3. Elevators current position is established and Current_Floor_ID is initialized. System enters 'Recovery Mode' if Current_Position cannot be verified via floor proximity sensors.

- FR002:
The system shall process three user input types:
1. Target Floor Selection
2. Door Hold
3. Manual Door Close

- FR003:
The controller shall determine motion direction by comparing Current_Floor_ID to Target_Floor_ID.

- FR004:
The motion profile shall execute a jerk-Limited S-Curve during all acceleration and deceleration phases.

- FR005:
The Door_Open_Command shall be inhibited unless all below conditions are met
1. Velocity == 0
2. Mechanical_Brake == Engaged
3. Floor_Alignment == TRUE.

- FR006:
During In-Motion states, the system shall ignore Door_Control inputs unless a Priority Safety Override is active.

- FR007:
The system shall keep mechanical brakes engaged for all below conditions,
1. Current_Floor_ID = Target_Floor_ID AND Velocity < 0.05 m/s AND Floor_Alignment = TRUE
2. While in Loading phase where elevator and floor doors stay Open
3. After Loading phase, until system receives feedback that,
    1. Elevator door is Closed and Locked
    2. Floor door is Closed and Locked

- FR008:
Upon arrival, the doors shall remain in Open state for a default Dwell Time of 10 seconds (configurable) before auto-closing.

- FR009:
The Door_Close sequence shall be immediately aborted and reversed if the Light Curtain (obstruction sensor) is interrupted.

- FR010:
The system shall initiate motion only after all following conditions are met,
1. Current_Floor_ID is different than Target_Floor_ID.
2. Elevator Door is closed
3. Elevator door is locked
4. Floor door is closed
5. Floor door is locked



