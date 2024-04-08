FROM python:3.8

WORKDIR /stocks_products

COPY ./stocks_products /stocks_products


RUN pip install -r /stocks_products/requirements.txt

ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:3000", "stocks_products.wsgi"]
