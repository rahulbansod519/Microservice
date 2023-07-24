FROM python:3.10-slim-bullseye
RUN apt-get update \
    && apt-get install -y --no-install-recommends --no-install-suggests \
    pkg-config \
    build-essential  ffmpeg\
    && pip install --no-cache-dir --upgrade pip

WORKDIR /app
COPY ./requirements.txt /app
RUN pip install -r /app/requirements.txt

COPY . /app

CMD ["python","consumer.py"]