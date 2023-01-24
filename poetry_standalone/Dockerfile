ARG python_version=3.10

FROM python:$python_version

RUN apt update -y && apt install default-jre -y

RUN curl -sSL https://install.python-poetry.org | python3 -

ENV PATH="/root/.local/bin:${PATH}"
