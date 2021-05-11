FROM python:3.6.5-alpine

COPY . /app
WORKDIR /app
RUN set -e; \
        apk add --no-cache --virtual .build-deps \
                gcc \
                libc-dev \
                linux-headers \
                mariadb-dev \
                python3-dev \
                postgresql-dev \
                tesseract-ocr \
        ;
COPY requirements.txt /app
RUN pip install -r requirements.txt
ENTRYPOINT ["python"]
CMD ["app.py"]