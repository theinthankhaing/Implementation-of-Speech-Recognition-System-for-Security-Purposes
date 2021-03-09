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
* Obtained 90% of recognition accuracy for the user by using Vector Quantization for recognition
________________________________________________________________________________________________________
## SetUp Environment
* MATLAB (>2018a version)
* Arduino Software
* [MATLAB support package for ARDUINO Hardware](https://www.mathworks.com/matlabcentral/fileexchange/47522-matlab-support-package-for-arduino-hardware)
_____________________________________________________________________________________________________________
## Hardware Requirement
* Arduino Uno
* HC - 05 Bluetooth Module
* 16 x 2 LCD Display
* Servo Motor (Tower Pro Sg 90 micro servo motor is used)
* Buzzer for alarm
* LEDs
* Potentiometer
* Power bank or Mobile phone charger
* PCB boards
* Wood
* Fibre card
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
## Recognition Accuracy with different codebook sizes in 20 testing times using VQ for 6 words with different syllables
### The word "Open"
![image](https://user-images.githubusercontent.com/50255936/110489185-25ef9580-812a-11eb-977b-be46d39d5b34.png)

### The word "Close"
![image](https://user-images.githubusercontent.com/50255936/110489223-2ee06700-812a-11eb-91db-12f7d4acfd2b.png)

### The word "Hello"
![image](https://user-images.githubusercontent.com/50255936/110489302-3e5fb000-812a-11eb-9f54-f38b0649cbee.png)

### The word "Camera"
![image](https://user-images.githubusercontent.com/50255936/110489366-4d466280-812a-11eb-98ce-d2e1703c9452.png)

### The word "Gallery"
![image](https://user-images.githubusercontent.com/50255936/110489429-5c2d1500-812a-11eb-8971-26bf13a0ef82.png)

### The word "Intelligence"
![image](https://user-images.githubusercontent.com/50255936/110489513-6b13c780-812a-11eb-9e31-8cc06fd05904.png)
__________________________________________________________________________
## Recognition Accuracy in 20 Testing Times using DTW
![image](https://user-images.githubusercontent.com/50255936/110490317-250b3380-812b-11eb-9c98-4de67695d26c.png)
_____________________________________________________________________________________
## Hardware Setup
![image](https://user-images.githubusercontent.com/50255936/110490720-8fbc6f00-812b-11eb-842a-8dfb9cdf1b6e.png)
_____________________________________________________________________
## How the system works
* Identifying the user is done by asking the user to type the name before recording the test signal
* Identifying the user, recording of the test signal, preprocessing, extracting features, matching features and assigning numbers to recognized speech output are done by MATLAB in PC
* The assigned number of recognied speech output from MATLAB is sent to Arduino by serial communication via Bluetooth
* The Arduio, which has already programmed, control devices such as LCD display, servo motor (for closing and opening door), buzzer and LED indicators
* Firstly, the user is identified by asking the user to type the name
* If the name is the same, speech recognition process will continue
* If the name is wrong or the test voice signal features are different from the database, the Red LED indicator and buzzer will turn on, LCD display will show that the user is the imposter and the door will be in close condition
* If the name is right and recognized output is "Open", Green LED indicator will turn on, LCD display will show "Welcome Home" and the door will open and it will close again after 3s of opening

![image](https://user-images.githubusercontent.com/50255936/110492357-10c83600-812d-11eb-969a-0ddf4cb61dc0.png)

### When the voice is different
![image](https://user-images.githubusercontent.com/50255936/110493608-bd0a1c80-812d-11eb-982f-46928b4e6710.png)

### When user's voice and trained voice are matched
![image](https://user-images.githubusercontent.com/50255936/110492860-76b4bd80-812d-11eb-82a6-dce6f09cddeb.png)

![image](https://user-images.githubusercontent.com/50255936/110493067-82a07f80-812d-11eb-9b45-171ac2a00629.png)

https://user-images.githubusercontent.com/50255936/110493627-c2fffd80-812d-11eb-9d85-9dbcbe91c5ad.mp4





