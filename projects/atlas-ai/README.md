# Atlas AI

## Agente de conhecimento com ferramentas

**Status:** 🟡 Planejado

O Atlas AI é um experimento de agente capaz de consultar uma base de conhecimento controlada, recuperar contexto relevante e responder perguntas utilizando ferramentas específicas.

## Problema

Encontrar informações em vários documentos exige buscas repetitivas e leitura manual.

## Solução proposta

`Pergunta → agente → decisão → busca → contexto → LLM → resposta`

O agente poderá usar:

- ferramenta de busca;
- ferramenta de cálculo;
- ferramenta de registro/log.

## Stack

- n8n
- LLMs
- RAG
- Agentes de IA
- APIs
- Prompt Engineering
- Cursor

## Regras de segurança e qualidade

O agente deverá:

- não inventar respostas ausentes da base;
- informar quando não houver contexto suficiente;
- limitar respostas ao conteúdo permitido;
- indicar a fonte utilizada;
- registrar casos problemáticos para revisão.

## Base de conhecimento

Use apenas documentos públicos ou fictícios. Um exemplo está em [`docs/base_conhecimento_exemplo.md`](./docs/base_conhecimento_exemplo.md).

## Prompt

O prompt inicial está em [`prompts/agente_prompt.md`](./prompts/agente_prompt.md).

## Avaliação

Registrar:

- pergunta;
- fonte recuperada;
- resposta;
- aderência à fonte;
- presença de alucinação;
- tempo de resposta;
- observações.

Use [`metrics/avaliacao.csv`](./metrics/avaliacao.csv).

## Próximos passos

- [ ] Definir base de conhecimento
- [ ] Criar mecanismo de busca
- [ ] Conectar LLM
- [ ] Criar ferramenta de cálculo
- [ ] Criar logs
- [ ] Rodar conjunto fixo de perguntas
- [ ] Medir qualidade
- [ ] Adicionar demo
