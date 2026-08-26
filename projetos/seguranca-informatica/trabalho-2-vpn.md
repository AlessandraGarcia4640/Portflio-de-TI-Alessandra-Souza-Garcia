# Trabalho 2 · VPN e identidade digital

[Visão geral dos laboratórios](./README.md)

[Baixar trabalho completo — ZIP revisado](./materiais/trabalho-pratico-2-publico.zip?raw=true) · [Nota sobre a revisão](./materiais/README.md)

## Objetivo

Exercitar o acesso remoto no cenário *road warrior*: um cliente externo conecta-se a uma rede interna por VPN, com certificados e uma camada adicional de autenticação.

**Tecnologias:** CentOS, VirtualBox, OpenVPN, OpenSSL, PKI, X.509, OCSP, Apache, PAM e TOTP com Google Authenticator.

## Componentes e responsabilidades

| Componente | Função no laboratório |
|---|---|
| Cliente remoto | Iniciar a conexão e apresentar as credenciais exigidas |
| Gateway OpenVPN | Estabelecer o túnel e encaminhar o tráfego autorizado |
| Servidor interno | Hospedar os serviços de laboratório, incluindo Apache e responder OCSP |
| Autoridade certificadora | Emitir certificados e registrar seu estado de revogação |
| Integração PAM/TOTP | Acrescentar a verificação de autenticação multifator |

## Trabalho desenvolvido pela equipe

- Preparação de três máquinas virtuais e das redes do cenário.
- Criação de uma autoridade certificadora de laboratório e emissão de certificados.
- Configuração de servidor e cliente OpenVPN.
- Consulta OCSP e exercício de revogação de certificado.
- Integração de autenticação multifator com PAM e TOTP.
- Configuração de acesso ao Apache com certificados e autenticação adicional.

## Resultados registrados no relatório

| Cenário | Resultado descrito | Referência |
|---|---|---|
| Conexão VPN inicial | Interface de túnel ativa e teste de conectividade bem-sucedido | Páginas 9–11 |
| Certificado válido | Consulta OCSP com estado `good` e conexão aceita | Páginas 12–13 |
| Certificado revogado | Estado `revoked` e interrupção da autenticação relatada | Páginas 14–15 |
| Segundo fator na VPN | Autenticação concluída no cenário apresentado | Páginas 15–17 |
| Acesso ao Apache | Cenários de certificado, autenticação válida e credenciais inválidas documentados | Páginas 20–22 |

## Aprendizados e limites

O foco é compreender o ciclo de confiança: emitir uma identidade, verificar sua validade, restringir o acesso e revogar uma autorização anteriormente concedida.

Os resultados acima foram relatados pela equipe; não foram reproduzidos durante a organização do portfólio. O material não é apresentado como implementação completa ou auditada de uma PKI. Os trechos de integração OCSP e PAM exigiriam revisão e novos testes antes de qualquer reutilização operacional.

Nesta apresentação não são distribuídos certificados de cliente, chaves privadas, senhas, segredos TOTP, códigos de recuperação ou capturas brutas dos autenticadores. Isso preserva o valor técnico da descrição sem replicar material de autenticação.

## Fontes

`TP2.pdf`, 23 páginas; arquivos `server.conf.txt` e `cliente.conf.txt`. O pacote complementar contém uma cópia revisada do relatório e as configurações originais, com nota das ocultações.

[Anterior: redes](./trabalho-1-redes.md) · [Próximo: segurança web](./trabalho-3-seguranca-web.md)
