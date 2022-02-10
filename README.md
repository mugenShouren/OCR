# OCR
## Training
Trainer notebook holds everything from:
- Preprocessing
    - Data cleaning
    - Skewing the data
    - Setting up frames for the input training images
-  Model Training
    - We are training a RCNN to learn the patterns between the consecutice words(The model can be enhanced to read Hand written text)
    - Network Architecture is also defined here
- Post Processing
    - The ROI is marked on the images
    - The detected text is marked over the images 

Model was trained on 135000 image samples.
## ROI 
For ROI detection we have used [CRAFT API](https://github.com/clovaai/CRAFT-pytorch). The detected ROI is then passsed through out model and letters are classfied and text is detected.
## Prediction
The prediction file loads the saved weights into the model (Netwrod architecture), and provides prediction for the images present in the input directory.

The model was tested on 15000 images and an accuracy of 96% was achieved.

## Refrences
- MSRA Text Detection 500 Database (MSRA-TD500) by Cong Yao (Huazhong University of Science and Technology)
- THE MNIST DATABASE of handwritten digits by Yann LeCun, Courant Institute, NYU, Corinna Cortes, Google Labs, New York and Christopher J.C. Burges, Microsoft Research, Redmond.
- KAIST Scene Text Database by Prof. Jin Hyung Kim, Artificial Intelligence and Pattern Recognition Lab, Computer Science Department of KAIST, KOREA
- NEOCR: Natural Environment OCR Dataset by Robert Nagy, University of Erlangen-Nuremberg
- An End-to-End Trainable Neural Network for Image-based Sequence Recognition and Its Application to Scene Text Recognition Baoguang Shi, Xiang Bai and Cong Yao School of Electronic Information and Communications Huazhong University of Science and Technology, Wuhan, China.
