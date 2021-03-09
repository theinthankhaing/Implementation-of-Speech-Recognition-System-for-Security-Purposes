# Implementation of Speech Recognition System for Security Purposes
_______________________________________________________________________________________________
## Project Overview
* Implemented Speaker Dependent Isolated Word Speech Recognition based Securtiy System using MATLAB and Arduino UNO
* Recorded  6 words  with different syllables  
* Preprocessed these words using combination of zero-crossing rate (ZCR) and Energy Calculation
* Extracted features using Mel-Frequency Cepstral Coefficients (MFCC)
* Performed recognition using Vector Quantization (VQ) and Dynamic Time Warping (DTW)
* Built a prototype of house and  attached the door, which is automated by using ARDUINO controlling servo motor
* Sent the recognized output from MATLAB to ARDUINO using Bluetooth and  ARDUINO performed open and close of the door based on the recognition ouput
* Obtained 90% of recognition accuracy for the user
________________________________________________________________________________________________________
## SetUp Environment
* MATLAB (>2018a version)
* Arduino Software
* [MATLAB support package for ARDUINO Hardware](https://www.mathworks.com/matlabcentral/fileexchange/47522-matlab-support-package-for-arduino-hardware)
_____________________________________________________________________________________________________________
## Hardware Requirement
* Arduino Uno
* HC - 05 Bluetooth Module
* LCD Display
* Servo Motor (Tower Pro Sg 90 micro servo motor is used)
* Buzzer for alarm
* LEDs
______________________________________________________________________________________________________________________________
## System Block Diagram
![image](https://user-images.githubusercontent.com/50255936/110486989-20914b80-8128-11eb-8649-c4db3941f43c.png)
__________________________________________________________________________________________________________________
## Computation Steps of MFCC
![image](https://user-images.githubusercontent.com/50255936/110488405-669adf00-8129-11eb-8dc7-04fc65e83329.png)
_____________________________________________________________________________________________________________________________
## Overall Block Diagram of VQ system
![image](https://user-images.githubusercontent.com/50255936/110487490-97c6df80-8128-11eb-8118-3561573ca4e3.png)
_____________________________________________________________________________________________________________________________
## Overall Block Diagram of DTW system
![image](https://user-images.githubusercontent.com/50255936/110487602-b200bd80-8128-11eb-827f-2303b6cc6686.png)
_______________________________________________________________________________________________________________________________
