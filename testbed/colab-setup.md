First draft @ 2024 - March

Colab with T4 and V100 GPU



```
!nvidia-smi
!nvcc --version
!gcc --version
```



```shell
!git clone https://github.com/NVIDIA/cuda-samples
```



```shell
%cd /content/cuda-samples/Samples/1_Utilities/deviceQuery
!ls -lrt
!make
```



```shell
!./deviceQuery
```



```shell
%cd /content/cuda-samples/Samples/1_Utilities/bandwidthTest
!ls -lrt
!make
```



```shell
!./bandwidthTest
```



```shell
%cd /content/cuda-samples/Samples/1_Utilities/topologyQuery
!ls -lrt
!make
```



```shell
!./topologyQuery
```



```shell
%cd /content/cuda-samples/Samples/6_Performance/LargeKernelParameter
!ls -lrt
!make
```



```shell
!./LargeKernelParameter
```



```shell
%cd /content/cuda-samples/Samples/6_Performance/UnifiedMemoryPerf
!ls -lrt
!make
```



```shell
!./UnifiedMemoryPerf
```



```shell
%cd /content/cuda-samples/Samples/6_Performance/alignedTypes
!ls -lrt
!make
```



```shell
!./alignedTypes
```



```shell
%cd /content/cuda-samples/Samples/6_Performance/transpose
!ls -lrt
!make
```



```shell
!./transpose
```



