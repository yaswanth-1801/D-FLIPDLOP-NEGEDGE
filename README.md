# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1. Define Inputs/Outputs: Inputs: D (data), c1k (clock); Outputs: Q, Qbar (~Q).
2. Initialization: Set Q = 0 and Qbar = 1 at the start of the simulation.
3. D Flip-Flop Logic: On the positive edge of c1k, assign Q = D.
4. Complementary Output: Update Qbar = ~D to maintain complementarity.
5. Testbench: Test with various D and c1k values to verify data storage functionality.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
Developed by: KABELAN G K
RegisterNumber: 24900985
*/

```
module exp8(D,c1k,Q,Qbar);
input D,c1k;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge c1k)
begin
Q=D;
Qbar=~D;
end
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/user-attachments/assets/4f09eb8b-075c-4260-a2c6-2b9d5a34193c)



**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/user-attachments/assets/4ddec297-8a03-4d92-8601-826a237273b1)



**RESULTS**

Thus the D flipflop is implemented and verified.
