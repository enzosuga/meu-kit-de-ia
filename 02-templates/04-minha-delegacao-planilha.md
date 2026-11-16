# Minha Delegação: Lançamentos da Semana na Planilha

O [Template de Delegação](03-delegacao.md) preenchido para a tarefa real que eu deleguei a um agente de IA com acesso ao Google Sheets: lançar de uma vez os gastos e entradas da semana.

Revisado com o [Checklist Antes de Delegar](../03-checklists/03-antes-de-delegar.md).

```text
OBJETIVO
Lançar na minha planilha de controle financeiro todos os gastos e entradas da semana,
cada um na célula certa, sem quebrar as fórmulas de saldo.

CONTEXTO
- Planilha no Google Sheets, uma aba por ano. Cada mês é um bloco de colunas
  Data | Entrada | Saída | Diário | Saldo, e o dia D fica na linha D + 2.
- Pix, débito, dinheiro ou sem forma informada → Diário do dia da compra.
- Crédito à vista → Saída do dia 1 do mês da fatura. A fatura fecha no dia 25.
- Crédito parcelado → uma parcela na Saída do dia 1 de cada mês, a diferença de
  centavos fica na última parcela.
- Dinheiro recebido → Entrada do dia.
- Lançamentos da semana: [lista colada abaixo].

RECURSOS
- Conector do Google Sheets: ler valores e gravar valores.
- A data de hoje, consultada na ferramenta de hora (não chutar).
- Só esta planilha. Nenhum outro arquivo, e-mail ou banco.

LIMITES
- Não grave nada antes de eu aprovar a tabela de lançamentos.
- Nunca escreva nas colunas Saldo e Data nem nas linhas de total.
- Nunca apague um valor existente: some ao que já está na célula.
- Grave sempre número, nunca texto ("R$ 46,99" como texto quebra o Saldo).
- Se a aba do ano não existir ou um lançamento estiver ambíguo, pare e pergunte.

SUCESSO
- Cada lançamento está na célula prevista na tabela aprovada.
- Depois de gravar, o Saldo de cada dia alterado recalculou sem erro.
- Recebo um relatório com uma linha por célula: Aba!Célula, antes → depois,
  separando o que é fato (lido/gravado) do que é sugestão da IA.

Antes de começar, mostre como pretende realizar essa tarefa.
```

## Ações que Esperam a Minha Aprovação

| Ação | Quem decide |
|---|---|
| Ler a planilha | A IA pode fazer sozinha |
| Montar a tabela de destino | A IA pode fazer sozinha |
| Gravar qualquer célula | **Só depois da minha aprovação** |
| Lançamento ambíguo ou aba inexistente | **A IA para e pergunta** |
| Apagar ou corrigir um lançamento antigo | **Só com pedido explícito meu** |
