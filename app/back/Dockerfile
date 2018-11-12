FROM python:3-alpine

WORKDIR ./

COPY requirements.txt ./

RUN pip install -r requirements.txt

COPY . .

RUN mkdir logs

CMD [ "python","-u", "webservice.py" ]
