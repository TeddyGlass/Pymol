ARG VARIANT
FROM python:${VARIANT}-slim

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
  apt-utils \
  # zsh \
  gcc \
  zsh \
  build-essential \
  && pip install --no-cache-dir --upgrade pip \
  && pip install --no-cache-dir \
  autopep8 \
  flake8 \
  && apt-get autoremove -y\
  && apt-get clean -y \
  && rm -rf /var/lib/apt/lists/* 


# RUN chsh -s /bin/zsh