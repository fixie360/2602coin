FROM python:3.6-alpine
COPY requirements.txt /
COPY ./ /2602coin_client
WORKDIR /2602coin_client
RUN apk add libc-dev gcc
RUN pip3 install -r requirements.txt
EXPOSE 8080
EXPOSE 2602
CMD ["python", "2602coin_client.py"]
