# FlowMind

## Triagem inteligente de solicitações com IA

**Status:** 🟡 Em desenvolvimento

O FlowMind é um experimento de automação para triagem de solicitações em texto livre usando **n8n + LLMs**.

> Este projeto utiliza apenas dados fictícios/públicos e não representa sistemas internos da B3.

## Problema

Solicitações operacionais normalmente chegam em texto livre. A leitura manual para identificar assunto, prioridade e encaminhamento pode consumir tempo e gerar classificações inconsistentes.

## Solução

O workflow foi pensado para:

1. receber uma solicitação por formulário ou webhook;
2. enviar o conteúdo para um LLM;
3. gerar resumo, categoria, prioridade e ação sugerida;
4. validar a resposta estruturada;
5. registrar o resultado;
6. disparar uma notificação ou próxima etapa.

## Arquitetura

`Entrada → n8n → LLM → classificação → validação → registro → notificação`

## Stack

- n8n
- LLM/API
- Prompt Engineering
- JSON
- Webhooks
- Google Sheets/Excel
- Cursor

## Estrutura de saída esperada

```json
{
  "categoria": "Acesso",
  "prioridade": "Média",
  "resumo": "Usuário solicita liberação de acesso a um sistema.",
  "acao_sugerida": "Validar autorização e encaminhar para o time responsável.",
  "justificativa": "Solicitação sem impacto crítico ou indisponibilidade."
}
```

## Experimentação

O projeto compara versões de prompts e observa:

- precisão da classificação;
- aderência ao formato solicitado;
- tempo de processamento;
- erros recorrentes;
- casos em que a IA não possui contexto suficiente.

## Métricas

As métricas devem ser preenchidas apenas após testes reais:

- tempo médio de triagem manual;
- tempo médio de triagem automatizada + revisão;
- quantidade de solicitações testadas;
- taxa de classificação correta;
- taxa de respostas válidas em JSON.

Use o arquivo [`metrics/resultados.csv`](./metrics/resultados.csv) para registrar os testes.

## Próximos passos

- [ ] Criar workflow no n8n
- [ ] Conectar um LLM via API
- [ ] Testar o prompt inicial
- [ ] Rodar os casos fictícios
- [ ] Registrar métricas
- [ ] Adicionar print do fluxo
- [ ] Adicionar vídeo curto da demo
- [ ] Atualizar este README com resultados medidos
