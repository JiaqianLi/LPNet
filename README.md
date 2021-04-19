
This repository is an official PyTorch implementation of the paper **"Luminance-aware Pyramid Network for Low-light Image Enhancement"** from **IEEE Transactions on Multimedia, 2020**.

If you find our work useful in your research or publication, please cite our work:

J. Li, J. Li, F. Fang, F. Li and G. Zhang, "Luminance-aware Pyramid Network for Low-light Image Enhancement," in IEEE Transactions on Multimedia, doi: 10.1109/TMM.2020.3021243.

```
@ARTICLE{9186194,
  author={J. {Li} and J. {Li} and F. {Fang} and F. {Li} and G. {Zhang}},
  journal={IEEE Transactions on Multimedia}, 
  title={Luminance-aware Pyramid Network for Low-light Image Enhancement}, 
  year={2020},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/TMM.2020.3021243}}
```


## Environment
* Python 3.6
* PyTorch = 0.4
* numpy
* skimage
* imageio
* matplotlib
* tqdm
* cv2


## Quickstart (Demo)
We give an example command for train and test the code in "LPNet/demo.sh".

### Test the model
You can test our image enhancement algorithm with your images. Place your images in "TestCode/LR/LRBI/" folder. (like "TestCode/LR/LRBI/eval15") We support **png** and **jpeg** files.

Baseline models are in "LPNet/TestCode/model/xxx_baseline.pt". There are three model files corresponding to the three datasets of LOL, MIT5K, and SID.

Run the script in "TestCode/code" folder. Before you run the demo, please uncomment the appropriate line in "demo.sh" that you want to execute.
```bash
cd TestCode/code       # You are now in */LPNet/TestCode/code
sh demo.sh
```
### Retain the model
If you want to retrain the model, place the training dataset in "dataset/DIV2K/DIV2K_train_LR_bicubic/X1/" folder. (like "dataset/DIV2K/DIV2K_train_LR_bicubic/X1/xxx.png") We support **png** files as default. If you want to use the **jpeg** files, you should modify the code in "LPNet/data/srdata.py" for the corresponding suffix.

Run the code in root directory (like "LPNet/"). Before you run the demo, please uncomment the appropriate line in ```demo.sh``` that you want to execute.
```bash
cd LPNet       # You are now in */LPNet
sh demo.sh
```

## Acknowledgements
Our code architecture is inspired by the open repository at https://github.com/sanghyun-son/EDSR-PyTorch.


