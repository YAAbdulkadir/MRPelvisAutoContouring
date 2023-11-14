# MRPelvisAutoContouring
## MIM Extensions for Autocontouring of Images of the Pelvis from a 0.35T MR System
This repository contains the java implementation of [`MIM Extensions`](https://www.mimsoftware.com/) for autocontouring of MR images of the pelvis used for radiotherapy. There are four separate extensions to autocontour the femoral heads (left and right), bladder and rectum. There are separate deep learning models for each OAR used by the corresponding extensions. The models were trained in python using tensorflow and the [UNET++](https://ieeexplore.ieee.org/abstract/document/8932614) model architecture. The details of the implementation within a clinical workflow for research purposes can be found in our [`publication`](https://aapm.onlinelibrary.wiley.com/doi/full/10.1002/mp.16676). 

## Setup and Build Instructions
Please follow the setup instructions provided by [`MIM Software`](https://www.mimsoftware.com/) under the [`MIM Extensions`](https://www.mimsoftware.com/portal/training/extensions) tab in the knowledge center. MIM account is required to access this page. 

## Downloading the Models
The models can be downloaded from [here](https://drive.google.com/drive/folders/1jiswRsa59ADvz7HG5iFQ_KxpS1M2I_zW?usp=drive_link). There are six models in the linked drive. Four of the models were trained using [`UNET++`]() (`model_bladder_10_21`, `model_femr_lt_10_17`, `model_femr_rt_10_16`, `model_rectum_11_16`). The other two models (`bladder_full_3D` and `rectum_cropped_3d`) were trained using the [`VNET`](https://ieeexplore.ieee.org/abstract/document/7785132) model architecture for 3D segmentation. 

## Reference
If you use all or parts of this implementation or the models provided, please cite our [`Medical Physics paper`](https://aapm.onlinelibrary.wiley.com/doi/full/10.1002/mp.16676). 
> **Abdulkadir, Y, Luximon, D, Morris, E, et al. Human factors in the clinical implementation of deep learning-based automated contouring of pelvic organs at risk for MRI-guided radiotherapy. Med Phys. 2023; 50: 5969–5977. https://doi.org/10.1002/mp.16676**

Please also cite the [`UNET++ paper`](https://ieeexplore.ieee.org/abstract/document/8932614).
> **Z. Zhou, M. M. R. Siddiquee, N. Tajbakhsh and J. Liang, "UNet++: Redesigning Skip Connections to Exploit Multiscale Features in Image Segmentation," in IEEE Transactions on Medical Imaging, vol. 39, no. 6, pp. 1856-1867, June 2020, doi: 10.1109/TMI.2019.2959609.**

If you use the models trained using [`VNET`](https://ieeexplore.ieee.org/abstract/document/7785132), please cite their paper.
> **F. Milletari, N. Navab and S. -A. Ahmadi, "V-Net: Fully Convolutional Neural Networks for Volumetric Medical Image Segmentation," 2016 Fourth International Conference on 3D Vision (3DV), Stanford, CA, USA, 2016, pp. 565-571, doi: 10.1109/3DV.2016.79.**

## Contacts
If you have any questions or suggestions, please contact me at Yasinaabdulkadir@gmail.com