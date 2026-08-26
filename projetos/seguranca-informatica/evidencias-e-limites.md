# Fontes, evidências e limites

[Visão geral dos laboratórios](./README.md)

## Base documental

| Trabalho | Material consultado | Conteúdo selecionado para a apresentação |
|---|---|---|
| TP1 | Relatório de 11 páginas; comandos IPTables e regras Suricata | Topologia, controles de rede, alertas e resposta manual |
| TP2 | Relatório de 23 páginas; configurações de servidor e cliente VPN | Arquitetura, ciclo de certificados e cenários de autenticação |
| TP3 | Relatório de 114 páginas; configurações Apache e ModSecurity | Metodologia, comparação entre cenários, logs de bloqueio e limites |

**Autoria dos relatórios:** Alessandra Souza Garcia e Pedro Bampi Gollo. A apresentação preserva o caráter coletivo dos trabalhos, sem atribuir tarefas individuais que os documentos não discriminam.

## Critério editorial

- **Configuração documentada:** há comandos ou parâmetros nos materiais; isso não equivale a comprovar sua execução atual.
- **Resultado relatado:** a equipe descreve o comportamento de um teste, eventualmente acompanhado de captura.
- **Evidência selecionada:** é indicada uma página ou figura que sustenta uma afirmação específica.
- **Limitação:** o material não permite uma conclusão mais ampla, contém divergência ou declara algo fora de escopo.

O processo de organização do portfólio não incluiu execução de scripts, varredura de alvos, validação de credenciais nem reconstrução das máquinas virtuais. A revisão foi documental e não constitui auditoria integral dos ambientes ou dos arquivos originais.

## Ajustes de precisão

| Ponto observado | Como foi apresentado |
|---|---|
| TP1 menciona prevenção automática no objetivo, mas descreve bloqueio manual na seção 5.3 | Detecção por Suricata e resposta manual por IPTables |
| TP1 combina política padrão restritiva com exceções de diferentes abrangências | Políticas e exceções documentadas, sem garantir mínimo privilégio efetivo em todos os fluxos |
| TP2 apresenta integração de certificados, OCSP e PAM | Exercício de integração e resultados relatados, sem certificação da solução |
| TP3 contém classificações divergentes entre fases e referências diferentes à versão do CRS | Seleção de evidências específicas, sem afirmar cobertura completa ou reprodução exata do ambiente |
| TP3 registra respostas 403 para determinadas requisições | Bloqueio observado nesses cenários, sem generalizar para ausência de vulnerabilidades |

## Publicação responsável

Além das sínteses em Markdown e dos diagramas conceituais, a subpasta [materiais](./materiais/README.md) contém três ZIPs com cópias públicas revisadas dos relatórios e arquivos de configuração. As áreas com dados de autenticação identificados foram removidas do conteúdo dos PDFs e marcadas em cinza, sem substituir o conteúdo por evidências inventadas.

Nas sínteses, endereços e identificadores de sessão foram omitidos por não serem necessários para demonstrar o aprendizado. Nos pacotes, foram preservados os endereços de laboratório e as configurações, mas ocultadas matrículas, contatos pessoais e áreas com valores de autenticação identificados. Não foi disponibilizado um ambiente vulnerável na internet.

**Limite desta entrega:** os ZIPs antigos da raiz foram substituídos, na versão atual, pelos pacotes revisados em `materiais/`. Os originais permanecem no histórico, que não foi reescrito. A revisão não invalida credenciais e não deve ser interpretada como uma declaração de que todo o histórico do repositório está livre de dados sensíveis.

## Possíveis evoluções

- Ampliar a curadoria de evidências visuais revisadas, sem credenciais ou identificadores desnecessários.
- Separar resultados esperados e observados em uma matriz de testes reproduzível.
- Confirmar as versões efetivamente usadas e resolver divergências dos relatórios.
- Registrar a contribuição individual de cada integrante, após confirmação da equipe.
- Recriar configurações exemplificativas com dados sintéticos e validá-las exclusivamente em laboratório isolado.

[Voltar ao portfólio](../../README.md)
