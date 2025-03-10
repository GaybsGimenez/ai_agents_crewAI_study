# ai_agents_crewAI_study

Este repositório contém um estudo sobre o uso do framework **crewAI** para criação de equipes de inteligência artificial que realizam pesquisas, redação e tradução de informações.

## Instalação

Antes de iniciar, instale as dependências necessárias:
```bash
pip install crewai
pip install 'crewai[tools]'
```

## Configuração das Credenciais

Para utilizar algumas funcionalidades, como buscas no Google e acesso a modelos de IA, é necessário configurar credenciais de API. Registre-se nos seguintes serviços e obtenha suas chaves:

- [Serper.dev](https://serper.dev/) (para buscas no Google)
- [OpenAI](https://platform.openai.com/usage) (para uso do ChatGPT)

## Como Funciona

O código cria uma equipe de agentes utilizando o **crewAI**, onde cada agente tem um papel específico:

- **Pesquisador**: Coleta informações recentes sobre um tópico.
- **Redator**: Produz um artigo detalhado baseado na pesquisa.
- **Especialista em Qualidade**: Garante a precisão e a qualidade das informações.
- **Tradutor**: Traduz o conteúdo para Português do Brasil.

Cada agente possui um conjunto de ferramentas que auxiliam na execução de suas tarefas, como busca na web e extração de textos de sites.

## Execução

Para iniciar a equipe e gerar um relatório sobre um tópico específico, basta executar:
```python
result = crew.kickoff(inputs={'topic': 'lojas renner enchente rio grande do sul maio 2024'})
print(result)
```
O resultado será impresso e formatado em **Markdown**.
