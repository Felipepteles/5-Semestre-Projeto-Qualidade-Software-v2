# Aula 17 – Integração Contínua, Qualidade Automatizada, Métricas e Gestão de Defeitos

## 👤 Integrante

- Felipe Teles

---

## 1. Repositório da Atividade

| Item | Descrição |
| :--- | :--- |
| Nome do repositório | 5-Semestre-Projeto-Qualidade-Software-v2 |
| Link do repositório | https://github.com/Felipepteles/5-Semestre-Projeto-Qualidade-Software-v2 |

### Estrutura de Diretórios
Abaixo está a estrutura de arquivos do projeto, contemplando os artefatos de documentação e o ambiente configurado para testes automatizados com Python e GitHub Actions.

```text
5-Semestre-Projeto-Qualidade-Software-v2/
├── .github/
│   └── workflows/
│       └── quality.yml
├── artefatos/
├── docs/
│   ├── aula-14-qualidade-processo.md
│   ├── aula-15-modelos-maturidade.md
│   ├── aula-16-qualidade-metodologias-ageis.md
│   └── aula-17-integracao-continua-qualidade.md
├── referencias/
├── src/
├── tests/
│   └── test_order.py
├── order.py
├── requirements.txt
└── README.md
```

---

## 2. Planejamento da Funcionalidade

| Item | Descrição |
|--------|--------|
| Título da Issue | Implementar cálculo do valor total do pedido |
| Objetivo da funcionalidade | Calcular automaticamente a soma dos itens do pedido |
| Link da Issue | https://github.com/Felipepteles/5-Semestre-Projeto-Qualidade-Software-v2/issues/1 |

---

## 3. Teste Automatizado

| Item | Descrição |
|--------|--------|
| Tipo de teste | Unitário |
| Objetivo do teste | Verificar o cálculo correto do valor total |
| Link para o arquivo do teste | https://github.com/Felipepteles/5-Semestre-Projeto-Qualidade-Software-v2/blob/main/tests/test_order.py |

```python
from order import calculate_total

def test_calculate_total():
    assert calculate_total([10, 20, 30]) == 60
```

---

## 4. Pipeline de Integração Contínua

| Item | Descrição |
|--------|--------|
| Nome do workflow | Quality Check |
| Evento que dispara a execução | push e pull_request |
| Link para o workflow | https://github.com/Felipepteles/5-Semestre-Projeto-Qualidade-Software-v2/blob/main/.github/workflows/quality.yml |
| Link da execução | https://github.com/Felipepteles/5-Semestre-Projeto-Qualidade-Software-v2/actions |

```yaml
name: Quality Check

on:
  push:
    branches: [ "main", "master" ]
  pull_request:
    branches: [ "main", "master" ]

jobs:
  tests:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - name: Configurar Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.12"

      - name: Instalar dependencias
        run: pip install -r requirements.txt

      - name: Rodar testes com Pytest
        run: pytest tests/
```

---

## 5. Indicadores de Qualidade

| Indicador | Valor |
|------------|---------|
| Quantidade de testes executados | 1 |
| Quantidade de testes aprovados | 1 |
| Quantidade de testes com falha | 0 |
| Status final do pipeline | Sucesso |

---

## 6. Registro de Defeito

| Item | Descrição |
|--------|--------|
| Título do defeito | Erro no cálculo do valor total |
| Severidade | Alta |
| Link da Issue | https://github.com/Felipepteles/5-Semestre-Projeto-Qualidade-Software-v2/issues/2 |

O defeito foi simulado alterando a função para retornar um valor incorreto. O problema foi identificado pela falha do teste automatizado durante a execução do pipeline. Após corrigir a implementação, os testes voltaram a ser aprovados.