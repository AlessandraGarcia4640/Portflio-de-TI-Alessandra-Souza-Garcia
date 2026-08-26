# Fundamentos de Segurança Informática

Laboratórios acadêmicos de redes, identidade digital e segurança de aplicações web, realizados em equipe na Universidade de Coimbra.

**Autoria dos trabalhos:** Alessandra Souza Garcia e Pedro Bampi Gollo.  
**Contexto:** mobilidade acadêmica, 2026.  
**Situação:** trabalhos concluídos em ambiente de laboratório; apresentação documental para portfólio.

> Da infraestrutura à aplicação: três exercícios para compreender como configurar controles, observar seu comportamento e reconhecer seus limites. Não se trata de um serviço de segurança em produção nem de uma demonstração pública dos ambientes vulneráveis.

## Explore os trabalhos

| Laboratório | Pergunta central | Entregas documentadas |
|---|---|---|
| [01 · Redes e defesa perimetral](./trabalho-1-redes.md) | Como separar zonas de rede e acompanhar tráfego suspeito? | Topologia virtual, firewall, NAT, regras Suricata e plano de testes |
| [02 · VPN e identidade digital](./trabalho-2-vpn.md) | Como controlar o acesso remoto e lidar com credenciais revogadas? | OpenVPN, autoridade certificadora de laboratório, certificados, OCSP e autenticação multifator |
| [03 · Segurança web e WAF](./trabalho-3-seguranca-web.md) | O que muda quando uma aplicação vulnerável recebe uma camada de filtragem HTTP? | Testes com OWASP ZAP, comparação antes/depois, Apache, ModSecurity e análise de limitações |

## Competências exercitadas

- **Redes e sistemas:** Linux, virtualização, segmentação, roteamento e filtragem de tráfego.
- **Identidade e acesso:** PKI, certificados X.509, revogação, VPN e autenticação multifator.
- **Segurança web:** testes em aplicação intencionalmente vulnerável, inspeção HTTP e leitura de logs.
- **Análise e documentação:** relacionar objetivos, configurações, resultados registrados e limitações.

**Tecnologias:** CentOS Stream 9, VirtualBox, IPTables/Netfilter, Suricata, OpenVPN, OpenSSL, Apache, PAM, Google Authenticator, Kali Linux, OWASP ZAP, OWASP Juice Shop, ModSecurity e OWASP CRS.

## Como interpretar esta apresentação

Os resumos foram elaborados a partir dos relatórios e arquivos de configuração entregues pela equipe. A revisão para o portfólio foi documental: os laboratórios não foram reconstruídos nem os testes repetidos. Resultados mencionados são os registrados nos materiais de origem, não uma certificação independente de segurança.

A autoria é compartilhada. A documentação disponível não discrimina a contribuição individual em cada atividade; por isso, não se atribui a implementação integral a uma única pessoa.

Estas páginas não reproduzem senhas, tokens, códigos de recuperação, matrículas, endereços pessoais ou capturas brutas de autenticação. Os documentos originais não foram incorporados a esta pasta. Esta seleção editorial não equivale à remoção de arquivos antigos ou à limpeza do histórico do repositório.

[Consultar fontes, evidências e limites](./evidencias-e-limites.md) · [Voltar ao portfólio](../../README.md)
