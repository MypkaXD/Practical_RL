FROM nvidia/cuda:12.9.1-base-ubuntu24.04
WORKDIR /app
RUN apt-get -qq update && apt-get install -y python3 python3-pip python3.12-venv
COPY .devcontainer/requirements.txt requirements.txt
RUN python3 -m venv /app/venv && \
    /app/venv/bin/pip install --no-cache-dir -r requirements.txt
ENV PATH="/app/venv/bin:$PATH"
# wget unzip git cmake xvfb sudo freeglut3-dev ffmpeg