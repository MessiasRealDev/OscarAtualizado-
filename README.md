# 📊 Banco de Dados do Oscar com MongoDB

Este projeto contém um banco de dados com indicações ao Oscar, importado de um arquivo `.csv` e armazenado em uma coleção do MongoDB. Os dados foram traduzidos para o português e podem ser manipulados via `mongosh` ou `mongoimport`.

---

## 🧩 Estrutura dos Dados

Cada documento possui os seguintes campos:

- `ano_filme`: Ano de lançamento do filme
- `ano_cerimonia`: Ano em que ocorreu a cerimônia
- `cerimonia`: Número da cerimônia do Oscar
- `categoria`: Categoria da premiação (ex: ATOR, ATRIZ COADJUVANTE)
- `nome`: Nome da pessoa indicada
- `filme`: Nome do filme indicado
- `vencedor`: Valor booleano (`true` para vencedores, `false` para não vencedores)

---

## 📥 Importar Dados com mongoimport

Para importar o arquivo CSV para o MongoDB, use o seguinte comando no terminal:

```bash
mongoimport --uri "mongodb://localhost:27017" \
  --db oscar \
  --collection Registros \
  --type csv \
  --file oscar_database_traduzido.csv \
  --headerline
