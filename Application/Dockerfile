FROM ubuntu:16.04

RUN apt-get update && apt-get install -y python3-pip python3-dev && apt-get clean

RUN mkdir /code
WORKDIR /code
ADD requirements.txt /code/
RUN pip3 install -r requirements.txt
ADD . /code/
	
EXPOSE 8000 2222
CMD ["python", "/code/manage.py", "runserver", "0.0.0.0:8000"]
