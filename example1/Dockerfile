FROM python:3.9-alpine
ENV PYTHONUNBUFFERED 1
RUN apk update && apk upgrade && apk add bash

RUN mkdir main
WORKDIR main
COPY requirments.txt .
RUN pip3 install -r requirments.txt
COPY ../.. .
EXPOSE 8004
CMD ["python3", "flask_server_dice.py"]