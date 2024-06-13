FROM python:3.6.0-alpine

WORKDIR /app
ADD . /app

RUN apk --no-cache --update add build-base && \
    pip install -r /app/requirements.txt --trusted-host pypi.python.org && \
    apk del build-base

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts
ENV network-alias post2

ENTRYPOINT ["python3", "post_app.py"]
