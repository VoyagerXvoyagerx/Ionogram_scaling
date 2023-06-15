# A Benchmark for Ionogram Autoscaling

## Install OpenMMLab repositories

If your device have access to the Internet:

```shell
pip install openmim
mim install "mmengine>=0.6.0"
mim install "mmcv>=2.0.0rc4,<2.1.0"
mim install "mmdet>=3.0.0rc6,<3.1.0"
pip install "mmsegmentation>=1.0.0"
mim install "mmyolo"
```

If your machine could not connect to the Internet, but the pip mirror:

Also install with pip:
```shell
pip install mmengine
pip install /home/zyj/mmcv-2.0.0-cp38-cp38-manylinux1_x86_64.whl    # use whl file
pip install "mmdet==3.0.0"
pip install "mmsegmentation>=1.0.0"
cd mmyolo
# Install albumentations
pip install -r requirements/albu.txt
# Install MMYOLO
mim install -v -e .
```

## Filetree
```shell
./
├── mmsegmentation
│   ├── configs
│   │   └── _ionoseg
│   ├── data
│   │   └── IonoSeg
│   │       ├── rgbimg
│   │       └── rgbmask
│   └── work_dirs
│       └── se4ionogram
└── mmyolo
    ├── configs
    │   └── custom_dataset
    │       ├── rtmdet
    │       ├── yolov5
    │       ├── yolov6
    │       └── yolov7
    ├── Iono4311
    │   ├── annotations
    │   ├── images
    │   └── labels
    ├── tools
    │   ├── analysis_tools
    │   ├── dataset_converters
    │   └── misc
    └── work_dirs
        ├── rtmdet_s_100e
        ├── rtmdet_tiny_100e
        ├── yolov5_m_100e
        ├── yolov5_s_100e
        ├── yolov6_l_100e
        ├── yolov6_m_100e
        ├── yolov6_s_100e
        ├── yolov7_tiny_100e
        └── yolov7_x_100e
```

## Train
Please refer to the document [A benchmark for ionogram real-time object detection based on MMYOLO](https://mmyolo.readthedocs.io/en/dev/recommended_topics/application_examples/ionogram_detection.html#)

## Ionogram scaling test

Please refer to [Ionogram_scaling.ipynb](./mmyolo/Ionogram_scaling.ipynb).

## Download
Dataset and models: [Ionogram_scaling_v0-dataset_models.zip](https://github.com/VoyagerXvoyagerx/Ionogram_scaling/releases/download/v0/Ionogram_scaling_v0-dataset_models.zip)