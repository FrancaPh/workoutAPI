# WorkoutAPI

[![Python Version](https://img.shields.io/badge/python-3.11.4-blue.svg)](https://www.python.org/downloads/)
![Star Badge](https://img.shields.io/static/v1?label=%F0%9F%8C%9F&message=If%20Useful&style=style=flat&color=BC4E99)
![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)
[![View My Profile](https://img.shields.io/badge/View-My_Profile-green?logo=GitHub)](https://github.com/FrancaPh)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Descrição
Essa API foi criada como desafio de um lab durante um bootcamp da **[DIO](https://web.dio.me)** com parceria da Vivo, [Python AI Backend Developer](https://web.dio.me/track/coding-future-vivo-python-ai-backend-developer).
O desafio consiste na criação de uma poderosa API assíncrona de um academia para uma competição de crossfit. Usando o framework FastAPI, permitiu a construção eficiente desse aplicativo web, moderno, que ajuda a lidar com operações simultâneas de maneira eficaz e escalável. 

## Stack da API

A API foi desenvolvida utilizando o `fastapi` (async), junto das seguintes libs: `alembic`, `SQLAlchemy`, `pydantic`. Para salvar os dados está sendo utilizando o `postgres`, por meio do `docker`.

## Execução da API

Para executar o projeto, utilizei a [pyenv](https://github.com/pyenv/pyenv), com a versão 3.11.4 do `python` para o ambiente virtual.

Caso opte por usar pyenv, após instalar, execute:

```bash
pyenv virtualenv 3.11.4 workoutapi
pyenv activate workoutapi
pip install -r requirements.txt
```
Para subir o banco de dados, caso não tenha o [docker-compose](https://docs.docker.com/compose/install/linux/) instalado, faça a instalação e logo em seguida, execute:

```bash
make run-docker
```
Para criar uma migration nova, execute:

```bash
make create-migrations d="nome_da_migration"
```

Para criar o banco de dados, execute:

```bash
make run-migrations
```

## API

Para subir a API, execute:
```bash
make run
```
e acesse: http://127.0.0.1:8000/docs

# Referências

FastAPI: https://fastapi.tiangolo.com/

Pydantic: https://docs.pydantic.dev/latest/

SQLAlchemy: https://docs.sqlalchemy.org/en/20/

Alembic: https://alembic.sqlalchemy.org/en/latest/

Fastapi-pagination: https://uriyyo-fastapi-pagination.netlify.app/
