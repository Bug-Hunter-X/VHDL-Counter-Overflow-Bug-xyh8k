# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an integer counter that can overflow.  The original code (`buggy_counter.vhdl`) increments a counter without checking for the upper limit of its range, leading to unexpected behavior once it reaches its maximum value.  The corrected code (`buggy_counter_fixed.vhdl`) addresses this issue, preventing overflow.

## Bug Description
The `buggy_counter.vhdl` file contains a counter that increments on each rising edge of the clock signal.  However, it lacks a mechanism to handle the case when the counter reaches its maximum value (15). Once it reaches 15, the next increment wraps around to 0, resulting in incorrect behavior.

## Solution
The `buggy_counter_fixed.vhdl` file provides a corrected version of the counter.  It includes a check to prevent the counter from exceeding its upper limit. If the counter reaches 15, it remains at 15 instead of wrapping around.