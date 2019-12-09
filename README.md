# BlendedMVS


## About the Dataset
[BlendedMVS](https://arxiv.org/abs/1911.10127) is a large-scale MVS dataset for generalized multi-view stereo networks. The dataset contains over 17k MVS training samples covering a variety of scenes, including architectures, sculptures and small objects. If you find the dataset useful for your research, please cite:
```
@article{yao2019blendedmvs,
  title={BlendedMVS: A Large-scale Dataset for Generalized Multi-view Stereo Networks},
  author={Yao, Yao and Luo, Zixin and Li, Shiwei and Zhang, Jingyang and Ren, Yufan and Zhou, Lei and Fang, Tian and Quan, Long},
  journal={arXiv:1911.10127 [cs.CV]},
  year={2019}
}
```

To visualize each scene via Altizure online platform, please go to ``https://www.altizure.com/project-model?pid=PID``, where ``PID`` is the unique project ID (e.g., ``5bfe5ae0fe0ea555e6a969ca``). All ``PID`` are listed in the ``all_list.txt`` file.

<iframe src="https://site.altizure.com/project/5bfe5ae0fe0ea555e6a969ca/model/embed#lights=off&amp;share=off&amp;view_mode=off" style="border:none;width:425px;height:300px"></iframe>

<iframe src="https://site.altizure.com/project/58eaf1513353456af3a1682a/model/embed#lights=off&amp;share=off&amp;view_mode=off" style="border:none;width:425px;height:300px"></iframe>

<iframe src="https://site.altizure.com/project/5c34529873a8df509ae57b58/model/embed#lights=off&amp;share=off&amp;view_mode=off" style="border:none;width:425px;height:300px"></iframe>

<iframe src="https://site.altizure.com/project/57f8d9bbe73f6760f10e916a/model/embed#lights=off&amp;share=off&amp;view_mode=off" style="border:none;width:425px;height:300px"></iframe>

## Dataset Structure:

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
├── ...                         -
└── PID112                      
```

``PID`` here is the unique project ID listed in the ``all_list.txt`` file. For file formats of other training inputs, users may refer to [MVSNet](https://github.com/YoYo000/MVSNet) for more details. 


## TODO: 
1. Dataset license.
2. Dataset download link.
3. Training and validation codes.

The dataset will be uploaded soon once the license is determined.
