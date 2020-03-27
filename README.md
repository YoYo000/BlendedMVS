# BlendedMVS


## About the Dataset
[BlendedMVS](https://arxiv.org/abs/1911.10127) is a large-scale MVS dataset for generalized multi-view stereo networks. The dataset contains over 17k MVS training samples covering a variety of scenes, including architectures, sculptures and small objects. If you find the dataset useful for your research, please cite:
```
@article{yao2020blendedmvs,
  title={BlendedMVS: A Large-scale Dataset for Generalized Multi-view Stereo Networks},
  author={Yao, Yao and Luo, Zixin and Li, Shiwei and Zhang, Jingyang and Ren, Yufan and Zhou, Lei and Fang, Tian and Quan, Long},
  journal={Computer Vision and Pattern Recognition (CVPR)},
  year={2020}
}
```

To visualize each scene via Altizure online platform, please go to ``https://www.altizure.com/project-model?pid=PID``, where ``PID`` is the unique project ID (e.g., ``5bfe5ae0fe0ea555e6a969ca``). All ``PID`` are listed in the ``all_list.txt`` file.

<a href="https://www.altizure.com/project-model?pid=5bfe5ae0fe0ea555e6a969ca"><img src="doc/cover0.gif" width="425"></a> <a href="https://www.altizure.com/project-model?pid=58eaf1513353456af3a1682a"><img src="doc/cover1.gif" width="425"></a>

<a href="https://www.altizure.com/project-model?pid=5c34529873a8df509ae57b58"><img src="doc/cover2.gif" width="425"></a> <a href="https://www.altizure.com/project-model?pid=57f8d9bbe73f6760f10e916a"><img src="doc/cover3.gif" width="425"></a>


## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Dataset" property="dct:title" rel="dct:type">BlendedMVS</span> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>!!!


## Download

We provide both high-resolution and low-resolution training data in BlendedMVS dataset. 

* High-resolution set: Image and depth map resolutions are set to 2048 x 1536.
* Low-resolution set: Image and depth map resolutions are set to 768 x 576. 

Currently the [low-resolution set](https://drive.google.com/open?id=1ilxls-VJNvJnB7IaFj7P0ehMPr7ikRCb) is provided for MVSNet training, the high-resolution set is provided upon request.

## Dataset Structure

BlendedMVS dataset adopts MVSNet input format. The dataset structure is listed below:
 
```
BlendedMVS                      
├── all_list.txt                
├── training_list.txt           
├── validation_list.txt         
├── PID0                        
│   ├── blended_images          
│   │	├── 00000000.jpg        
│   │	├── 00000001.jpg        
│   │	└── ...                 
│   ├── cams                    
│   │  	├── 00000000_cam.txt    
│   │  	├── 00000001_cam.txt    
│   │  	└── ...                 
│   ├── rendered_depth_maps     
│   │  	├── 00000000.pfm        
│   │  	├── 00000001.pfm        
│   │  	└── ...                 
│   └── pair.txt                
├── PID1                        
├── ...                         
└── PID112                      
```

``PID`` here is the unique project ID listed in the ``all_list.txt`` file. For file formats of other training inputs, users may refer to [MVSNet](https://github.com/YoYo000/MVSNet) for more details. 

## Usage
Users may refer to [MVSNet](https://github.com/YoYo000/MVSNet) for training/validating MVSNet/R-MVSNet using BlendedMVS dataset.

## Note 

* Online augmentation should be implemented by users themselves. An example for tensorflow users could be found in [MVSNet](https://github.com/YoYo000/MVSNet).
* The number of selected source images for a given reference image might be smaller than 10 (when parsing pair.txt).
* The `depth_min` in ground truth cameras might be smaller or equal to zero (when parsing *_cam.txt).

## TODO: 
* Stand alone validation scripts.
* Download link for textured mesh models
* Download link for input images and rendered images
