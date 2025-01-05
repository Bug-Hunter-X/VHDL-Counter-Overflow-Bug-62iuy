# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL code: improper handling of counter overflow.  The `buggy_counter.vhdl` file contains a counter that lacks robust overflow management.  The `fixed_counter.vhdl` file provides a corrected version.

## The Bug
The original VHDL code increments a counter. However, when the counter reaches its maximum value (15), it wraps around to 0 without explicitly signaling any overflow condition.  This could cause unexpected behavior in a larger design.

## The Solution
The solution uses a more robust approach.  It either adds an overflow output signal or uses a modulo operator for cleaner overflow handling. This version explicitly manages the counter limit.