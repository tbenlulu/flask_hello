FROM python:3.5.3-alpine

COPY flask_hello /flask_hello

WORKDIR /falsk_hello

RUN pip3 install -r requirements.txt
	
EXPOSE 5555

CMD ["python","run.py"]

