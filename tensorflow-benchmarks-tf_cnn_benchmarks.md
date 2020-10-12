# benchmark tensorflow cnn network with fp16 and fp32

## contents:
- [setup](#setup)
- [fp32](#fp32)
- [fp16](#fp16)

## setup
GPU: GTX 2080ti * 8
docker image: nvidia/cuda:10.1-cudnn7-devel-ubuntu18.04
tensorflow version: 2.3

## fp32
### command
`python tf_cnn_benchmarks.py --use_fp32`


## fp16
### command 
`python tf_cnn_benchmarks.py --use_fp16`
