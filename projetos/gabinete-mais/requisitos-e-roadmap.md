# Gabinete+ — requisitos e próximos passos

[Voltar à apresentação](./README.md)

## Perfis propostos

Os perfis abaixo representam papéis genéricos de uso, não pessoas reais:

| Perfil | Necessidade principal |
|---|---|
| Gestão | Consultar visão consolidada, prioridades e pendências. |
| Coordenação | Organizar atividades, distribuir trabalho e acompanhar transições. |
| Execução | Consultar instruções e registrar andamento de tarefas atribuídas. |
| Substituição temporária | Assumir responsabilidades por período definido e devolver o contexto ao término. |

A matriz final de permissões depende de validação. O papel temporário não deve ser tratado como acesso permanente.

## Requisitos funcionais iniciais

| ID | Requisito proposto | Critério de aceitação sugerido para a implementação |
|---|---|---|
| RF01 | Cadastrar atividades com instruções | Uma atividade salva mantém nome, instruções e situação consultáveis. |
| RF02 | Atribuir tarefas com prazo | A tarefa identifica responsável, prazo e estado atual. |
| RF03 | Consultar e atualizar checklists | Uma atualização autorizada preserva o vínculo com a tarefa e seu registro de execução. |
| RF04 | Transferir responsabilidades | A transferência registra responsável anterior, novo responsável, momento e autor. |
| RF05 | Definir substituição temporária | O sistema valida o período e impede conflitos conforme as regras aprovadas. |
| RF06 | Encerrar substituição | O encerramento revoga o acesso temporário e preserva o registro das pendências. |
| RF07 | Preservar histórico | Mudanças relevantes permanecem consultáveis pelos perfis autorizados. |
| RF08 | Gerar ocorrências de atividades recorrentes | A geração respeita a frequência configurada, sem criar duplicidades. |

Os critérios são uma proposta pública para orientar testes futuros. Não foram apresentados como testes executados.

## Critérios transversais

- Linguagem clara e navegação consistente em telas pequenas.
- Ações autorizadas também no servidor.
- Uso de dados fictícios em demonstrações e testes públicos.
- Confirmação em operações com impacto sobre responsabilidades.
- Preservação de contexto e rastreabilidade nas transições.
- Avaliação de acessibilidade e testes com usuários antes de afirmar adequação de uso.

## Próximos passos

| Etapa | Resultado esperado | Situação da cópia revisada |
|---|---|---|
| Definição do problema e requisitos iniciais | Perfis, catálogo de atividades e navegação documentados | Material existente. |
| Wireframes e preparação de validação | Telas de baixa fidelidade e cenários para discussão | Material existente; validação conclusiva não comprovada nesta revisão. |
| Estrutura técnica | Mobile, API, persistência inicial e ferramentas | Base inicial presente, sem execução verificada nesta revisão. |
| Fluxo mínimo de tarefas | Cadastrar, consultar, atribuir e concluir tarefas | A implementar. |
| Autenticação e permissões | Identificação e autorização verificadas no servidor | A implementar. |
| Substituições e histórico | Transferência temporária com encerramento e rastreabilidade | A implementar. |
| Validação e avaliação | Testes de uso, testes técnicos e indicadores comparáveis | A planejar e executar. |

As etapas não constituem promessa de prazo. A sequência deve ser ajustada conforme validação dos requisitos e dependências técnicas.

## Limites desta apresentação

Esta pasta publica documentação resumida e imagens conceituais. Não oferece login, backend, base de dados, exportação ou operações de escrita. Os elementos que parecem botões nas imagens não são interativos.

Não são distribuídos o pacote original de desenvolvimento, os materiais brutos de pesquisa nem configurações internas. O projeto privado não é necessário para ler esta apresentação.
