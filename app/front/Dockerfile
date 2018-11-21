FROM python:3

WORKDIR /usr/src/app/front

COPY requirements.txt ./ 
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "-u", "./front.py" ]
