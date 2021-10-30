# 4-bit_Register-Verilog
A verilog program that mimics the circuitry of a 4-bit register implemented with four 4x1 multiplexers and four D-Flipflops.  
The register operates according to the value of the select lines as shown below:-  
  
**s1          s0     Output**   
0             0      No change  
0             1      Complement Output  
1             0      Shift bits to right  
0             1      Shift bits to the left    
'Load' input is used to enable the D-FlipFlop.  
'Reset' used to remove don't care state and set the initial values of the flip flops to 0.  
  
The lib.v file contains the code for the basic gates, D-flip flop and a 2x1 multiplexer. The source.v contains code for the 4-bit register and four 4x1 multiplexers. The reg_tb files contains the input test bench values used by the program as input.  
  
Link to their website: [Icarus-Verilog](http://iverilog.icarus.com/)  
### Steps to run this code:-      
 _Open command prompt in the location where the files are stored and type the following commands to run the code_
 
 ``` 
 iverilog -o reg_v lib.v source.v reg_tb.v  
 ``` 
 ``` 
 vvp reg_v  
 ```
``` 
gtkwave tb_file.vcd 
``` 
(enter the dump file name specified in the reg_tb file for `tb_file.vcd`)  
