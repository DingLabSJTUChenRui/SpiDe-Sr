This file contains three sections:
1. denoising network
2.Super-resolution network
3. images used for testing

The computer hardware (we used):
computer workstation equipped with an AMD Ryzen 5975WX CPU
NVIDIA RTX 3090 graphics processing card

Program Operating Environment:
Important Package	   Version
python	                   3.7.11
tensorflow	   1.15.0
torch	                   1.9.1+cu111
torchvision	   0.10.1+cu111
numpy	                   1.20.3
scipy	                   1.7.2
sklearn	                   0.0
scanpy	                   1.8.2
tensorflow-estimator   2.6.0
yaml	                   0.2.5
opencv-python	   4.5.4.58
pandas	                   1.3.4
imageio	                   2.12.0
scikit-image	   0.19.3

How to run the code:
Step 1: Change the address of the pretrained_model(test1w_epoch_500.pth) in the SpiDe-Sr-Code\De-Net\reference.py;
Step 2: Run reference.py to get the result;
Step 3: Run SpiDe-Sr-Code\Sr-Net\PrepareImages.m to adjust the image format;
Step 4: Open SpiDe-Sr-Code\Sr-Net\codes\test_Sr.py and change the correct addresses of the three .yml files in SpiDe-Sr-Code\Sr-Net\codes\options\test\;
Step 5: Run SpiDe-Sr-Code\Sr-Net\codes\test_Sr.py.

Dataset for testing: testImages

Estimated run time on the GPU: about 0.5 s/pic (The image size is 300 x 300 pixels.)

We demonstrated SpiDe-Sr respectively with fluorescent/metal dual-labeled cells, mouse and human tissues, resulting 18.95%/ 27.27%/ 21.16% increase in peak signal-to-noise ratio (PSNR).
