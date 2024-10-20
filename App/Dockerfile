FROM alpine

RUN apk -U upgrade
RUN apk add python3
RUN apk add py3-pip
RUN python3 -m venv pythonenv
RUN pythonenv/bin/pip install Django
RUN apk add mysql mysql-client

WORKDIR /app
COPY /src ./

CMD ["python", "hello.py"]