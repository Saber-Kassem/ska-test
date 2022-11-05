FROM python:3.7-alpine

WORKDIR /app

RUN apk add --no-cache gcc musl-dev linux-headers geos libc-dev postgresql-dev

COPY requirements.txt /app
RUN pip install -r requirements.txt

EXPOSE 5000

COPY . /app

CMD ["flask", "run", "--host", "0.0.0.0"]