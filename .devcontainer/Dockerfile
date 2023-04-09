FROM python:3.9-slim-buster

# Install necessary packages
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    git \
    libssl-dev \
    zlib1g-dev

# Install Jupyter
RUN pip install --no-cache-dir \
    jupyterlab \
    nbdev \
    dvc \
    rdflib \
    csvw \
    openai \
    weaviate-client

# Expose Jupyter port
EXPOSE 8888

# Set the working directory
WORKDIR /workspace

# Start Jupyter
CMD ["jupyter", "lab", "--ip", "0.0.0.0", "--no-browser", "--allow-root"]
