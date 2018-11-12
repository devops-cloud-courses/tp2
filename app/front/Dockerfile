FROM python:3.7.1-stretch

WORKDIR /app/front

COPY requirements.txt ./
RUN pip install -r requirements.txt

COPY . .

CMD ["python", "-u",  "./front.py" ]

VOLUME /app/log
