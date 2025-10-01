# EmpacotamentoDePacotesComPython

===========================================
README.txt — Projeto: SimpleCalc
===========================================

📌 DESCRIÇÃO DO PROJETO
------------------------
SimpleCalc é uma calculadora simples desenvolvida em Python. Ela realiza operações básicas (adição, subtração, multiplicação e divisão) e foi empacotada para distribuição via PyPI. O projeto inclui testes automatizados com pytest e segue boas práticas de empacotamento e versionamento.

📁 ESTRUTURA DO PROJETO
------------------------
simplecalc/
├── simplecalc/            → Código-fonte do pacote
│   └── __init__.py        → Funções da calculadora
├── tests/                 → Testes automatizados
│   └── test_basic.py
├── setup.py               → Configuração do pacote
├── pyproject.toml         → Configuração de build
├── README.txt             → Documentação completa
├── README.md              → Versão para PyPI
├── LICENSE                → Licença (MIT)
├── requirements.txt       → Dependências
└── .gitignore             → Arquivos ignorados pelo Git

🚀 FASES DO PROJETO
-------------------

1️⃣ CRIAÇÃO DO PROJETO
-----------------------
- Criar novo projeto no PyCharm com ambiente virtual (virtualenv)
- Nome: simplecalc
- Python 3.6 ou superior

2️⃣ IMPLEMENTAÇÃO DAS FUNÇÕES
------------------------------
Arquivo: simplecalc/__init__.py

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b

CRIAÇÃO DOS TESTES

import pytest
from simplecalc import add, subtract, multiply, divide

def test_add():
    assert add(2, 3) == 5

def test_subtract():
    assert subtract(5, 2) == 3

def test_multiply():
    assert multiply(3, 4) == 12

def test_divide():
    assert divide(10, 2) == 5

def test_divide_by_zero():
    with pytest.raises(ValueError):
        divide(10, 0)

4- INSTALAÇÃO DE DEPENDENCIAS COM O AMBIENTE VIRTUAL ATIVADO

pip install setuptools wheel twine build pytest

SALVAR OS ARQUIVOS REQUIREMENTS.TXT

pip freeze > requirements.txt

5- CONFIGURAÇÃO DO SETUP.PY

from setuptools import setup, find_packages

setup(
    name="simplecalc",
    version="0.1.0",
    packages=find_packages(),
    description="Uma calculadora simples em Python",
    long_description=open("README.md", encoding="utf-8").read(),
    long_description_content_type="text/markdown",
    author="Carlos",
    author_email="seu@email.com",
    license="MIT",
    classifiers=[
        "Programming Language :: Python :: 3",
        "License :: OSI Approved :: MIT License",
        "Operating System :: OS Independent",
    ],
    python_requires=">=3.6",
    install_requires=[],
)

CONFIGURAÇÃO DO PYPROJECT.TOML
[build-system]
requires = ["setuptools>=42", "wheel"]
build-backend = "setuptools.build_meta"


7- EXECUÇÃO DOS TESTES
pytest

8-EMPACOTAMENTO DO PROJETO
python -m build

Gera os arquivos em dist/:

9-    PUBLICAÇÃO NO PYPI

    Crie uma conta em 
FAÇA LOGIN NO TERMINAL:
twine login

PUBLIQUE 

twine upload dist/*

10-VERSIONAMENTO COM GIT (OPCIONAL)

git init
git add .
git commit -m "Versão inicial"
git remote add origin https://github.com/seuusuario/simplecalc.git
git push -u origin master




📌 OBSERVAÇÕES FINAIS

    Atualize a versão no SETUP.PY
    USE README.MD para a descrição no pypi
    teste totalment antes de publicar
    para testes de publicação, user tespypy:https://test.pypi.org
