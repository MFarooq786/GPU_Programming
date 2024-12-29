# GPU Setup on Google Colab with Numba for CUDA Programming

This guide explains how to connect to a GPU like T4 on Google Colab, install Numba, and use CUDA on it.

## Steps:

### 1. Enable GPU in Google Colab

To access a GPU like the T4, follow these steps:
1. Open your Google Colab notebook.
2. Go to the **Runtime** menu.
3. Select **Change runtime type**.
4. Under **Hardware accelerator**, choose **GPU**.
5. Click **Save**.

You are now connected to a GPU, and Colab should allocate the best available GPU, including the T4.

### 2. Install numba library on the Google Collab
!pip install numba

### 2. Check for GPU Availability

After enabling the GPU, run the following Python code to confirm that the GPU is available:
```python
import tensorflow as tf
tf.config.list_physical_devices('GPU')
