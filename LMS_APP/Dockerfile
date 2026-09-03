FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .
COPY config ./config
COPY controllers ./controllers
COPY dao ./dao
COPY models ./models
COPY services ./services
COPY utils ./utils
COPY templates ./templates
COPY static ./static

EXPOSE 3000

CMD [ "gunicorn", "--bind", "0.0.0.0:3000", "app:app" ]