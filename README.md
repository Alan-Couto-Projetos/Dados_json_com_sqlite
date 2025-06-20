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

### Segunda consulta:

![Extrai campos específicos de um registro JSON armazenado na tabela](https://private-user-images.githubusercontent.com/139778665/457444400-c29ddb85-8d73-4dc4-8205-deb5c6c121b1.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTA0Mzg1NjksIm5iZiI6MTc1MDQzODI2OSwicGF0aCI6Ii8xMzk3Nzg2NjUvNDU3NDQ0NDAwLWMyOWRkYjg1LThkNzMtNGRjNC04MjA1LWRlYjVjNmMxMjFiMS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDYyMFQxNjUxMDlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0wZGQ4NDg2N2Y1OWVmZTc2MWYwMGUyNmIzNTJjNjljOGM0NDQ5YTA4ZWI3ODMwNTVhNzVlZmVlN2Y4MmEyYjk4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.AUohmUhYr7fVjhH8EjWAJGEeb-LexdqQsdLR-St4mC8)

### Terceira consulta:

![Consulta um registro específico (id = 2)](https://private-user-images.githubusercontent.com/139778665/457444598-0d7017ba-b960-4765-aa97-130ba9297e55.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTA0Mzg1NjksIm5iZiI6MTc1MDQzODI2OSwicGF0aCI6Ii8xMzk3Nzg2NjUvNDU3NDQ0NTk4LTBkNzAxN2JhLWI5NjAtNDc2NS1hYTk3LTEzMGJhOTI5N2U1NS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDYyMFQxNjUxMDlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kNGJhOGJjYTJiNzM4OWQ0YjhhODRmYjQxNjA0Y2ExMGRlNzA5ZjU1ZDg2MjkyMzBhZmY5Y2MyOGNhNDdkNWYyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.4nZCotcjB4WrIX76i_Qe8kIaFXtxvAHPEWK-Eqzp1yY)

### Quarta consulta:

![Explode os dados de produtos armazenados como array JSON, associando com o evento](https://private-user-images.githubusercontent.com/139778665/457444658-4cd5e216-3ab3-48a4-bafe-4b358aa2cfc6.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTA0Mzg1NjksIm5iZiI6MTc1MDQzODI2OSwicGF0aCI6Ii8xMzk3Nzg2NjUvNDU3NDQ0NjU4LTRjZDVlMjE2LTNhYjMtNDhhNC1iYWZlLTRiMzU4YWEyY2ZjNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDYyMFQxNjUxMDlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02Y2VhNzhhNDE0MDVlZWEzYzYyY2MzM2MyNDViYzZmZjAxNmIwY2IwY2MzOTBlODAxMDk1ODYwNTQ4MGFlYTVkJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.cjzU2Nk8pEvRdNcJcVb7JuHjXCR9_qIn5tabpmXZPgc)

### Quinta consulta:

![Criação da tabela estruturada 'produtos_eventos', combinando dados de eventos e produtos](https://private-user-images.githubusercontent.com/139778665/457444700-99c33e57-3949-49a7-aed3-90084af3175c.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTA0Mzg1NjksIm5iZiI6MTc1MDQzODI2OSwicGF0aCI6Ii8xMzk3Nzg2NjUvNDU3NDQ0NzAwLTk5YzMzZTU3LTM5NDktNDlhNy1hZWQzLTkwMDg0YWYzMTc1Yy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDYyMFQxNjUxMDlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05ZjNlMDcxNzc4Y2E4ZDAwZmQ0NGUzMmY0ZDY1N2RjZWE5ZjU0NWM2NjUyMGNkMThlYmEyODczY2MzZjMyMGI0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.5x5_4V2-LJqHnS8vV6sjudFCzCyNrcKtMnhijnM9KGs)

### Sexta consulta:

![Gera e exibe objetos JSON estruturados a partir da tabela 'produtos_eventos'](https://private-user-images.githubusercontent.com/139778665/457444746-bf03cc01-a94b-4539-bbc3-d42422ede208.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTA0Mzg1NjksIm5iZiI6MTc1MDQzODI2OSwicGF0aCI6Ii8xMzk3Nzg2NjUvNDU3NDQ0NzQ2LWJmMDNjYzAxLWE5NGItNDUzOS1iYmMzLWQ0MjQyMmVkZTIwOC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNjIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDYyMFQxNjUxMDlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02ZDE1ODdmOGU5ZGM2ZGZlNDg2M2IxOTJhZTE4ZGMzMGQ4NTg3MDMxMmZjNWRkMDBjMmQxZTg1NzVkN2NkYWRjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.X8PJUGvCYdIfEP5XwN8DS8DcTF8OmSo6WOgUCWMBRCs)

---

## Resultados

### Primeira consulta:

(1, '{"event_time": "2025-06-03T10:15:00Z", "user_id": 12345, "session_id": "abcde-12345", "event_type": "product_view", "product": {"id": 9876, "name": "Smartphone XYZ", "category": "Electronics", "price": 1999.99}, "device": {"type": "mobile", "os": "Android"}, "location": {"country": "Brazil", "city": "São Paulo"}}')

### Segunda consulta:

('abcde-12345', 'product_view', 'Smartphone XYZ', 'Electronics', 'Brazil')

### Terceira consulta:

[('{"user_id": 12345, "session_id": "abcde-12345", "event_type": "cart_view", "products": [{"id": 9876, "name": "Smartphone XYZ", "category": "Electronics"}, {"id": 1234, "name": "Notebook ABC", "category": "Computers"}]}',)]

### Quarta consulta:

[('abcde-12345', 9876, 'Smartphone XYZ', 'Electronics'), ('abcde-12345', 1234, 'Notebook ABC', 'Computers')]

### Quinta consulta:

[('2025-06-03T10:15:00Z', 12345, 'abcde-12345', 'product_view', 9876, 'Smartphone XYZ', 'Electronics', 1999.99, 'mobile', 'Brazil', 'São Paulo'), ('2025-06-03T10:15:00Z', 12345, 'abcde-12345', 'cart_view', 9876, 'Smartphone XYZ', 'Electronics', None, None, 'Brazil', 'São Paulo'), ('2025-06-03T10:15:00Z', 12345, 'abcde-12345', 'cart_view', 1234, 'Notebook ABC', 'Computers', None, None, 'Brazil', 'São Paulo')]

### Sexta consulta:

[('{"user_id":12345,"session_id":"abcde-12345","product":{"id":9876,"name":"Smartphone XYZ"},"event_type":"product_view"}',), ('{"user_id":12345,"session_id":"abcde-12345","product":{"id":9876,"name":"Smartphone XYZ"},"event_type":"cart_view"}',), ('{"user_id":12345,"session_id":"abcde-12345","product":{"id":1234,"name":"Notebook ABC"},"event_type":"cart_view"}',)]

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
