FROM python:3.6

RUN apt-get update && apt-get install -y cmake

RUN mkdir -p /rasa_app
WORKDIR /rasa_app

COPY . /rasa_app

RUN python -m pip install -U pip
RUN pip install -r requirements.txt

RUN python -m spacy download en

RUN pip install --no-warn-script-location rasa==2.1.2
RUN pip install --no-warn-script-location sanic==19.9.0
