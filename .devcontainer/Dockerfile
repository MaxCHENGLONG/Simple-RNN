FROM pytorch/pytorch:1.0-cuda10.0-cudnn7-runtime

WORKDIR /workspaces/Char-RNN-PyTorch

ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

RUN pip install --no-cache-dir numpy==1.16.3

COPY . .

RUN mkdir -p data preTrained logs outputs

RUN python -c "import torch; print('Torch:', torch.__version__); print('CUDA:', torch.version.cuda)"

CMD ["python", "-u", "CharRNN.py"]