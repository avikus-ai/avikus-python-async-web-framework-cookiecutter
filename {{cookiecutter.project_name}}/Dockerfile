FROM python:3.8-alpine3.11

COPY requirements.txt /tmp/requirements.txt

RUN apk add --no-cache --virtual .build-deps gcc libc-dev \
    && pip install --no-cache-dir -r /tmp/requirements.txt \
    && apk del .build-deps gcc libc-dev




CMD ["uvicorn main:app"]