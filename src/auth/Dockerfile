FROM python:3.10-slim-bullseye
RUN apt-get update \
    && apt-get install -y --no-install-recommends --no-install-suggests \
    pkg-config \
    build-essential default-libmysqlclient-dev \

    && pip install --no-cache-dir --upgrade pip

WORKDIR /app
COPY ./requirements.txt /app
RUN pip install -r /app/requirements.txt
# RUN pip install --no-cache-dir flask pyjwt
# RUN pip install --no-cache-dir flask_mysqldb
COPY . /app

EXPOSE 5000

CMD ["python","server.py"]