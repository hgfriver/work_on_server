FROM ubuntu:20.04


WORKDIR /app

RUN apt update && \
    apt upgrade -y && \
    apt install -y \
    python3 \
    python3-pip && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
    
    
RUN pip3 --no-cache-dir install torch \
    torchvision \
    torchaudio --extra-index-url https://download.pytorch.org/whl/cpu \
    tensorboard
    
CMD ["tensorboard", "--logdir=runs" ,"--host=0.0.0.0", "--port=6006"]
# tensorboard --logdir=runs => means directory will be /runs




EXPOSE 6006
