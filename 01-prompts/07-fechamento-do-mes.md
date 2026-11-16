# Prompt: Fechamento do Mês na Planilha

Atalho adaptado do [Template de Pesquisa e Decisão](../02-templates/02-pesquisa-e-decisao.md). Uso no fim do mês para entender para onde foi o dinheiro antes de decidir o que ajustar no mês seguinte. É só leitura: a IA não altera nada.

**Fixo:** onde ficam os totais, os critérios de análise e a separação entre fato e sugestão.
**Muda a cada uso:** o mês analisado e o mês de comparação.

## Modelo

```text
PERGUNTA
Como foi o meu mês de [mês/ano] em comparação com [mês anterior]?

PESQUISA
Leia na minha planilha financeira do Google Sheets os totais de [mês] e [mês anterior]
(Entradas, Saídas, Diário, Saída Total e Performance ficam logo abaixo do dia 31)
e os valores diários da coluna Diário.

FONTES E EVIDÊNCIAS
Cite a aba e as células de cada número que usar. Se uma célula estiver vazia ou com erro,
diga isso em vez de estimar.

CRITÉRIOS
- variação do Diário (gasto do dia a dia) entre os dois meses;
- peso da fatura do cartão (Saída do dia 1) no mês;
- dias com gasto fora do padrão (mais que o dobro da média diária).

COMPARAÇÃO
Uma tabela com os dois meses lado a lado e a variação em R$ e em %.

DECISÃO
Separe em duas listas: "Fatos lidos na planilha" e "Sugestões da IA".
A decisão do que mudar é minha. Não altere nenhuma célula.
```
