# DataTalk AI

## Copiloto para análise de dados

**Status:** 🟡 Planejado

O DataTalk AI é uma aplicação experimental para carregar dados em CSV/XLSX, calcular indicadores e usar IA para transformar resultados em explicações e insights em linguagem natural.

## Problema

Planilhas podem concentrar informações importantes, mas interpretar rapidamente padrões, desvios e indicadores pode exigir análise manual.

## Solução proposta

`CSV/XLSX → Python → tratamento → métricas → LLM → insights → dashboard`

A aplicação deverá:

- carregar CSV/XLSX;
- tratar dados com Pandas;
- calcular indicadores de forma determinística;
- exibir gráficos;
- gerar interpretações com apoio de LLM;
- evitar usar a IA como fonte dos números calculados.

## Stack

- Python
- Pandas
- Streamlit
- LLM/API
- Cursor
- Excel
- Prompt Engineering

## Papel do Cursor

O Cursor será usado para acelerar desenvolvimento, revisão e refatoração do código, sempre com validação manual das sugestões.

## Avaliação

O projeto deverá comparar:

- números calculados pelo Python;
- números citados pela IA;
- qualidade e utilidade dos insights;
- presença de afirmações não suportadas pelos dados.

## Dados de exemplo

Uma base fictícia está disponível em [`data/base_exemplo.csv`](./data/base_exemplo.csv).

## Métricas

Use [`metrics/avaliacao.csv`](./metrics/avaliacao.csv) para registrar perguntas, respostas e validações.

## Próximos passos

- [ ] Criar aplicação em Streamlit
- [ ] Implementar upload de CSV
- [ ] Calcular KPIs
- [ ] Criar gráficos
- [ ] Integrar LLM
- [ ] Validar respostas
- [ ] Adicionar prints e demo
- [ ] Publicar resultados medidos
