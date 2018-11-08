FROM python:3-alpine

WORKDIR ./

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

RUN mkdir logs
CMD [ "python", "-u", "./front.py" ]
