# Dados JSON com SQLite

Este projeto simula um cenário real de e-commerce, onde eventos de navegação de usuários são registrados em formato JSON. Utilizei o SQLite, um banco de dados leve e embutido para armazenar, explorar e transformar esses dados semiestruturados usando SQL puro.

---

## Objetivo

Demonstrar como é possível manipular dados em formato JSON diretamente no SQLite, realizando extrações, transformações e consultas em uma base simulada de eventos de usuários.

---


## Estrutura dos Dados

Exemplo de dado armazenado (coluna `data_raw`):


<pre> <code>```json
{
  "event_time": "2025-06-03T10:15:00Z",
  "user_id": 12345,
  "session_id": "abcde-12345",
  "event_type": "product_view",
  "product": {![consulta 1](https://github.com/user-attachments/assets/1de440c2-c6bf-41c3-9d5d-3887b2cf1403)

    "id": 9876,
    "name": "Smartphone XYZ",
    "category": "Electronics",
    "price": 1999.99
  },
  "device": {
    "type": "mobile",
    "os": "Android"
  },
  "location": {
    "country": "Brazil",
    "city": "São Paulo"
  }
}```</code> </pre>

---

## Como Rodar

Este projeto foi desenvolvido em Jupyter Notebook usando Python e SQLite. Abaixo estão os passos completos para rodá-lo no seu computador.

### Pré-requisitos
Antes de tudo, você precisa ter instalado:

Python 3.9+

Git (Para clonar o projeto)

VS Code com extensão do Jupyter

### Passo 1 – Instale o VS Code (caso ainda não tenha)
Acesse: https://code.visualstudio.com/

Baixe o instalador para seu sistema operacional

Instale normalmente

Abra o VS Code e vá em:

Extensões (Ctrl+Shift+X)

Busque por Jupyter e instale a extensão oficial da Microsoft

### Passo 2 – Instale as bibliotecas necessárias
Abra um terminal e execute:

pip install jupyter
### Passo 3 – Clone o repositório (ou baixe o ZIP)
Com Git:

git clone https://github.com/Alan-Couto-Projetos/Dados_json_com_sqlite
cd Sqlite
Ou baixe o projeto como .zip e extraia os arquivos.

### Passo 4 – Rode o Jupyter Notebook
Você pode executar o notebook diretamente no VS Code:

Abra o VS Code e navegue até a pasta do projeto

Abra o arquivo .ipynb

Execute cada bloco com Shift + Enter

---

## Consultas Implementadas

### Primeira consulta:
![Consulta e imprime a primeira linha da tabela para verificação](https://private-user-images.githubusercontent.com/139778665/457444206-67dbf59e-b35a-41db-bd3b-c9107871e4f7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTA0MzgxMjUsIm5iZiI6MTc1MDQzNzgyNSwicGF0aCI6Ii8xMzk3Nzg2NjUvNDU3NDQ0MjA2LTY3ZGJmNTllLWIzNWEtNDFkYi1iZDNiLWM5MTA3ODcxZTRmNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDYyMFQxNjQzNDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03YWE3NDljMWIwOGJiNzkwMjE3ZTUwYzZiMThlOGRlZmZkZjhmYmY1MmUxMjUxY2FlNzUzZDA4ZDUyMjkyODM1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.1MrP-OjkORfcURwi9RNyFBVFodpXhU2umA3vNBUqylw)


---

## Resultados


---

## Aprendizados

SQLite possui suporte nativo a JSON com json_extract, json_each, json_object.

Mesmo sem ferramentas em nuvem, é possível simular cenários reais de engenharia de dados.

A prática com dados semiestruturados é essencial para projetos modernos de BI e ciência de dados.

---

## Repositório

Código-fonte completo + base simulada:
https://github.com/Alan-Couto-Projetos/Dados_json_com_sqlite

---

## Autor

Alan Couto
