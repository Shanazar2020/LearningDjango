 
FROM python:3.10

WORKDIR /app

COPY . .

ARG PYTHONUNBUFFERED=1
ARG PIP_NO_CACHE_DIR=1

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

COPY entrypoint.sh /

RUN chmod +x /entrypoint.sh

EXPOSE 8000

ENTRYPOINT ["/entrypoint.sh"]