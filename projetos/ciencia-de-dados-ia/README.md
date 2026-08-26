# Ciência de Dados e IA | Oficina Automóvel

[Voltar ao portfólio](../../README.md) · [Arquitetura](./arquitetura.md) · [Evidências e limites](./evidencias-e-limites.md)

## Dados organizados para apoiar decisões de manutenção

Um veículo tem dados de identificação que mudam pouco e registos técnicos que evoluem ao longo do tempo. O desafio deste projeto acadêmico é organizar essas informações e integrar uma previsão de necessidade de revisão, preservando a distinção entre a indicação do modelo e a decisão do mecânico.

**Contexto:** Introdução à Inteligência Artificial e Ciência de Dados / Introdução à Engenharia e Ciência de Dados, Universidade de Coimbra, ano letivo 2025/2026.

**Entrega analisada:** código Python e relatório do Projeto II, identificado em nome de Alessandra Souza Garcia. A documentação descreve o material recebido; não atribui autoria exclusiva de cada componente nem confunde resoluções dos docentes com trabalho autoral.

> Protótipo educacional. Não é um sistema de diagnóstico automóvel validado nem uma aplicação em produção. Esta página apresenta evidências do código e seus limites, sem afirmar desempenho preditivo.

## O que o projeto reúne

| Frente | Evidência na entrega | Limite da apresentação |
| --- | --- | --- |
| Integração de dados | Leitura de oficinas em JSON e veículos em CSV; conversão de campos numéricos e inserção no SQLite | Não foi identificado um pipeline completo de limpeza de valores ausentes ou anômalos |
| Banco relacional | Cinco tabelas para oficinas, veículos, registos técnicos, previsões e decisões do mecânico | Declarar relacionamentos não garante que sua integridade esteja sendo aplicada |
| Consulta e organização | Menu de terminal, listagens, pesquisa por matrícula e exclusão de veículo | Não equivale a um CRUD completo nem a controle de acesso por perfil |
| Integração com IA | Carregamento de modelo serializado e chamada de previsão com quatro atributos | Treinamento, pré-processamento e avaliação não foram fornecidos |
| Persistência de previsões | Rotina que grava resultado, data/hora e identificação do modelo | O banco entregue contém resultados armazenados, não uma validação de sua qualidade |

## Duas etapas de uma mesma proposta acadêmica

**Projeto I — classificação:** o enunciado propõe preparação de dados, seleção de variáveis e comparação de classificadores. O arquivo de dados recebido contém 600 linhas e sete colunas: seis atributos e uma decisão de revisão, conforme o enunciado. Isso demonstra a disponibilidade de dados e requisitos, não a execução de todas as etapas.

**Projeto II — engenharia de dados:** a entrega contém o sistema em Python e SQLite, importadores, consultas e código de integração com o modelo. É a parte com maior evidência concreta nos materiais analisados e o foco deste estudo de caso.

## Como a solução foi organizada

- **Entrada:** arquivos JSON e CSV.
- **Transformação:** leitura dos campos, conversão de tipos e construção de objetos.
- **Persistência:** classes de acesso a dados (DAO) e banco SQLite.
- **Consulta:** interface de terminal com opções de pesquisa e listagem.
- **Previsão:** quatro atributos técnicos enviados ao modelo, com gravação do resultado.

A [arquitetura](./arquitetura.md) detalha as entidades, as camadas e os atributos utilizados.

## Competências evidenciadas

Python, SQL, modelagem relacional, organização de código em camadas, importação de dados estruturados e integração de inferência com persistência.

NumPy e Pandas aparecem nos materiais didáticos recebidos. Não são apresentados como dependências diretas comprovadas dos importadores do Projeto II, que utilizam os módulos `csv`, `json` e `sqlite3`.

## Estado da versão

A análise estática confirmou a presença das rotinas descritas e a sintaxe dos arquivos Python. Um teste isolado de SQL confirmou uma inconsistência no relatório estatístico. Não houve execução integral da aplicação nem carregamento do modelo serializado.

**Próximos passos:** recuperar o treinamento do Projeto I; corrigir relatório e integridade dos dados; testar o fluxo completo em ambiente isolado; preparar exemplos públicos e instruções reproduzíveis.

[Consultar a revisão técnica e os cuidados de publicação](./evidencias-e-limites.md)

## Materiais e atribuição

Esta versão pública contém apenas documentação elaborada a partir da entrega. Código, banco, modelo, relatório original e resoluções didáticas não estão incluídos nesta pasta.

Os enunciados e as fichas de resolução pertencem ao contexto didático da Universidade de Coimbra e mantêm sua autoria docente. Sua presença entre os materiais de estudo não implica autoria da estudante nem autorização de redistribuição.
