# tensorrt

## Upgrade Nvidia Driver
* general system upgrade
<pre><code>sudo apt update && sudo apt upgrade</code></pre>
* check available versions
<pre><code>ubuntu-drivers list</code></pre>
* upgrade nvidia driver
<pre><code>sudo apt install nvidia-driver-VERSION_NUMBER</code></pre>
* reboot

## Purge Nvidia Driver
<pre><code>sudo apt --purge autoremove nvidia*</code></pre>

## TensorRT docker image download
https://ngc.nvidia.com/catalog/containers/nvidia:tensorrt
<pre><code>docker pull nvcr.io/nvidia/tensorrt:20.03-py3 # nvidia driver version should be higher than 440</code></pre>

There is dependency on nvidia driver versions of host.
Check dependency from following link.
https://docs.nvidia.com/deeplearning/frameworks/support-matrix/index.html

## TensorRT container run
<pre><code>docker run --gpus all -it nvcr.io/nvidia/tensorrt:20.03-py3</code></pre>
