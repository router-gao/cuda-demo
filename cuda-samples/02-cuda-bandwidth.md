### T4 bandwidth output

```shell
ecs-user@iZ2ze59179jmm5xn1azmthZ:/tmp/cuda-samples/Samples/1_Utilities/bandwidthTest$ ./bandwidthTest
[CUDA Bandwidth Test] - Starting...
Running on...


Device 0: Tesla T4
Quick Mode


Host to Device Bandwidth, 1 Device(s)
PINNED Memory Transfers
   Transfer Size (Bytes)        Bandwidth(GB/s)
   32000000                     9.7


Device to Host Bandwidth, 1 Device(s)
PINNED Memory Transfers
   Transfer Size (Bytes)        Bandwidth(GB/s)
   32000000                     11.1


Device to Device Bandwidth, 1 Device(s)
PINNED Memory Transfers
   Transfer Size (Bytes)        Bandwidth(GB/s)
   32000000                     239.6


Result = PASS

NOTE: The CUDA Samples are not meant for performance measurements. Results may vary when GPU Boost is enabled.
```



### A100 bandwidth output

```shell
[CUDA Bandwidth Test] - Starting...
Running on...

 Device 0: NVIDIA A100-SXM4-40GB
 Quick Mode

 Host to Device Bandwidth, 1 Device(s)
 PINNED Memory Transfers
   Transfer Size (Bytes)	Bandwidth(GB/s)
   32000000			12.3

 Device to Host Bandwidth, 1 Device(s)
 PINNED Memory Transfers
   Transfer Size (Bytes)	Bandwidth(GB/s)
   32000000			13.2

 Device to Device Bandwidth, 1 Device(s)
 PINNED Memory Transfers
   Transfer Size (Bytes)	Bandwidth(GB/s)
   32000000			1157.5

Result = PASS

NOTE: The CUDA Samples are not meant for performance measurements. Results may vary when GPU Boost is enabled.
```



### V100 bandwidth output

```shell
ecs-user@iZ2ze59179jmm5xn1azmthZ:/tmp/cuda-samples/Samples/1_Utilities/bandwidthTest$


[CUDA Bandwidth Test] - Starting...
Running on...


Device 0: Tesla V100-SXM2-16GB
Quick Mode


Host to Device Bandwidth, 1 Device(s)
PINNED Memory Transfers
   Transfer Size (Bytes)        Bandwidth(GB/s)
   32000000                     9.6


Device to Host Bandwidth, 1 Device(s)
PINNED Memory Transfers
   Transfer Size (Bytes)        Bandwidth(GB/s)
   32000000                     11.4


Device to Device Bandwidth, 1 Device(s)
PINNED Memory Transfers
   Transfer Size (Bytes)        Bandwidth(GB/s)
   32000000                     739.8


Result = PASS


NOTE: The CUDA Samples are not meant for performance measurements. Results may vary when GPU Boost is enabled.
```



