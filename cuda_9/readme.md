# Use an official CUDA image as the base image
FROM nvidia/cuda:9.0-base

# Install basic dependencies
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
&& rm -rf /var/lib/apt/lists/*

# Install PyTorch with CUDA 9 support
RUN pip3 install torch==1.4.0+cu90 torchvision==0.5.0+cu90 -f https://download.pytorch.org/whl/cu90/torch_stable.html

# Copy your Python script into the container
COPY your_script.py /app/your_script.py

# Set the working directory
WORKDIR /app

# Run the Python script
CMD ["python3", "your_script.py"]
