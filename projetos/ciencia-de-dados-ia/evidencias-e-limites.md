# Evidências, limites e evolução

[Apresentação](./README.md) · [Arquitetura](./arquitetura.md)

Revisão documental e técnica realizada em 26 de agosto de 2026 sobre os materiais fornecidos para organizar o portfólio. O código original não foi modificado.

## Classificação dos materiais

| Material recebido | Papel nesta revisão |
| --- | --- |
| `Trabalho Projeto II.zip` | Entrega com código, dados de exemplo, banco, modelo e relatório identificado em nome da estudante |
| `IIACD_IECD2026_Projeto_II(1).pdf` | Enunciado de requisitos do Projeto II; não comprova sua implementação |
| `Projeto_cienciaDados_202526.pdf` | Enunciado do Projeto I, com etapas de preparação, classificação e avaliação |
| `PROJETO.txt` | Matriz numérica com 600 linhas e sete colunas, compatível com as dimensões descritas no enunciado |
| Fichas `FP_II_1_res` e `FP_II_2_res` | Resoluções didáticas de NumPy e Pandas, com autoria docente; não tratadas como projeto autoral |
| `municipios.csv` e `municipios.json` | Arquivos auxiliares recebidos; integração com o sistema de oficina não demonstrada nos importadores analisados |

As fichas identificam Alberto Cardoso, Jorge Henriques, Diogo Pessoa e Vítor Cerqueira como autores. Esta documentação não redistribui esses materiais.

## O que foi efetivamente verificado

- Leitura do enunciado, do relatório e dos arquivos Python da entrega.
- Análise sintática dos arquivos Python, sem executar a aplicação.
- Leitura do banco SQLite recebido em memória: 2 oficinas, 4 veículos, 8 registos técnicos, 12 previsões e nenhuma decisão do mecânico.
- Conferência da dimensão do arquivo numérico do Projeto I.
- Inspeção textual do artefato de modelo, sem desserializá-lo.
- Reprodução isolada da consulta do relatório contra o esquema declarado: erro `no such table: revisao`.

Essas contagens descrevem o banco recebido, não uma taxa de sucesso. Doze previsões armazenadas não equivalem a doze veículos nem comprovam acerto do modelo.

## Limitações identificadas

| Ponto | Evidência e consequência | Evolução sugerida |
| --- | --- | --- |
| Relatório estatístico | Consulta `revisao.previsao_modelo`, mas o esquema utiliza `previsao_revisao.necessita_revisao_prevista` | Corrigir a consulta e definir contagem por veículo, oficina e período |
| Agregação por oficina | Conta veículos globalmente e usa a população da primeira oficina | Filtrar a oficina e estabelecer o significado do indicador per capita |
| Reimportação | A inserção de registos técnicos não possui prevenção de duplicação por evento | Definir chave do evento e testar reimportação sem duplicação |
| Integridade referencial | Há chaves estrangeiras declaradas, sem habilitação explícita na conexão | Ativar a verificação e definir tratamento de exclusões e dados existentes |
| Decisão humana | Tabela criada, mas sem operação correspondente identificada no menu | Implementar e testar o registro da decisão do mecânico |
| Treinamento e avaliação | Ausência de script de treinamento, partição de dados e métricas | Recuperar o Projeto I antes de afirmar qualidade preditiva |
| Pré-processamento | Importadores fazem conversão de tipos, sem tratamento completo de faltantes ou anomalias | Documentar e testar as regras, inclusive sua consistência com o treinamento |
| Reprodutibilidade | Não há dependências fixadas nem execução integral validada nesta revisão | Preparar ambiente isolado, exemplos públicos e testes |

## O que ainda não é possível afirmar

Não há evidência suficiente para declarar uma taxa de acerto, sensibilidade, especificidade ou capacidade de generalização do modelo. Também não é possível afirmar que os quatro classificadores pedidos no Projeto I foram implementados: o material recebido inclui o enunciado, mas não as respectivas soluções.

Não foi demonstrado um fluxo completo de atualização de fichas, controle de acesso por perfil ou decisão final do mecânico. Funcionalidades solicitadas no enunciado são distintas das funcionalidades identificadas no código.

O uso de um modelo em apoio à decisão não substitui inspeção profissional do veículo.

## Publicação responsável

Nesta etapa foram publicados apenas textos de apresentação e revisão, sem reproduzir os arquivos brutos.

Antes de uma versão pública executável:

1. Confirmar a autoria e os direitos de distribuição do código e dos dados.
2. Remover o identificador acadêmico do relatório e revisar quaisquer dados identificáveis.
3. Substituir exemplos cuja origem não esteja confirmada por dados explicitamente fictícios.
4. Excluir banco preenchido, caches, configurações locais e binários desnecessários do pacote público.
5. Recuperar o treinamento e preferir regenerar o modelo a distribuir um artefato sem procedência e ambiente documentados.
6. Testar o fluxo completo e registrar resultados observados, separando-os das expectativas do enunciado.

## Próxima entrega recomendada

Uma demonstração reproduzível com dados fictícios, importação sem duplicações, consultas consistentes e treinamento documentado. A documentação atual é um estudo de caso da entrega acadêmica, não uma declaração de que essa evolução já foi realizada.
