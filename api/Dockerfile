FROM python:3.9-buster

ENV PYTHONUNBUFFERED 1

WORKDIR /app

COPY requirements.txt ./

RUN apt update && apt install libpq-dev python-dev gcc -y
RUN pip install -r requirements.txt

COPY ./ ./

CMD ["python3", "manage.py", "runserver"]