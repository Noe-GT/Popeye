FROM python:3.8-slim-buster

RUN mkdir /poll_app

WORKDIR /poll_app

COPY . /poll_app

RUN pip3 install -r requirements.txt

EXPOSE 80

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=80"]
