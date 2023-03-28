FROM python:3.8.2-alpine3.11

LABEL cf_account="salesdemo" \
      source="https://github.com/codefresh-contrib/salesdemo-flaskr"

# ENV
ENV FLASK_APP=flaskr
ENV FLASK_ENV=development
ENV ENABLE_IMPORTANT_FEATURE=true

COPY . /app

WORKDIR /app

RUN pip install --editable .
RUN flask init-db

EXPOSE 5000

CMD [ "flask", "run", "--host=0.0.0.0" ]
