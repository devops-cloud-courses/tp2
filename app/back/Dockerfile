FROM python:3.7.1-stretch

WORKDIR /usr/src/app/back

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

RUN mkdir logs

CMD ["python", "-u", "./webservice.py"]
