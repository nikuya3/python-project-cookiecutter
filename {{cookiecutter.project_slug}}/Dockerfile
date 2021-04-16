FROM python:3.8-slim as base
ARG PRODUCTION
WORKDIR /app

COPY poetry.lock pyproject.toml README.md ./
COPY {{cookiecutter.project_slug}} ./{{cookiecutter.project_slug}}/
COPY res ./res/

ENV PATH=$PATH:/home/user/.local/bin
RUN pip install poetry==1.1.6
RUN poetry config virtualenvs.create false
RUN poetry install ${PRODUCTION:+--no-dev} --no-interaction --no-ansi

CMD poetry run {{cookiecutter.project_name}}
