FROM python:3.7.1-stretch

WORKDIR /app/back

COPY requirements.txt ./

RUN pip install -r requirements.txt

COPY . .

CMD ["python", "-u", "./webservice.py"]

VOLUME /app/log
