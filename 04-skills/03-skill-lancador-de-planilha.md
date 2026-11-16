# Skill: Lançador da Planilha Financeira

O atalho que eu mais uso ([Lançar na Planilha](../01-prompts/06-lancar-na-planilha.md)) transformado em skill, seguindo o [guia de estrutura](01-como-estruturar-uma-skill.md) e o modelo da [Skill Preparador de Reuniões](02-skill-preparador-de-reunioes.md). Com ela, basta dizer "gastei 32 no mercado no Pix" e a IA segue sempre o mesmo procedimento.

```text
OBJETIVO
Lançar gastos e entradas na planilha de controle financeiro do Google Sheets,
na célula correta, sem quebrar as fórmulas.

INSTRUÇÕES
- Uma aba por ano; cada mês é um bloco Data | Entrada | Saída | Diário | Saldo.
- O dia D fica na linha D + 2. Totais ficam da linha 34 para baixo.
- Pix, débito, dinheiro ou sem forma de pagamento → Diário do dia.
- Crédito à vista → Saída do dia 1 do mês da fatura (fecha dia 25).
- Crédito parcelado → uma parcela por mês na Saída do dia 1; centavos na última.
- Dinheiro recebido → Entrada do dia.

PROCEDIMENTO
1. Consultar a data de hoje na ferramenta de hora.
2. Identificar tipo, valor, data e forma de pagamento de cada lançamento.
3. Calcular aba e célula de destino de cada um.
4. Ler o valor atual de cada célula de destino.
5. Mostrar a tabela Aba!Célula | antes → depois e esperar aprovação.
6. Gravar como número, somando ao valor existente.
7. Ler o Saldo dos dias alterados para confirmar o recálculo.
8. Entregar o relatório.

VERIFICAÇÕES
- O valor foi gravado como número, não como texto?
- O Saldo do dia mudou e não mostra erro?
- A soma das parcelas é igual ao valor da compra?

EXCEÇÕES
- Valor, data ou forma de pagamento ambíguos → perguntar antes de gravar.
- Aba do ano não existe → avisar e não lançar aquela parcela.
- Saldo com erro depois de gravar → regravar como número e avisar.

REGRAS
- Não gravar nada sem aprovação da tabela.
- Não escrever em Saldo, Data ou linhas de total.
- Não apagar valores existentes sem pedido explícito.
- Não acessar outros arquivos, e-mails ou contas.

FORMATO DE SAÍDA
Fatos (lido e gravado na planilha): uma linha por célula, "Diário 12/nov: R$ 25,00 → R$ 72,90".
Sugestões da IA: separadas, marcadas como sugestão, nunca executadas sozinhas.
```
