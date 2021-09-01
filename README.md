# setting-up-gcp-gpu
- Select Ubuntu 18.04 as Disk Image
- Install GCC and make

  `sudo apt install gcc`
  
  `sudo apt install make`
  
- Download CUDA 11.2 + NVIDIA driver

  `wget https://developer.download.nvidia.com/compute/cuda/11.2.2/local_installers/cuda_11.2.2_460.32.03_linux.run`
  
  `sudo sh cuda_11.2.2_460.32.03_linux.run`
  
  `export PATH=/usr/local/cuda-11.2/bin${PATH:+:${PATH}}`
  
- Download cudnn 8.1.0 from [https://developer.nvidia.com/rdp/cudnn-archive](https://developer.nvidia.com/rdp/cudnn-archive). Requires a developer account.
- Transfer the `tgz` file to VM
- Download and install Anaconda

  `wget https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh`
  
  `bash Anacon....`
  
  `source ~/.bashrc`
  
  `pip install gdown` for downloading from google drive
  
- Install cuDNN

  `tar -xzvf cudnn-11.2-linux-x64-v8.1.0.77.tgz`
  
  `sudo cp cuda/include/cudnn*.h /usr/local/cuda/include`
  
  `sudo cp -P cuda/lib64/libcudnn* /usr/local/cuda/lib64 `
  
  `sudo chmod a+r /usr/local/cuda/include/cudnn*.h /usr/local/cuda/lib64/libcudnn*`
