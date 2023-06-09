# Shift Register

## Installation
To clone the repository go to a safe directory and in the terminal type the following, replacing `<URL>` with the url of the repository. <br> 
```
git clone <URL>
```

## Source Files
- shift_reg.sv : This is where the design code should be located.
- tb_shift_reg.sv : This is the test bench used to test your design.

## Specifations
### <u>Module Name</u> 
- shift_reg
### <u>Inputs</u>
- clk  &emsp; : System clock (Max Operating Frequency: 400 Mhz)
- nrst &ensp; : This is an asynchronous, active-low system reset. When this line is  asserted(logic ‘0’), all <br> &emsp; &emsp; &nbsp; &nbsp; registers/flip-flops in the device must reset to their initial value.
- D &emsp; &nbsp; : Serial Input to the shift register.
- mode_i [1:0] :  
  - hold &nbsp;: when mode_i = 2’b00, value in shift register doesn’t change.
  - load &nbsp;: when mode_i = 2’b01, store value of par_i in the register.
  - left &nbsp;: when mode_i = 2’b10, shift register contents to the left.
  - right : when mode_i  = 2’b11, shift register contents to the right.
- par_i [7:0] &nbsp; : Parallel input to the shift register.
### <u>Outputs</u>
- P [7:0] : Parallel output of the shift register.
## Behaviour
This design implements a parallel to parallel or serial to parallel (MSB or LSB) shift register. The behavior of the shift register is determined by the mode_i input of the module.
## Instructions
1. Clone the repo from github.
2. Run `make setup` to cofigure directory for the project.
3. Make an rtl-diagram for the shift register and have the design approved by a TA. Use [draw.io](https://app.diagrams.net/) **Make sure your design is located in the docs directory.**
4. Code your design in SystemVerilog.
5. Run `make help`/`make` to see the make file targets.
6. Have both source and mapped versions of your code working.
7. Have a TA review your source and mapped waveforms.

## Expected Results
Use the following signal dump to debug your HDL.

![GTKwave Simulation!](/img/sig_dump.png "GTKwave simulation")

## Submitting your design
Once your design has passed all the test cases, you need to commit your design.
This can be done in one of many ways, the primary one is through the Source Control
VS Code Tool (Ctrl + Shift + G). You will need to stage your changes, then you
can commit them, then you hit the sync button to sync your local repository with
the remote repository. These are a lot of words which are explaned in more detail 
in the GitHub fundementals assignment.
