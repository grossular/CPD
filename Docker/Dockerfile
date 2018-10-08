FROM lspvic/tensorboard-notebook

USER root

RUN apt-get update && apt-get install -y curl

ADD requirements.txt .

RUN pip install -r requirements.txt && rm -rf requirements.txt

EXPOSE 6006
EXPOSE 4040
EXPOSE 8888

USER jovyan
