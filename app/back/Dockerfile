FROM python:3.7.1-stretch

COPY requirements.txt ./
RUN pip install -r requirements.txt

COPY . .

CMD [ "python", "-u", "./webservice.py"]

ENV ENVIRONMENT = python:3-alpine
