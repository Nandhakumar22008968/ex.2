### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![Screenshot 2023-05-30 173039](https://github.com/Nandhakumar22008968/ex.2/assets/129037794/ae4a20d5-3768-407b-af4e-a63cc24adbe8)
![Screenshot 2023-05-30 173126](https://github.com/Nandhakumar22008968/ex.2/assets/129037794/3c01c2d9-ca15-41f3-81aa-b15287a84766)


## Truth Table:


## Program:
~~~
module exp2a(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
~~~



## RTL Schematic:
![Screenshot_20230526_085919](https://github.com/Nandhakumar22008968/ex.2/assets/129037794/e1ab6668-337f-4eca-8086-b2680fd7a41b)




## Timing Diagram:
![Screenshot_20230421_024510](https://github.com/Nandhakumar22008968/ex.2/assets/129037794/2917b902-e85c-4129-87be-35f13a633f32)





## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



