# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2012.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 
% P.S.VISVANTH 212223050061

clc; % clear screen

clear all; % clear variables

close all; % close all figure windows


% INPUT SIGNAL-1

a = input('Enter the starting x(n): ');

x = input('Enter the x(n) sequence: ');

n = a:1:length(x)+a-1;


figure(1)

stem(n, x)

xlabel('Time')

ylabel('Amplitude')

title('Input Signal-1')


% INPUT SIGNAL-2

b = input('Enter the starting y(n): ');

y = input('Enter the y(n) sequence: ');

m = input('Enter the ending y(n): ');

n1 = b:1:length(y)+b-1;


figure(2)

stem(n1, y)

xlabel('Time')

ylabel('Amplitude')

title('Input Signal-2')


% DISCRETE AUTO-CORRELATED SIGNAL

out1 = xcorr(x, x);

n2 = a - m : 1 : length(out1) + a - m - 1;


figure(3)

stem(n2, out1)

xlabel('Time')

ylabel('Amplitude')


title('Discrete Auto Correlated Waveform')


% DISCRETE CROSS-CORRELATED SIGNAL

out2 = xcorr(x, y);

n3 = a - m : 1 : length(out2) + a - m - 1;


figure(4)

stem(n3, out2)

xlabel('Time')

ylabel('Amplitude')

title('Discrete Cross Correlated Waveform')

## OUTPUT:
<img width="1600" height="846" alt="image" src="https://github.com/user-attachments/assets/86fb74a5-d56a-4dd3-86fa-fef50093d729" />
## RESULT:
<img width="1280" height="647" alt="image" src="https://github.com/user-attachments/assets/e073664f-8f9f-49de-a54e-087d8152b3ee" />
