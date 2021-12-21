# SuperResolution
EE 8108 Course Project

There are multiple ways to run the code. Either the Colab notebooks or the source code can be used. The recommended method is the Colab notebook, as Google Colab will handle all pypi dependencies. Additional dependencies may be required when using the source code.

## Colab Instructions (Recommended Method)
**Method 1: Single Image Upscaling and Visualization (Recommended Method)**

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

[1]  	C. Ledig et al., "Photo-realistic single image super-resolution using a generative adversarial network," Proc. - 30th IEEE Conf. Comput. Vis. Pattern Recognition, CVPR 2017, vol. 2017-Janua, pp. 105–114, 2017, doi: 10.1109/CVPR.2017.19.

[2]  	J. Li, L. Wu, S. Wang, W. Wu, F. Song, and G. Zheng, "Super resolution image reconstruction of textile based on SRGAN," Proc. - 2019 IEEE Int. Conf. Smart Internet Things, SmartIoT 2019, pp. 436–439, 2019, doi: 10.1109/SmartIoT.2019.00078.

[3]  	X. Wang et al., "ESRGAN: Enhanced super-resolution generative adversarial networks," Lect. Notes Comput. Sci. (including Subser. Lect. Notes Artif. Intell. Lect. Notes Bioinformatics), vol. 11133 LNCS, pp. 63–79, 2019, doi: 10.1007/978-3-030-11021-5_5.

[4]  	"ESRGAN + : FURTHER IMPROVING ENHANCED SUPER-RESOLUTION GENERATIVE ADVERSARIAL NETWORK Nathana ¨ el Carraz Rakotonirina , Andry Rasoanaivo Laboratoire d' Informatique et Math' ematiques , Universit' e d' Antananarivo , Madagascar," pp. 3637–3641, 2020.

[5]  	Y. Yan et al., "Fine-grained Attention and Feature-sharing Generative Adversarial Networks for Single Image Super-Resolution," IEEE Trans. Multimed., vol. 14, no. 8, pp. 1–15, 2021, doi: 10.1109/TMM.2021.3065731.

[6]	Takano, Nao, and Gita Alaghband. “SRGAN: Training Dataset Matters,”  2019-March., https://arxiv.org/ftp/arxiv/papers/1903/1903.09922.pdf.

[7] 	Yang, W., Zhang, X., Tian, Y., Wang, W., Xue, J. H., & Liao, Q. (2019). Deep learning for single image super-resolution: A brief review. IEEE Transactions on Multimedia, 21(12), 3106-3121.

[8]	https://machinelearningmastery.com/what-are-generative-adversarial-networks-gans/

**Code References**

[1] https://pypi.org/project/basicsr/

[2] https://github.com/ncarraz/ESRGANplus

[3] https://github.com/Rainyfish/FASRGAN-and-Fs-SRGAN

**Data References**

[1]  	E. Agustsson and R. Timofte, "NTIRE 2017 Challenge on Single Image Super-Resolution: Dataset and Study," IEEE Comput. Soc. Conf. Comput. Vis. Pattern Recognit. Work., vol. 2017-July, pp. 1122–1131, 2017, doi: 10.1109/CVPRW.2017.150.

[2] https://cvnote.ddlee.cc/2019/09/22/image-super-resolution-datasets
