FROM python:3.7.1-stretch

COPY requirements.txt ./

RUN pip install -r requirements.txt
RUN mkdir logs

COPY . .

CMD ["python", "-u", "./front.py"]
