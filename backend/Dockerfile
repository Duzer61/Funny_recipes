FROM python:3.9

RUN pip3 install --upgrade pip

WORKDIR /app

RUN pip install setuptools

RUN pip install gunicorn==21.2.0

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "foodgram.wsgi"]
