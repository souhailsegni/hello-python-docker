
FROM python:3.8-slim

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

WORKDIR /app

COPY . /app

RUN pip install -r requirements.txt --timeout=120 --index-url https://pypi.org/simple/

EXPOSE 5000

CMD ["flask", "run"]
