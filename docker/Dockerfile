FROM pytorch/pytorch:2.0.1-cuda11.7-cudnn8-runtime

RUN mkdir workspace
WORKDIR /workspace

# RUN pip3 install fastapi uvicorn[standard] fsspec[http]==2023.1.0
RUN git clone https://github.com/117503445/nougat.git
WORKDIR /workspace/nougat

RUN python3 setup.py install

EXPOSE 8503

CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8503"]
# Run this using 'docker run -it -d -p <YOUR PORT>:8503 --gpus all <IMAGE NAME>
