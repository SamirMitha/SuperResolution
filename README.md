# SuperResolution
EE 8108 Course Project

There are multiple ways to run the code. Either the Colab notebooks or the source code can be used. The recommended method is the Colab notebook, as Google Colab will handle all pypi dependencies. Additional dependencies may be required when using the source code.

## Colab Instructions (Recommended Method)
**Method 1: Single Image Upscaling and Visualization**

To run single image upscaling using all of the methods use demo.ipynb

Steps:
1. Open demo.ipynb in Google Colab
2. Switch the Google Colab Runtime to GPU
3. Run the notebook block

To change the image that is evaluated on, change the folder paths in the .yml and .json files located in /options/test

**Method 2: Batch Image Upscaling**

To run image upscaling on the entire test set use test.ipynb

Steps:
1. Open test.ipynb in Google Colab
2. Switch Colab Runtime to GPU
3. Run the notebook blocks sequentially to ensure all dependencies are present

To change the test set that is evaluated on, change the folder paths in the .yml and .json files located in /options/test

## Source Code Instructions
A GPU is required to run the code from source.

Steps:
1. Download the source code
2. Install the following dependencies (basicsr, torch, scipy, numpy, scikit-image, tqdm, pandas) or install from requirements.txt
3. Download test_set_one_folder from the download links below and place the contents (test_set_HR and test_set_LR folders) in the test_set folder
4. Download the pretrained models from the download links below and place the contents in the experiments/pretrained_models folder (ESRGAN, ESRGANplus, FA-SRGAN, SRGAN)
5. Edit the folder paths in the .yml and .json files located in /options/test to the downloaded models and test data paths
6. Super resolution images can be evaluated from the command line using the test scripts where the '-opt' argument will take the .yml or .json file from /options/test:
```
python codes/ESRGANplus/test.py -opt options/test/ESRGANplus/test_ESRGANplus.json
```
7. Results will be placed in the results folder

## Download Links
Pretrained Models: https://drive.google.com/drive/folders/1aeqtlMlqvaCaQ6TNwlEbjvPbNdCzTo9o?usp=sharing

Data: https://drive.google.com/drive/folders/1UIVXcTaLKLjetmhJXrrbJVSqQvha9y9C?usp=sharing

## References
**Paper References**

**Code References**

**Data References**
