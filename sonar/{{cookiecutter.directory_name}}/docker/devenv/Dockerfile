FROM ubuntu:disco

RUN apt-get update && apt-get install -y python3 python3-pip git

COPY requirements.txt .
COPY setup.py .

RUN pip3 install --upgrade setuptools==40.6.3
RUN pip3 install -r requirements.txt
RUN pip3 install jupyter

RUN pip3 install git+https://github.com/pedrolisboa/poseidon

RUN useradd -ms /bin/bash tars

USER tars

WORKDIR /home/tars
