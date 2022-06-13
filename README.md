# Cylindrical and Asymmetrical 3D Convolution Networks for LiDAR Segmentation

## Installation
### Requirements
- PyTorch == 1.10 
- yaml
- Cython
- [torch-scatter](https://github.com/rusty1s/pytorch_scatter)
- [spconv](https://github.com/traveller59/spconv) (tested with spconv==1.2.1 and cuda==11.1)

## Data Preparation

### SemanticKITTI
```
./
├── 
├── ...
└── path_to_data_shown_in_config/
    ├──sequences
        ├── 00/           
        │   ├── velodyne/	
        |   |	├── 000000.bin
        |   |	├── 000001.bin
        |   |	└── ...
        │   └── labels/ 
        |       ├── 000000.label
        |       ├── 000001.label
        |       └── ...
        ├── 08/ # for validation
        ├── 11/ # 11-21 for testing
        └── 21/
	    └── ...
```

## Training
1. modify the config/semantickitti.yaml with your custom settings. 
2. modify the pytorch_device which you will use in "train_cylinder_asym.py"
3. train the network by running "python train_cylinder_asym.py"
