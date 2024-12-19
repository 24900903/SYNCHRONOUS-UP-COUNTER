### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram.

**PROGRAM**

     ```Developed by: Harisha 
        RegisterNumber:24900903
        module e11(out,clk,rst);
        input clk,rst;
        output reg [3:0]out;
        always @ (posedge clk)
        begin
        if(rst)
        out<=0=>
        else
       out <= out+1; end
       endmodule```


**RTL LOGIC UP COUNTER**
![d11a](https://github.com/user-attachments/assets/9ee5e86a-28ca-49b5-be48-dd0f7ebbef9f)

**TIMING DIAGRAM FOR IP COUNTER**
![d11b](https://github.com/user-attachments/assets/a7464f64-629c-47e2-a60e-385a561aafd1)

**TRUTH TABLE**
![d11c](https://github.com/user-attachments/assets/9ad95ff3-3d0f-48f5-a1d3-c756995b3f87)

**RESULTS**
Thus 4 bit synchronous up counter is implemented and functionality is validated.
