FROM python:3.7.1-stretch

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "-u", "./front.py" ]

VOLUME app/logs
