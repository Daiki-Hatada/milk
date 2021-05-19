FROM python:3.9
ENV PYTHONDONTWRITEBYTECODE=1 PYTHONBUNBUFFERED=1
WORKDIR /usr/src/
COPY requirements.txt ./
RUN python3 -m pip install --upgrade pip setuptools
RUN pip install -r requirements.txt
COPY ./src/ ./
# CMD [ "gunicorn", "--bind", ":8000", "config.wsgi:application" ]
CMD [ "uwsgi", "--http-websockets", "--ini", "uwsgi.ini" ]
EXPOSE 8000
