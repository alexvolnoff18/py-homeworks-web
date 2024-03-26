FROM python:3.8

WORKDIR stocks_products

COPY ../stocks_products
COPY ../logistic

RUN pip install -r /requirements.txt

ENV SECRET_KEY django-insecure-ob0yo7w(qxqv0!(lz4&0^y5)ryum=zs(v%h&y&-=@c7yezuczy
ENV DEBUG 1

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:3000", "stocks_products.wsgi"]
