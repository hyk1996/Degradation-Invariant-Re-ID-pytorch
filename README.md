# Degradation-Invariant-Re-ID-pytorch
This is the official code repository for *Learning Degradation-Invariant Representation for Robust Real-World Person Re-Identification*.

The training code will be released soon.

## Dataset
Download the MLR-CUHK03 dataset and reorganize the folders as follows:<br>
```
├── resolution-reid
│   ├── MLR-CUHK03
│       ├── train
│       ├── val
│       ├── gallery
│       ├── query
│           ├── 0020
│               ├── 00020_c0_00000.jpg
│               ├── ...
```

## Model
Trained model are provided. You may download it from [Google Drive](https://drive.google.com/drive/folders/1anHkFyEJaQWRsbkmVFjZX9y71zzb7rCs?usp=sharing), then move the `outputs` folder to your project's root directory.

## Dependencies
* Python 3.8
* PyTorch 1.8

## Usage
### 1. Re-ID Performance
**Command (Evaluation on the MLR-CUHK03 dataset):**

```
python test_reid.py --dataset mlr_cuhk03 --data_root path/to/resolution-reid/
```

**Results:**

`Rank@1=91.8  Rank@5=98.6  Rank@10=99.3  Rank@20=99.5  mAP=94.8`

### 2. Visualization
**Command:**
```
python visualize.py
```

**Visualization results of Degradation Swapping:**

<img src="https://github.com/hyk1996/Degradation-Invariant-Re-ID-pytorch/blob/main/demo/viz_swap.jpg" width="300px">

**Visualization results of Degradation Memory Replay:**

<img src="https://github.com/hyk1996/Degradation-Invariant-Re-ID-pytorch/blob/main/demo/viz_replay.jpg" width="500px">
