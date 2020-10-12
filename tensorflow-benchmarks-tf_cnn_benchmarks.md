# benchmark tensorflow resnet50 with fp16 and fp32

## contents:
- [setup](#setup)
- [fp32](#fp32)
- [fp16](#fp16)
- [Observation](#observation)

## setup
- GPU: GTX 2080ti * 8
- docker image: nvidia/cuda:10.1-cudnn7-devel-ubuntu18.04
- tensorflow version: 2.3
- script: [tensorflow/benchmarks](https://github.com/tensorflow/benchmarks/tree/master/scripts/tf_cnn_benchmarks) (no longer maintained)

## fp32
- command: `python tf_cnn_benchmarks.py --num_gpus=1 --batch_size=32 --model=resnet50`
- result:
  - throughput:
```
total images/sec: 281.12
```

## fp16 benchmark
- command: `python tf_cnn_benchmarks.py --num_gpus=1 --batch_size=32 --model=resnet50 --use_fp16`
- result:
  - throughput:
```
total images/sec: 605.40
```

## Observation:
fp16/fp32 throughput ratio is 2.15x 
