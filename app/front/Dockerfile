FROM python:3-alpine

WORKDIR /Users/cpiovesan/Documents/ECE/ING5/Microservices/tp2/front

COPY . .

RUN pip install --no-cache-dir -r requirements.txt

RUN mkdir logs

CMD [ "python", "-u", "./front.py" ]
