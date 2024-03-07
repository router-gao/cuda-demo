![memory-hierarchy-in-gpus-2](https://github.com/router-gao/cuda-demo/assets/144886373/62e2136e-3da6-4a2a-a10a-1647d5b26851)

### T4 Single-Precision calculation ( 8.1TFLOPS ) 

The single-precision performance of the Tesla T4 based on the deviceQuery output, we can use the formula provided earlier:


$$
Performance (TFLOPS)=Core Count×Core Clock Frequency (GHz)×Operations Per Clock Cycle
$$
From the deviceQuery output, we have:

- **Core Count**: 2560 CUDA Cores
- **GPU Max Clock rate**: 1590 MHz (1.59 GHz)
- **Operations Per Clock Cycle**: For NVIDIA GPUs, it's generally 2 operations per cycle for single-precision (FP32) calculations.

Let's plug these values into the formula to calculate the Tesla T4's single-precision performance.

Based on the given information from the deviceQuery output and the calculation formula, the Tesla T4's single-precision performance is approximately 8.14 TFLOPS.



### CUDA Samples output - deviceQuery

```shell
ecs-user@iZ2ze59179jmm5xn1azmthZ:/tmp/cuda-samples/Samples/1_Utilities/deviceQuery$ ./deviceQuery
./deviceQuery Starting...


CUDA Device Query (Runtime API) version (CUDART static linking)


Detected 1 CUDA Capable device(s)


Device 0: "Tesla T4"
  CUDA Driver Version / Runtime Version          12.0 / 12.0
  CUDA Capability Major/Minor version number:    7.5
  Total amount of global memory:                 15102 MBytes (15835398144 bytes)
  (040) Multiprocessors, (064) CUDA Cores/MP:    2560 CUDA Cores
  GPU Max Clock rate:                            1590 MHz (1.59 GHz)
  Memory Clock rate:                             5001 Mhz
  Memory Bus Width:                              256-bit
  L2 Cache Size:                                 4194304 bytes
  Maximum Texture Dimension Size (x,y,z)         1D=(131072), 2D=(131072, 65536), 3D=(16384, 16384, 16384)
  Maximum Layered 1D Texture Size, (num) layers  1D=(32768), 2048 layers
  Maximum Layered 2D Texture Size, (num) layers  2D=(32768, 32768), 2048 layers
  Total amount of constant memory:               65536 bytes
  Total amount of shared memory per block:       49152 bytes
  Total shared memory per multiprocessor:        65536 bytes
  Total number of registers available per block: 65536
  Warp size:                                     32
  Maximum number of threads per multiprocessor:  1024
  Maximum number of threads per block:           1024
  Max dimension size of a thread block (x,y,z): (1024, 1024, 64)
  Max dimension size of a grid size    (x,y,z): (2147483647, 65535, 65535)
  Maximum memory pitch:                          2147483647 bytes
  Texture alignment:                             512 bytes
  Concurrent copy and kernel execution:          Yes with 3 copy engine(s)
  Run time limit on kernels:                     No
  Integrated GPU sharing Host Memory:            No
  Support host page-locked memory mapping:       Yes
  Alignment requirement for Surfaces:            Yes
  Device has ECC support:                        Enabled
  Device supports Unified Addressing (UVA):      Yes
  Device supports Managed Memory:                Yes
  Device supports Compute Preemption:            Yes
  Supports Cooperative Kernel Launch:            Yes
  Supports MultiDevice Co-op Kernel Launch:      Yes
  Device PCI Domain ID / Bus ID / location ID:   0 / 0 / 7
  Compute Mode:
     < Default (multiple host threads can use ::cudaSetDevice() with device simultaneously) >


deviceQuery, CUDA Driver = CUDART, CUDA Driver Version = 12.0, CUDA Runtime Version = 12.0, NumDevs = 1
Result = PASS
ecs-user@iZ2ze59179jmm5xn1azmthZ:/tmp/cuda-samples/Samples/1_Utilities/deviceQuery$
```



### Device Information

- **CUDA Driver Version / Runtime Version**: Indicates the version of the CUDA Driver and the CUDA Runtime environment, both are version 12.0. This ensures compatibility with CUDA 12.0 features and functionalities.
- **CUDA Capability Major/Minor version number**: 7.5. This figure denotes the compute capability of the GPU, which affects its general architecture, features, and the types of CUDA operations it supports. A compute capability of 7.5 indicates support for a variety of modern CUDA features, including enhanced parallelism and efficiency.

### GPU Architecture and Cores

- **Total amount of global memory**: **15,102 MB.** This is the total available memory for storing data such as variables and arrays used by programs running on the GPU.
- **Multiprocessors, CUDA Cores/MP**: **The T4 has 40 Multiprocessors, with 64 CUDA Cores per Multiprocessor, totaling 2560 CUDA Cores.** These cores perform the actual computation work, including integer and floating-point operations. The architecture does not explicitly separate cores by type (INT32, FP32, FP64, Tensor Cores) in this summary. However, the Tesla T4 is known to have Tensor Cores designed specifically for AI and deep learning computations.

### Performance Metrics

- **GPU Max Clock rate**: **1590 MHz. This is the maximum operating frequency of the GPU, which influences its computation speed.**
- **Memory Clock rate**: 5001 MHz. The speed at which the GPU's memory operates, affecting data transfer rates to and from the global memory.
- **Memory Bus Width**: **256-bit.** This width determines the amount of data that can be transferred to the GPU's memory in a single operation, impacting overall memory bandwidth.
- **L2 Cache Size**: **4,194,304 bytes (4 MB).** The size of the GPU's L2 cache, which helps improve performance by storing frequently accessed data closer to the compute cores.

### Computational Limits

- **Total amount of shared memory per block**: **49,152 bytes.** This memory is shared among threads in a block, facilitating fast data exchange and cooperation.
- **Total number of registers available per block**: **65,536.** Registers are fast memory locations available to each thread. More registers allow for more complex or numerous local variables per thread.
- **Maximum number of threads per multiprocessor/block**: **The GPU supports up to 1024 threads per multiprocessor and per block**, indicating how work is divided and processed in parallel.

### Additional Features

- **Concurrent copy and kernel execution**: Indicates the GPU can perform data transfers concurrently with kernel execution, with up to 3 copy engines supported.
- **Device supports Unified Addressing (UVA)**: Allows the CPU and GPU to share pointers, simplifying data management.
- **Device supports Managed Memory**: Simplifies memory management by allowing automatic migration of memory between the GPU and CPU.
- **Supports Cooperative Kernel Launch**: This feature allows multiple threads to cooperate and synchronize more complex operations within a single kernel launch.

### ECC (Error Correcting Code) Memory

- **Device has ECC support**: Enabled. This means the GPU can detect and correct certain types of memory errors, which is crucial for maintaining data integrity in critical applications.

In summary, the Tesla T4 GPU is a high-performance, CUDA-capable device designed for a wide range of compute-intensive applications, including machine learning, deep learning, and high-performance computing. Its architecture offers a balance between computational power, memory bandwidth, and advanced features like managed memory and ECC support, making it suitable for both computational workloads and AI inference tasks.
