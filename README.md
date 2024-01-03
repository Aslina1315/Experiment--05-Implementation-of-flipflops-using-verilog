# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables

### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime

### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/50da9a82-958e-41ec-a998-bba4b7769967) 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/6ceb98af-bad2-4fcf-a1c2-4ea4af6b906b)
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/7de46630-78d6-4def-9bec-1975213efe87)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/d0183cd0-2f8d-4441-bc8f-dcf55d49e8b3) 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/be2a98a9-cc8f-4b9a-94da-9363d0df8eba)
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/fd14558a-973d-49c7-a626-077ecf1ab5e2)
Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/9226869a-d5e2-4f9d-ad42-1c98fbe93492)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/e3d453b2-f9d3-4539-856a-c5e695a6b052)


 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/3a148e4a-11c8-4419-998b-c5fe765eaa9e)
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/103851d9-69e5-4087-be20-0809805e8cde)



By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 ![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/b7580b90-c7ab-4422-9022-ae14643ed06f)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/4380a504-d98d-4c4e-9e13-64e89d0e7d7e)
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/e363c2d7-799e-45cc-8b3d-8dbfeb92b551)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
Step:1 Open Quartus II and select new project and choose the file location. 
Step:2 Module Declaration. Module should have the file name.
Step:3 Declare Inputs and outputs.
Step:4 Use assign declaration and wire to define the functionality of logic circuits. 
Step:5 End the program with endmodule. 
Step:6 Run the program and choose RTL viewer to get RTL realization.

### PROGRAM :
PROGRAM :
SR Flip-Flop :-
module exp_5_1(S,R,clk,Q,Qbar);
input S,R,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=S|((~R)&Q);
Qbar=R|((~S)&(Qbar));
end
endmodule

D Flip-Flop :-
module exp_5D(D,clk,Q,Qbar);
input D,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin 
Q=D;
Qbar=~D;
end
endmodule

JK Flip-Flop :-
module exp_5_2(J,K,clk,Q,Qbar);
input J,K,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=(J&(~Q))|((~K)&Q);
Qbar=((~J)&(Qbar))|K&(~Qbar);
end
endmodule

T Flip-Flop :-
module exp_5_4(T,clk,Q,Qbar);
input T,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=(T&(~Q))|((~T)&Q);
Qbar=((~T)&Qbar)|(T&(~Qbar));
end 
endmodule
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by:M.Noorul aslina
RegisterNumber: 212223050033 
*/


### RTL LOGIC FOR FLIPFLOPS 

SR Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/e1564f86-9ec2-4bcc-a650-2eda3fa1faee)


D Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/a2290ad9-8349-4a2a-920f-e03a00727a9b)


JK Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/a8983ed8-f834-4e35-a937-729f13e47b0d)


T Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/ff7f2d7a-ec96-4232-a103-aece6fa57689)


TIMING DIGRAMS FOR FLIP FLOPS
SR Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/f6a75587-dbaf-4089-b87f-6d69f286da09)


D Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/64188863-c877-45c2-bd34-0b542d6454cd)


JK Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/2bf094cf-5d91-498a-86be-debe49a13068)


T Flip-Flop :-
![image](https://github.com/Aslina1315/Experiment--05-Implementation-of-flipflops-using-verilog/assets/155459437/daf13c18-6b61-4091-b609-7b9a9a52cd5e)


### RESULTS :
Implementation-of-flipflops-using-verilog successfully completed.


