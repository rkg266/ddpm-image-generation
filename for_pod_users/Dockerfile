# Use a base image with the necessary environment (e.g., Python, PyTorch)
FROM pytorch/pytorch:latest

# Set the working directory inside the container
WORKDIR /workspace

# Copy the contents of your training code directory into the container
COPY . /workspace

# Install any dependencies required for your training code
RUN pip install -U pip setuptools
RUN pip install absl-py scipy tensorflow tensorboardX torch torchvision torchaudio

# Define the command to run your training script when the container starts
CMD ["python", "train.py"]  # Replace with the command to run your training script