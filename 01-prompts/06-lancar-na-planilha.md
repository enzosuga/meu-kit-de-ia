# Prompt: Lançar Gastos e Entradas na Planilha

Atalho adaptado do [Template do Bom Pedido](../02-templates/01-bom-prompt.md) para o meu controle financeiro no Google Sheets. Uso sempre que preciso lançar o que gastei ou recebi.

**Fixo:** a estrutura da planilha, as regras de onde cada tipo de gasto entra e o formato da resposta.
**Muda a cada uso:** só o bloco `LANÇAMENTOS`.

## Modelo

```text
CONTEXTO
Tenho uma planilha de controle financeiro no Google Sheets.
- Uma aba por ano. Cada mês é um bloco de colunas: Data | Entrada | Saída | Diário | Saldo.
- Linha 1 = mês, linha 2 = cabeçalhos, o dia D fica na linha D + 2.
- Saldo é fórmula. Data e as linhas de total (34 para baixo) não podem ser editadas.
- Pix, débito, dinheiro ou sem forma de pagamento → coluna Diário do dia da compra.
- Crédito à vista → Saída do dia 1 do mês da fatura (fecha dia 25: compra até dia 24 vai
  para o mês seguinte; do dia 25 em diante, para daqui a 2 meses).
- Crédito parcelado em N vezes → uma parcela na Saída do dia 1 de N meses seguidos,
  arredondando centavos e deixando a diferença na última parcela.
- Dinheiro recebido → coluna Entrada do dia.

INSTRUÇÃO
Para cada lançamento abaixo, diga a aba, a célula de destino, o valor atual e o novo valor
(somando ao que já existe). Se algum lançamento estiver ambíguo, pergunte antes.

LANÇAMENTOS
[cole aqui, um por linha: data, descrição, valor, forma de pagamento]

OBJETIVO
Manter o saldo do mês correto sem quebrar as fórmulas da planilha.

FORMATO
Uma tabela: Data | Descrição | Regra aplicada | Aba!Célula | Antes → Depois.
Valores no formato brasileiro (R$ 1.234,56). Não grave nada antes de eu aprovar a tabela.
```
