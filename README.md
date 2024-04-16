## SEKD

Multi-Level Feature Distillation via Channel Relational Graph

Image[TODO]

SE

Image[TODO]

## Installation



### Requirements



- Python >= 3.6
- Pytorch >= 1.7.0
- Torchvision >= 0.8.1
- Pycocotools 2.0.2

Follow the install instructions in detectron2, note that in this repo we use detectron2 commit version `ff638c931d5999f29c22c1d46a3023e67a5ae6a1`. Download [COCO](https://cocodataset.org/) dataset and `export DETECTRON2_DATASETS=$COCOPATH` to direct to COCO dataset. We prepare our pre-trained weights for training in `Student-Teacher` format, please follow the instructions in [Pretrained](https://github.com/tianxingjingge/SEKD/tree/master/projects/Distillation/pretrained)

## Running



We prepare training [configs](https://github.com/tianxingjingge/SEKD/tree/master/projects/Distillation/configs) following the detectron2 format. For **training** a Faster R-CNN R18-FPN student with a Faster R-CNN R50-FPN teacher on 8 GPUs:

```
./start_train.sh train projects/Distillation/configs/Distillation-FasterRCNN-R18-R50-dsig-1x.yaml
```



For **testing**:

```
./start_train.sh eval projects/Distillation/configs/Distillation-FasterRCNN-R18-R50-dsig-1x.yaml
```



For **debugging**:

```
./start_train.sh debugtrain projects/Distillation/configs/Distillation-FasterRCNN-R18-R50-dsig-1x.yaml
```

## TODO

We have only uploaded the code for the graph distillation part. The code for the spectral embedding part and more experimental details will be released gradually.