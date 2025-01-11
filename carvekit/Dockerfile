# Use an official Python base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Install dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential ffmpeg libsm6 libxext6 \
    && rm -rf /var/lib/apt/lists/*

# Upgrade pip
RUN pip install --no-cache-dir --upgrade pip

# Install carvekit with the extra index URL for PyTorch
RUN pip install --no-cache-dir carvekit --extra-index-url https://download.pytorch.org/whl/cpu


