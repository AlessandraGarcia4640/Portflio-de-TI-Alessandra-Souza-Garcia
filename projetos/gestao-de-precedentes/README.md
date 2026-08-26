# Gestão de Precedentes Judiciais

### Do documento linear à consulta estruturada do conhecimento

Projeto de uma solução para pesquisar, organizar e acompanhar versões de precedentes. A apresentação conecta gestão do conhecimento, desenho de processos e desenvolvimento de uma experiência de consulta web.

**Alessandra Souza Garcia · Gestão pública · Transformação digital · Tecnologia**

> **Demonstração pública.** Os registros são fictícios e a interface é somente para consulta. O material não é uma publicação oficial, não fornece orientação jurídica e não demonstra integração com sistemas institucionais.

[Acessar demonstração](https://alessandragarcia4640.github.io/gestao-de-precedentes-Demo/) · [Ver código](https://github.com/AlessandraGarcia4640/gestao-de-precedentes-Demo) · [Voltar ao portfólio](../../README.md)

[Estudo de caso](./estudo-de-caso.md) · [Arquitetura e escopo](./arquitetura.md) · [Segurança e privacidade](./seguranca-e-privacidade.md)

## O problema

Um acervo crescente, mantido em documento único, pode preservar o conteúdo e ainda dificultar sua utilização. Encontrar uma orientação, combinar critérios de pesquisa e identificar alterações passa a depender de busca textual, conferência manual e conhecimento prévio do documento.

O projeto propõe transformar esse acervo em registros estruturados, com metadados, situação e histórico visíveis.

## A experiência demonstrada

| Recurso | Como apoia a consulta |
| --- | --- |
| Pesquisa livre | Localiza termos em títulos, ementas, palavras-chave e referências, sem diferenciar acentos ou maiúsculas |
| Filtros por tema e situação | Permitem combinar classificação temática com registros vigentes ou inativos |
| Detalhamento | Reúne conteúdo e metadados do registro em uma janela de consulta |
| Histórico de versões | Exibe datas e resumos das versões incluídas nos dados demonstrativos |
| Identificação de inativos | Mantém registros consultáveis com sinalização de sua situação |
| Cópia e impressão | Facilita reutilizar o texto demonstrativo ou salvar a coleção em PDF pelo navegador |

A consulta ao histórico não equivale a um editor de versões: a demonstração lê dados preparados em JSON e não permite cadastrar, alterar ou inativar registros.

## Duas camadas do projeto

**Demonstração pública:** HTML, CSS, JavaScript e JSON fictício, com pesquisa e apresentação executadas no navegador, sem login nem conexão com planilhas institucionais.

**Arquitetura de referência:** Google Apps Script e Google Sheets, com desenho de permissões, atualização e preservação de versões. O repositório disponibiliza uma amostra sanitizada de Apps Script; ela não representa a publicação integral de uma aplicação administrativa.

[Entender a separação entre demonstração e arquitetura](./arquitetura.md)

## Meu papel no projeto

Conforme o estudo de caso publicado no repositório de origem:

- Levantamento progressivo dos requisitos.
- Modelagem dos fluxos de acesso e validação.
- Definição da experiência de pesquisa.
- Desenho das regras de versionamento e inativação.
- Testes iterativos com usuários.
- Documentação da solução e de seus controles de segurança.

Esta apresentação não atribui métricas aos testes nem afirma implantação ou resultados institucionais.

## O que este projeto demonstra no portfólio

Capacidade de traduzir um problema de gestão do conhecimento em requisitos, fluxos de consulta, classificação de informações e decisões de arquitetura. O foco não é apenas disponibilizar documentos, mas tornar explícitas a situação de um registro e a necessidade de preservar seu histórico.

## Organização e continuidade

Esta pasta reúne a apresentação do projeto no mesmo formato dos demais estudos do portfólio. O código e a demonstração permanecem no [repositório próprio](https://github.com/AlessandraGarcia4640/gestao-de-precedentes-Demo), sem duplicação ou mudança de hospedagem.

**Base desta apresentação:** documentação e código público consultados em agosto de 2026. A reorganização não alterou a aplicação e não incluiu teste interativo completo no navegador.
