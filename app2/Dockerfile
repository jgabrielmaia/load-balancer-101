FROM ubuntu:latest

COPY ./requirements.txt /requirements.txt

WORKDIR /

RUN set -xe \
    && apt-get update \
    && apt-get install python3-pip -y
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

COPY . /

ENTRYPOINT [ "python3" ]

CMD [ "app2.py" ]
