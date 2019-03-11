FROM python:3.7.2-alpine3.9
MAINTAINER chriz

COPY ./app /app
WORKDIR /app

RUN pip install --upgrade pip
RUN pip install -r requirements.txt
RUN apk update && apk add postgresql-dev gcc python3-dev musl-dev
RUN pip install psycopg2

CMD ['python', 'manage.py', 'runserver', '0.0.0.0:8000']
