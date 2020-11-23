# KITTI-to-VOC

Support conversion from:

- KITTI
- KITTI tracking
- Pascal VOC

to:

- Pascal VOC
- KITTI

## Usage
Flags:
- `--from-path`: Source dataset
- `--from`: Type of source dataset:
    -   `kitti`: KITTI
    -   `voc`: Pascal VOC
- `--to-path`: Destination path
- `--to`: Type of destination dataset.
    - `kitti`: KITTI
    - `voc`: Pascal VOC

## Setup and Run 
### KITTI datasets
- Create `./KITTI-to-VOC/datasets/KITTI` folder 
- Place `./training/image_2` and `./training/label_2` into `./KITTI-to-VOC/datasets/KITTI`
### Create `train.txt` file for KITTI
``` markdown
$ cd datasets/KITTI && ls -1 training/image_2 | cut -d. -f1 > train.txt
```
### Convert KITTI datasets to Pascal VOC
``` markdown 
$ python converter/main.py --from kitti --from-path datasets/KITTI --to voc --to-path datasets
```

## Acknowledge
This repository is a fork from [vod-converter](https://github.com/umautobots/vod-converter) but has some changes to be compatible with both Python 2 and 3
