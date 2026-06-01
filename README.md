# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/* write all the steps invloved */

```
1.Open Quartus software and create a new project.
2.Write the Verilog code for the 4-bit ripple counter.
3.Compile the design and assign input/output pins.
4.Run simulation to check the counting output.
5.Program the FPGA board and observe the result.
```

**PROGRAM**
```
module exp6de(
    input clk,
    input rst,
    output reg [3:0] count
);

always @(posedge clk or posedge rst)
begin
    if (rst)
        count <= 4'b0000;
    else
        count <= count + 1'b1;
end

endmodule
```
/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.
```
 Developed by: KOPIGA N
 RegisterNumber: 212225220053
```
*/

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="1352" height="806" alt="image" src="https://github.com/user-attachments/assets/3ff539d0-0634-408e-93ed-5970cee802bb" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1390" height="745" alt="image" src="https://github.com/user-attachments/assets/f616c82b-8b4c-4e81-b218-ca1cbfc0a5a9" />

**RESULTS**
Thus, the 4-BIT-RIPPLE-COUNTER successfully designed and verified using Quartus software.
