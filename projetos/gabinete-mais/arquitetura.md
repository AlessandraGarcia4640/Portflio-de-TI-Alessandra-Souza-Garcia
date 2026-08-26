# Gabinete+ — arquitetura e estágio técnico

[Voltar à apresentação](./README.md)

> A análise descreve a cópia de desenvolvimento recebida em agosto de 2026. Os arquivos foram inspecionados, mas a aplicação, a integração contínua e o banco não foram executados para produzir esta apresentação.

## Organização presente na base

O projeto utiliza um monorepo pnpm com três unidades principais:

| Diretório da base privada | Responsabilidade | Evidência na cópia revisada |
|---|---|---|
| `apps/mobile` | Interface mobile | Estrutura Expo/React Native com navegação de exemplo; não contém os módulos funcionais de gestão. |
| `apps/api` | API HTTP | Aplicação Express com rota `/health`, validação da resposta e tratamento de erros. |
| `packages/shared` | Contratos compartilhados | Esquema da resposta de saúde da API. |

Os caminhos acima descrevem o projeto privado; não são links para código publicado nesta pasta.

## O que está implementado e o que é intenção

| Área | Presente no código revisado | Ainda necessário |
|---|---|---|
| API | Rota de verificação `/health` e um teste dessa rota | Rotas de usuários, atividades, tarefas e substituições. |
| Banco | Modelo `User`, enumeração de perfis e migração inicial | Modelagem dos módulos de negócio, vínculos temporais e histórico. |
| Autenticação | Esquema de validação de formulário; modelo com campo de hash de senha | Fluxo de autenticação, gestão segura de sessão e autorização no servidor. |
| Aplicativo | Telas iniciais do template Expo e componentes auxiliares | Telas próprias do Gabinete+ e integração funcional com a API. |
| Dados de exemplo | Arquivo de inicialização reservado para dados fictícios | Criação efetiva de uma base demonstrativa isolada. |
| Qualidade | Scripts de lint e tipos, teste da API e configuração de CI | Execução verificada, testes de negócio, permissões e interface. |

O estado de sessão inicial guarda apenas um nome de usuário. Ele não implementa autenticação. O comando de testes mobile é um aviso de implementação futura, não uma suíte de testes.

## Arquitetura-alvo

As seguintes responsabilidades são **propostas para as próximas etapas**, não integrações já comprovadas:

| Componente | Responsabilidade prevista |
|---|---|
| Aplicativo mobile | Apresentar tarefas, instruções, equipe e transições conforme o contexto do usuário. |
| API | Validar entradas, autenticar, verificar permissões e executar regras de negócio. |
| PostgreSQL e Prisma | Persistir entidades, vínculos e registros históricos. |
| Contratos compartilhados | Manter tipos e esquemas consistentes entre camadas quando aplicável. |

## Decisões e limites

**Monorepo:** a decisão de reunir mobile, API e código compartilhado está registrada na base. A organização permite coordenar mudanças entre camadas; não elimina a necessidade de testes e limites claros entre os pacotes.

**Perfis e substituições:** a documentação funcional prevê mudança de função e acesso temporário. O modelo atual de usuário ainda não representa essa evolução histórica. Será necessário definir entidades e regras antes de implementar as telas correspondentes.

**Ambiente local:** há configuração de PostgreSQL em Docker Compose e credenciais demonstrativas de desenvolvimento. Essa configuração não é apresentada como adequada para produção e não foi incluída nesta versão pública de apresentação.

**Dependências:** a base contém arquivo de travamento de versões, mas diversas dependências são declaradas como `latest`. A compatibilidade e a reprodutibilidade devem ser verificadas antes de publicar instruções de execução ou uma demonstração operacional.

## Segurança a implementar e verificar

- Autorizar operações no servidor, sem depender apenas de esconder botões.
- Definir o ciclo de concessão e revogação de acessos temporários.
- Registrar alterações de responsável e de conteúdo com informações proporcionais à finalidade.
- Evitar credenciais e dados reais em código, registros de teste e exemplos.
- Testar isolamento de usuários e transições de responsabilidade.
- Separar ambientes de desenvolvimento, demonstração e eventual uso institucional.

Esta lista é um plano de trabalho. Não constitui certificação de segurança nem afirma conformidade ou aprovação institucional.
