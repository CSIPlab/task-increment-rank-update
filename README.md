# Incremental Task Learning with Incremental Rank Updates

### [Paper](https://arxiv.org/abs/2207.09074) | [Code](https://github.com/CSIPlab/task-increment-rank-update/) | [Slides](https://github.com/CSIPlab/task-increment-rank-update/blob/main/doc/slides.pdf) | [Poster](https://github.com/CSIPlab/task-increment-rank-update/blob/main/doc/poster.pdf) | [Video](coming soon)

This repository is the official Pytorch implementation of *Incremental Task Learning with Incremental Rank Updates* in ECCV 2022.

[Incremental Task Learning with Incremental Rank Updates](https://arxiv.org/abs/2207.09074) </br>
Rakib Hyder , Ken Shao , Boyu Hou, Panos Markopoulos, Ashley Prater-Bennette, and [M. Salman Asif](https://intra.ece.ucr.edu/~sasif/) </br>
European Conference on Computer Vision (ECCV), 2022



## Requirements
```
numpy 1.20.3
matplotlib 3.4.3
torch 1.11.0
torchvision 0.12.0
tqdm 4.62.3
```

## Abstract
Incremental Task learning (ITL) is a category of continual learning that seeks to train a single network for multiple tasks (one after another), where training data for each task is only available during the training of that task. Neural networks tend to forget older tasks when they are trained for the newer tasks; this property is often known as catastrophic forgetting. To address this issue, ITL methods use episodic memory, parameter regularization, masking and pruning, or extensible network structures. In this paper, we propose a new incremental task learning framework based on low-rank factorization. In particular, we represent the network weights for each layer as a linear combination of several rank-1 matrices. To update the network for a new task, we learn a rank-1 (or low-rank) matrix and add that to the weights of every layer. We also introduce an additional selector vector that assigns different weights to the low-rank matrices learned for the previous tasks. We show that our approach performs better than the current state-of-the-art methods in terms of accuracy and forgetting. Our method also offers better memory efficiency compared to episodic memory- and mask-based approaches. 

![intro figure](./intro.png)
*An overview of our proposed method for continual learning via low-rank network updates. We first represent (and learn) the weight matrix (or tensor) for each layer as a product of low-rank matrices. To train a network for new tasks without forgetting the earlier tasks, we reuse the factors from the earlier tasks and add a new set of factors for the new task. Our experiments suggest that a rank-1 update is often sufficient for successful continual learning.*
## Citation
If you use this code in your research, please cite this paper: 
 
```
@inproceedings{hyder2022incremental,
  title={Incremental Task Learning with Incremental Rank Updates},
  author={Hyder, Rakib and Shao, Ken and Hou, Boyu and Markopoulos, Panos and Prater-Bennette, Ashley and Asif, M Salman},
  booktitle={Proceedings of the European Conference on Computer Vision (ECCV)},
  year={2022}
}
```
