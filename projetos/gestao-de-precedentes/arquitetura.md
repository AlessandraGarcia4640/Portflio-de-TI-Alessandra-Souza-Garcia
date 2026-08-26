# Arquitetura e escopo | Gestão de Precedentes

[Apresentação](./README.md) · [Estudo de caso](./estudo-de-caso.md) · [Segurança e privacidade](./seguranca-e-privacidade.md)

## Demonstração pública e arquitetura de referência

| Aspecto | Demonstração pública | Arquitetura de referência |
| --- | --- | --- |
| Interface | HTML, CSS e JavaScript | Interface web servida por Apps Script |
| Dados | Arquivo JSON fictício | Google Sheets como base estruturada |
| Pesquisa | Filtragem no navegador | Pesquisa na camada de aplicação |
| Acesso | Consulta sem login | Separação entre consulta e administração identificada |
| Alterações | Sem escrita ou edição | Regras de validação, versionamento e inativação descritas na documentação |
| Histórico | Leitura de versões demonstrativas já registradas | Preservação de redações e rastreabilidade como requisitos |
| Publicação | Site estático no GitHub Pages | Ambiente independente, não acessado nesta revisão |

A demonstração não utiliza o Apps Script como backend. A existência de código de exemplo não comprova que toda a arquitetura de referência esteja implementada ou implantada.

## Componentes consultados

| Arquivo no repositório de origem | Responsabilidade |
| --- | --- |
| `index.html` | Estrutura da página, campos de pesquisa, filtros e janelas de detalhe |
| `styles.css` | Estilos da interface |
| `app.js` | Carregamento do JSON, filtragem, ordenação, detalhes, histórico, cópia e impressão |
| `precedentes-demo.json` | Coleção de registros demonstrativos |
| `Code.sample.gs` | Amostra sanitizada de leitura de planilha, busca e verificação de validadores |
| `appsscript.example.json` | Arquivo de configuração de exemplo para Apps Script |

Os arquivos acima permanecem no [repositório da demonstração](https://github.com/AlessandraGarcia4640/gestao-de-precedentes-Demo); não foram transferidos para o portfólio.

## Pesquisa e apresentação

O JavaScript carrega `precedentes-demo.json` e mantém os registros em memória. A busca normaliza os termos, removendo acentos e diferenças entre maiúsculas e minúsculas, e exige a presença de todos os termos informados no conteúdo pesquisável.

Filtros por tema e situação são combinados com a busca. A listagem de consulta é ordenada por identificador. Detalhes e histórico são apresentados em elementos de diálogo; a cópia utiliza a área de transferência, e a exportação chama a impressão do navegador.

## Dados e versionamento

Os registros utilizados pela interface contêm identificador, título, ementa, tema, resultado, situação, versão e referências. Palavras-chave e histórico são utilizados quando presentes; a data de inativação é exibida quando disponível.

O histórico público mostra datas e resumos de versões. Não há gravação de alterações, auditoria de usuários ou manutenção de versões no site estático.

## Amostra de Apps Script

O exemplo publicado lê dados de uma planilha configurada por propriedade do script e verifica se o usuário pertence a uma lista configurada de validadores. Também inclui pesquisa textual e limite de resultados.

Não foram identificadas nessa amostra rotinas completas de criação, edição, inativação ou persistência de novas versões. As responsabilidades administrativas descritas na documentação devem ser lidas como arquitetura de referência, não como funcionalidades oferecidas pela demonstração.

## Escopo desta reorganização

Foram consultados o código e a documentação públicos. O endereço da demonstração foi obtido do campo de site do repositório, mas a disponibilidade e as interações no site publicado não foram validadas nesta etapa.

Nenhum código, configuração, dado ou implantação da aplicação foi alterado.

**Referências:** [JavaScript da demonstração](https://github.com/AlessandraGarcia4640/gestao-de-precedentes-Demo/blob/main/app.js), [amostra de Apps Script](https://github.com/AlessandraGarcia4640/gestao-de-precedentes-Demo/blob/main/Code.sample.gs) e [arquitetura original](https://github.com/AlessandraGarcia4640/gestao-de-precedentes-Demo/blob/main/arquitetura.md).
