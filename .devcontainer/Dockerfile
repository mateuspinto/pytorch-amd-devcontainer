FROM rocm/pytorch:latest

ENV DEBIAN_FRONTEND=noninteractive
ENV HSA_OVERRIDE_GFX_VERSION=10.3.0

RUN apt update -y && \
    apt autoremove -y && \
    apt install -y gnupg && \
    rm -rf /var/lib/apt/lists/*

RUN chsh -s /bin/bash jenkins

COPY requirements.txt /tmp/requirements.txt

RUN pip install --no-cache-dir -r /tmp/requirements.txt