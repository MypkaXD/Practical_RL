FROM nvidia/cuda:12.8.2-base-ubuntu24.04

WORKDIR /app

RUN apt-get -qq update && apt-get install -y python3 python3-pip python3.12-venv

COPY .devcontainer/requirements.txt requirements.txt

RUN python3 -m venv /app/venv

ENV PATH="/app/venv/bin:$PATH"

RUN pip install --no-cache-dir torch==2.11.0 torchvision==0.26.0 torchaudio==2.11.0 --index-url https://download.pytorch.org/whl/cu128
RUN pip install --no-cache-dir -r requirements.txt

RUN apt-get install graphviz wget -y