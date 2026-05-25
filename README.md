# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
```clc;
clear;
xn=[1 2 3 4 4 3 2 1];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
    for k=0:N-1;
    for n=0:N-1;  
    Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
    end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle=atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum');
```
### CALCULATIONS:
<img width="911" height="1600" alt="image" src="https://github.com/user-attachments/assets/dad078ab-2cc7-4138-b0b0-6a9d5d1f8abc" />


<img width="1006" height="1600" alt="image" src="https://github.com/user-attachments/assets/4b780180-cf3d-4a01-aaee-dd4a0d4fcdb2" />


<img width="1023" height="1600" alt="image" src="https://github.com/user-attachments/assets/5b9511b5-2794-4a9f-a1c3-b034ed962d8b" />


### SAMPLE OUTPUT:
<img width="756" height="715" alt="DFT dtsp" src="https://github.com/user-attachments/assets/aa0c7ff0-4927-4c84-8242-654cbe473753" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.
