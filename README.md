 Experiment-08- Encoders-and-decoders 
 AIM: To implement 8 to 3 Encoder and  3to8 Decoder using verilog and validate its outputs
 HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
 SOFTWARE REQUIRED:   Quartus prime
 THEORY 

 Encoders
Binary code of N digits can be used to store 2N distinct elements of coded information. This is what encoders and decoders are used for. Encoders convert 2N lines of input into a code of N bits and Decoders decode the N bits into 2N lines.

1. Encoders –
An encoder is a combinational circuit that converts binary information in the form of a 2N input lines into N output lines, which represent N bit code for the input. For simple encoders, it is assumed that only one input line is active at a time.

As an example, let’s consider Octal to Binary encoder. As shown in the following figure, an octal-to-binary encoder takes 8 input lines and generates 3 output lines.

![image](https://user-images.githubusercontent.com/36288975/171543588-bc0746df-a173-4b35-989e-5fb7d385fe8a.png)
 Figure -01 3 to 8 Encoder 


Implementation –

X = D4 + D5 + D6 + D7
Y = D2 +D3 + D6 + D7
Z = D1 + D3 + D5 + D7 
Hence, the encoder can be realised with OR gates as follows:


![image](https://user-images.githubusercontent.com/36288975/171543740-68403b82-aa93-4c98-9343-f32b14885a2e.png)
 Figure -02 3 to 8 Encoder implenentation 

  Decoders 
A decoder does the opposite job of an encoder. It is a combinational circuit that converts n lines of input into 2n lines of output.

Let’s take an example of 3-to-8 line decoder.
Implementation –
D0 is high when X = 0, Y = 0 and Z = 0. Hence,

D0 = X’ Y’ Z’ 
Similarly,

D1 = X’ Y’ Z
D2 = X’ Y Z’
D3 = X’ Y Z
D4 = X Y’ Z’
D5 = X Y’ Z
D6 = X Y Z’
D7 = X Y Z 


![image](https://user-images.githubusercontent.com/36288975/171543978-ee2d0671-2846-40a1-8705-507fd6287a49.png)
 Figure -03 8 to 3 Decoder 



![image](https://user-images.githubusercontent.com/36288975/171543866-5a6eace6-8683-49d7-9c4f-a7cb30ec3035.png)
 Figure -04 8 to 3 Decoder implementation 

 Procedure
1.create module encoder and decoder.

2.Get inputs and outputs for encoders and decoders.

3.perform or operation for encoder and and logic for decoders.

4.perform RTL LOGIC and get waveform.



 PROGRAM 
module enc(d0,d1,d2,d3,d4,d5,d6,d7,a,b,c);

input d0,d1,d2,d3,d4,d5,d6,d7;

output a,b,c;

or(a,d4,d5,d6,d7);

or(b,d2,d3,d6,d7);

or(c,d1,d3,d5,d7);

endmodule


Developed by: J.B.Viniya
RegisterNumber: 22008831 







 RTL LOGIC  





![Screenshot (36)](https://user-images.githubusercontent.com/121683551/214364274-1475f81b-b1ef-4cfa-9ee7-7a09590803a3.png)
![Screenshot (39)](https://user-images.githubusercontent.com/121683551/214364638-ada396b5-acfd-4649-abee-6308d5bf79bf.png)



 TIMING DIGRAMS  



![Screenshot (37)](https://user-images.githubusercontent.com/121683551/214364433-ca52c400-2f00-4264-b331-fa203d8464fa.png)

![Screenshot (40)](https://user-images.githubusercontent.com/121683551/214364748-1708ea7b-e5c6-49d3-868f-9ef8c6cb906a.png)

 TRUTH TABLE 




![Screenshot (41)](https://user-images.githubusercontent.com/121683551/214364845-ae2decff-ef44-4d45-b1d9-eef8546fb8fc.png)

![Screenshot (38)](https://user-images.githubusercontent.com/121683551/214364527-67f2711b-3405-4872-a8e2-b838f048e5b6.png)

 RESULTS 
