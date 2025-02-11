# Uncommon VHDL Counter Bug: Implicit Else Condition

This repository demonstrates a subtle bug in a VHDL counter implementation. The bug stems from an implicit 'else' condition within a `process` statement.  While seemingly functional, the lack of an explicit `else` statement can cause unpredictable behavior.

The `bug.vhdl` file contains the buggy code, which might lead to unexpected counter values under certain conditions.  The solution is demonstrated in the `bugSolution.vhdl` file.

## Bug Description:
The counter's increment logic inside the `rising_edge(clk)` section lacks an explicit `else` statement. Although the `if` condition handles the maximum count,  the code's behavior is undefined if the counter is not at its maximum, potentially leading to unintended consequences.

## Solution:
The solution involves explicitly stating the `else` condition, ensuring that the counter's behavior is clearly defined in all scenarios.  Refer to `bugSolution.vhdl` for the corrected implementation.