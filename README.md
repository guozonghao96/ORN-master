# ORN-pytorch
Baseline code for Oriented Response Networks[[Paper]](https://arxiv.org/pdf/1701.01833)

Please follow the instruction below to install it and run the experiment demo.

### Prerequisites
* Linux (tested on ubuntu 16.04LTS)
* NVIDIA-1080ti + CUDA-9.0 + CuDNN7.0
* Pytorch-1.0.0 + Torchvision

### Getting started
1.install the dependencies (required by the demo code):
   * [pillow](https://python-pillow.org): `pip install Pillow`

2. clone the this branch: 

  ```bash
  # git version must be greater than 1.9.10
  git clone https://github.com/SDL-GuoZhao/ORN-master
  ```
  
3.setup orn:

  ```bash
  cd ORN-pytorch
  export DIR=$(pwd)
  python setup.py develop
  ```

4. run the MNIST-Variants demo:

  ```bash
  cd $DIR
  # train baseline CNN on MNIST
  python main.py --net cnn --dataset MNIST
  # train ORN on MNIST
  python main.py --net orn --dataset MNIST
  # train baseline CNN on MNIST-rot
  python main.py --net cnn --dataset MNIST-rot
  # train ORN on MNIST-rot
  python main.py --net orn --dataset MNIST-rot

## Citation 
If you use the code in your research, please cite:
```bibtex
@INPROCEEDINGS{Zhou2017ORN,
    author = {Zhou, Yanzhao and Ye, Qixiang and Qiu, Qiang and Jiao, Jianbin},
    title = {Oriented Response Networks},
    booktitle = {CVPR},
    year = {2017}
}
```   
