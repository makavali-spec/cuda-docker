# cuda-docker
This repository provides a Dockerfile for seamlessly running JAX with CUDA support, addressing common issues encountered during installation. By leveraging existing NVIDIA Docker images, users can specify the desired CUDA version (e.g., 11.4.3) and operating system (e.g., Ubuntu 20.04 or CentOS 7) to ensure compatibility.

To mitigate potential mismatches between JAX and CUDA/CuDNN versions, users can select appropriate values for CUDA and JAX_CUDA_CUDNN building variables. These values are determined based on compatibility information available via Google Storage for JAX versions and the cuDNN archive for CUDA/CuDNN versions.

For instance, JAX for CUDA is compiled with specific cuDNN versions, such as jaxlib==0.4.2 (CUDA=11) supporting cuDNN 8.2 or 8.6. Users can then choose the suitable combination, ensuring alignment between CUDA and cuDNN versions.

Additionally, users should verify the compatibility of the NVIDIA environment, including the NVIDIA driver version, with the requested CUDA version.

The Docker image can be built using the provided Dockerfile, with customizable options such as CUDA version, operating system, and user settings. This streamlined process simplifies the setup of JAX with CUDA support within a Docker container, promoting ease of use and reproducibility in machine learning workflows.
