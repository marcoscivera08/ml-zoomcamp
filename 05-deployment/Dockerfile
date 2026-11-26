FROM python:3.12-slim

WORKDIR /app

RUN pip install --no-cache-dir scikit-learn==1.9.1 numpy==2.5.4 flask==3.1.3 gunicorn

COPY ["predict.py", "model_C=1.0.bin", "./"]

EXPOSE 9696

ENTRYPOINT ["gunicorn", "--bind=0.0.0.0:9696", "predict:app"]