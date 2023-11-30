# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/
### SR FLIPFLOP
![SR](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/484ba255-0f12-4b66-9605-f78c531df19d)

### D FLIPFLOP
![D](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/deee825b-b51d-4233-a35f-35fff500e6da)

### JK FLIPFLOP
![JK](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/89f3c9df-77bd-4d86-974c-2fdc18de1df8)

### T FLIPFLOP
![T](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/871c1c32-b4ce-419d-9388-6e6aa03fb967)

### RTL LOGIC FOR FLIPFLOPS 

### SR FLIPFLOP
![SR RTL](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/b9dd0006-7a10-4867-90a3-62a2ea827a83)

### D FLIPFLOP
![D RTL](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/2c803535-b97c-4510-9a53-41d7d81311bb)

### JK FLIPFLOP
![JK RTL](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/9fa75600-b48d-47ad-a6a8-c81999707125)

### T FLIPFLOP
![T RTL](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/f63ed0ef-6dcf-4fff-85ac-2132fc6d84cc)

### TIMING DIGRAMS FOR FLIP FLOPS 

### SR FLIPFLOP
![SR TIME](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/3ffe7570-20b8-4313-9677-c1afe8d05ac9)

### D FLIPFLOP
![D TIME](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/20108fcc-30c2-4222-8c92-006e447cc85e)

### JK FLIPFLOP
![JK TIME](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/0c5b7bb7-4a01-41f9-bf59-fc911f309d28)

### T FLIPFLOP
![t time](https://github.com/RANJANKUMAR007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152128740/24fbb53e-edbf-423a-b702-0d8a577839f0)

### RESULTS 
Thus SR, D , JK and T flip flop has been executed successfully using verilog programming
