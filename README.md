<h1 align="center"> AdaLip : AN OPTIMIZATION-BASED FRAMEWORK FOR ADVERSARIAL DEFENCE OF GRAPH NEURAL NETWORKS VIA
ADAPTIVE LIPSCHITZ REGULARIZATION</h1> 
<p align="center"> <a href="https://scholar.google.com/citations?user=MRJqKywAAAAJ&hl=en&oi=ao" target="_blank id="website">Vipul Kumar Singh </a>, <a href="https://github.com/SarathMohanIITD" target="_blank id="website">Sarath Mohan </a>, <a href="https://sites.google.com/view/sandeepkr/home" target="_blank id="website">Sandeep Kumar</a></p>
<p align="center">  <a href="[https://misn.iitd.ac.in/](https://openreview.net/forum?id=Xsrsj3cne4)" target="_blank id="website">Paper </a>



An Optimization-Based Framework for Adversarial Defence of Graph Neural Networks Via Adaptive Lipschitz Regularization

## Abstract 
- Graph Neural Networks (GNNs) have exhibited exceptional performance across diverse application domains by harnessing the inherent interconnectedness of data. However, the emergence of adversarial attacks targeting GNNs poses a substantial and pervasive threat, compromising their overall performance and learning capabilities. While recent efforts have focused on enhancing GNN robustness from both data and architectural perspectives, more attention should be given to overall network stability in the face of input perturbations. Prior methods addressing network stability have routinely employed gradient normalization as a fundamental technique. This study introduces a unifying approach, termed as AdaLip, for adversarial training of GNNs through an optimization framework that leverages the explicit Lipschitz constant. By seamlessly integrating graph denoising and network regularization, AdaLip offers a comprehensive and versatile solution, extending its applicability and enabling robust regularization for diverse neural network architectures. Further, we develop a provably convergent iterative algorithm, leveraging block majorization-minimization, graph learning, and alternate minimization techniques to solve the proposed optimization problem. Simulation results on real datasets demonstrate the efficacy of AdaLip over state-of-the-art defence methods across diverse classes of poisoning attacks. On select datasets, AdaLip demonstrates GCN performance improvements of up to 20% against modification attacks and approximately 10% against injection attacks. Remarkably, AdaLip achieves a similar performance gain on heterophily graph datasets.

## Requirements
Refer https://github.com/DSE-MSU/DeepRobust/blob/master/requirements.txt for requirements

## Installation
To run the code, first you need to install DeepRobust:
```
pip install deeprobust
```
Or you can clone it and install from source code:
```
git clone https://github.com/DSE-MSU/DeepRobust.git
cd DeepRobust
python setup.py install
```

## Run the code
After installation, you can clone this repository or you can use the demo notebook here [COLAB](https://github.com/SarathMohanIITD/RS-GNN/blob/main/RS_GNN.ipynb)
```
https://github.com/SarathMohanIITD/RS-GNN
cd RS-GNN
!python train.py --two_stage y --bound 0.5 --seed 30 --dataset citeseer  --attack meta --ptb_rate 0.25 --epochs 200 --epochs_pre 400 --alpha 1.0  --gamma 1.0 --beta 0.3 --lr_optim 1e-2 --lr 1e-3
```
<!-- [colab]: <https://colab.research.google.com/assets/colab-badge.svg>
[RS-GNN]: <https://github.com/SarathMohanIITD/RS-GNN/blob/main/RS_GNN.ipynb> -->

## Acknowledgements
The code is based on :
- DeepRobust [(https://github.com/DSE-MSU/DeepRobust)](https://github.com/DSE-MSU/DeepRobust)
- [Pro-GNN](https://github.com/ChandlerBang/Pro-GNN)
- [RWL-GNN](https://github.com/Bharat-Runwal/RWL-GNN)


