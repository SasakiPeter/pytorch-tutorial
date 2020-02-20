FROM python:3.7.6-slim-buster
RUN mkdir /code
WORKDIR /code
COPY requirements.txt /code/
RUN apt-get update && apt-get install -y \
  graphviz \
  xdg-utils &&\
  apt-get clean && \ 
  rm -rf /var/lib/apt/lists/* &&\
  # pip --no-cache-dir install --upgrade pip && \
  pip --no-cache-dir install -r requirements.txt
COPY . /code/