# SimpleCalc 🧮

**SimpleCalc** é um pacote Python simples que oferece operações matemáticas básicas por meio de funções e classes. Ideal para quem está começando com desenvolvimento em Python ou precisa de uma calculadora leve para projetos maiores.

## Funcionalidades

- Adição
- Subtração
- Multiplicação
- Divisão (com tratamento de divisão por zero)

## Instalação

Você pode instalar localmente com:

```bash
pip install .

Ou, se estiver empacotado e publicado:
pip install simplecalc

Exemplo de uso

from simplecalc import add, divide

print(add(10, 5))       # Saída: 15
print(divide(10, 2))    # Saída: 5.0

ou usando a classe:
from simplecalc.calculadora import Calculadora

calc = Calculadora()
print(calc.somar(3, 7))  # Saída: 10

Autor: Carlos
