FROM python:3.7.1-stretch

WORKDIR /tp2/app/back

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "-u", "./webservice.py" ]
