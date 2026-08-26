# Gabinete+ — estudo de caso

[Voltar à apresentação](./README.md)

## 1. Contexto e problema

O projeto parte da necessidade de organizar rotinas e preservar conhecimento durante mudanças de função, férias e outros afastamentos. Quando as instruções ficam dispersas, quem assume uma responsabilidade precisa reconstruir o contexto: o que fazer, como fazer, o que está pendente e quem pode orientar.

A pergunta de projeto é: **como apoiar a continuidade das rotinas sem depender exclusivamente da memória e da disponibilidade de uma pessoa?**

Esta versão descreve o problema em termos gerais. Não divulga respostas de participantes nem detalhes de funcionamento de uma unidade específica.

## 2. Do problema aos requisitos

| Necessidade | Resposta proposta no produto |
|---|---|
| Localizar orientações de trabalho | Catálogo de atividades com instruções e checklists. |
| Saber o que está pendente | Lista de tarefas com situação, prazo e responsável. |
| Transferir trabalho sem perder contexto | Registro de mudança de responsável e justificativa. |
| Preparar uma substituição | Período definido, responsabilidades e acesso temporário. |
| Compreender o que ocorreu durante a ausência | Histórico e resumo de transição no encerramento. |

Essas relações orientam a concepção da solução. Não representam recursos já disponíveis para uso.

## 3. Decisões de desenho

### Separar atividade de tarefa

Uma **atividade** descreve uma rotina reutilizável. Uma **tarefa** é uma ocorrência concreta dessa rotina. A separação permite planejar instruções consistentes e acompanhar cada execução de forma independente.

Exemplo fictício: “Revisar roteiro de integração” é uma atividade. “Revisar a versão demonstrativa do roteiro” é uma tarefa atribuída à Equipe A, com prazo e situação próprios.

### Separar pessoa de função

O desenho funcional prevê que a pessoa possa mudar de função sem apagar o histórico. Essa é uma intenção de modelagem; o esquema de banco atual ainda contém apenas um modelo inicial de usuário com um campo de perfil.

### Tratar substituição como um período

Uma substituição não deve significar acesso permanente. A proposta prevê início, término, registro de responsabilidades e encerramento com devolução de contexto. As regras de permissão e conflito ainda precisam ser implementadas e testadas.

### Validar antes de ampliar a implementação

Os wireframes permitem discutir nomenclatura, campos e sequência de ações antes de construir os módulos completos. Existe material para conduzir essa validação; esta apresentação não afirma que todas as telas tenham sido aprovadas por usuários.

## 4. Percurso conceitual

1. A coordenação registra uma atividade e suas instruções.
2. Uma tarefa é criada e atribuída a um responsável.
3. O responsável consulta o checklist e registra a execução.
4. Se houver uma transição, as responsabilidades são transferidas com registro.
5. No encerramento, pendências e alterações permanecem consultáveis.

O percurso é planejado e usa exemplos genéricos, sem conexão com sistemas ou registros reais.

## 5. Como avaliar o valor

Antes de afirmar ganhos de eficiência, o projeto deverá estabelecer uma linha de base e testar cenários comparáveis. Indicadores possíveis para uma avaliação futura:

- tempo necessário para localizar uma orientação;
- proporção de cenários concluídos sem ajuda;
- dúvidas recorrentes durante uma substituição;
- tarefas devolvidas com contexto suficiente;
- percepção de clareza sobre responsabilidades.

São propostas de avaliação, sem metas ou resultados numéricos apresentados como comprovados.

## 6. Aprendizados que a apresentação evidencia

O projeto aproxima levantamento de requisitos, gestão do conhecimento e desenvolvimento de software. Mostra a importância de explicitar limites do produto, traduzir regras de trabalho em critérios verificáveis e tratar privacidade como parte da preparação do portfólio.

[Consultar a arquitetura](./arquitetura.md) · [Consultar requisitos e próximos passos](./requisitos-e-roadmap.md)
