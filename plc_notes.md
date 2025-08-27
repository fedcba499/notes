## What is Coil (Output)?
Previously Coil was used to generate magnetic field, which in turns turn on lamp, motor or any output. Hence, from then coil or output used synonymously used in PLC Ladder Diagram.

## What is Positive Trigger or Negative Trigger?
Positive Trigger (Rising Edge) is used to determine if signal changes from 0 to 1. If switch is on (1), if we press again (1), then there is no increase in value. It does not affect circuit.
Negative Trigger (Falling Edge) is used to determine if signal changes from 1 to 0. 

## What is Memory bit, Set and Reset?
Memory bit is similar to Boolean variable, it stores 0 or 1 value, it does not attached to physical hardware (like sensors, buttons etc), instead it stores value in memory.
- Set is to assign 1, or True value to Memory Bit.
- Reset is to assign 0 or False value to Memory Bit.

## What is Function Block?
Function Block is like Functions in Python Programming (Methods). It has input variable in Left Side, and Output in Right Side. Certain Function Blocks are as under
- TIMER_ON_DELAY (TON)
- TIMER_OFF_DELAY
- UP_COUNTER
- DOWN_COUNTER

## What is TIMER_ON_DELAY ? What are Variables attached to it? Explain them?
TIMER_ON_DELAY is used to turn on after preferred delay time.
It has 4 variables
- IN - to indicate input signal
- ENO - Enable Output
- PV - Preset Value
- CV - Current Value

## What is Ent Button?
Ent button stands for "ENTER" to confirm entered value or to say "OK".


