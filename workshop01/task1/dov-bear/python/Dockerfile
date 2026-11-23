FROM python:3.13-alpine

LABEL name=myapp

ARG APP_DIR=/app 

WORKDIR ${APP_DIR}

COPY main.py .
COPY utils.py . 
COPY public public
COPY templates templates
COPY requirements.txt .

RUN pip install -r requirements.txt

ENV PORT=3000
ENV INSTANCE_NAME=""
ENV INSTANCE_HASH=""

EXPOSE ${PORT}

ENTRYPOINT ["python", "main.py" ,"${PORT}"]
