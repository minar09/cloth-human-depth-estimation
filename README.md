## Disclaimer
This is a slighly modified version of original [Deep_human](https://github.com/sfu-gruvi-3dv/deep_human) repository, for testing with custom sized custom images of clothing and human.

# Deep_human (Clothing/Human Depth Estimation)
Code for iccv2019 paper "A Neural Network for Detailed Human Depth Estimation from a Single Image" (Under construction)

Requirements<br/>
CUDA 9.0<br/>
OpenCV 3.2<br/>
Python 3.5<br/>
tensorflow >= 1.6.0<br/>
numpy<br/>


Preparation<br/>
Download model from https://drive.google.com/open?id=16CWE_1tx3IfWDucfkTmOnRPylvv2ekRM<br/>
mkdir models<br/>
tar -xf models.tar -C models<br/>

Demo:<br/>
run python demo.py <br/>
model and test dir can be set in file params/params_iccv.py<br/>
results will be saved in output/<br/>

The input image should be 256x256 sized and tightly cropped image, and the network predict the depth for all pixels, the computed depth image needs to be cropped by silhouette, you can use some off-the-shelf tools(e.g. MaskRCNN) to get the foreground region, or use the segmentation result obtained from segmentation-net.<br/>

Training data can be downloaded here:<br/>
https://drive.google.com/file/d/18tXcv68ke3ln0ITE-DbjnvIBiQV1QYbb/view?usp=sharing<br/>

References:<br/>
@InProceedings{Tang_2019_ICCV,
author = {Tang, Sicong and Tan, Feitong and Cheng, Kelvin and Li, Zhaoyang and Zhu, Siyu and Tan, Ping},
title = {A Neural Network for Detailed Human Depth Estimation From a Single Image},
booktitle = {The IEEE International Conference on Computer Vision (ICCV)},
month = {October},
year = {2019}
}



