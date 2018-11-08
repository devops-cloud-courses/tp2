FROM python:3-alpine

WORKDIR ./

COPY requirements.txt ./

RUN pip install -r requirements.txt

COPY . .

CMD [ "python","-u", "front.py" ]
