FROM python:3-alpine

WORKDIR /home/rv/micro-service/tp2/app/back

COPY . .

RUN pip install --no-cache-dir -r requirements.txt

RUN mkdir logs

CMD [ "python", "-u", "./webservice.py" ]
