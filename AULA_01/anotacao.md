## Anotações
Simular um ambiente real de produção
```mermaid
graph LR
A[Cliente] <--<b>dados-->B[servidor]
```
- Algo do mercado
- Administração de recursos
- Experiencia em servidores Linux 
## Servidor de arquvios 
Servidor educacional para arquvios, assim não dependendo da red externa 

```mermaid
graph TD
A[Servidor Senai
10.87.36.10]--Arquivos-->B[Nosso computador] 
```
## Servidor de desenvolvimento
---
- Cada aluno recebe o seu propio acesso.
- Cada máquina possui um endereço de IP diferente.
- 192.168.10.34
--- 
|Recurso|configuração|
|-------|------------|
|CPU|2 Cores|
|RAM|512Mb|
|Disco|6Gb|
|SOP| Ubuntu 26.04 LTS|
|Acesso|SSH (Secure Shell)
---
## Dados de acesso:

|Campo|valor|
|-----|------|
|IP Container| 192.168.10.34|
|Usuario|root|
|senha inicial|aluno01|
---
### Comando para visualizar uso de recursos:
```bash
htop    
```
### Comando para trocar a senha:
```bash
passwd
```
<br> 

## Banco de Dados
<B>Dados:</b> Tinformações isolados que não dizem muita coisa. EX: Platini, futebol, Chuteira.
<b>Informação:</b> Dados estruturados. EX: O platini comprou uma chuteira para jogar futebol.
- <b>Conhecimento:</b> O que podemos extrair à partir das informações. EX: O platini vai jogar futebol com a I1D35.

```mermaid
graph LR

A[Dado: Chuteira] --> B[Processamento] --> C[Informação: O cliente precisa de uma chuteira]
```
---
#### O fluxo normal de um banco de dados, está representado à seguir: 
```mermaid
graph LR
    A[Usuário] --> B[Aplicação] --> C[(Banco de Dados)]
```
---
<br>

> Por qual razão, as empresas não salvam os dados em arquivos comuns?
```mermaid
graph TD
A[Guardar dados] --> B[Banco de Dados]
A[Gurdar dados]--> C[Arquivos/Planilhas]
B --> B1[Vários usuários ao mesmo tempo]
B --> B2[Backup e sincronização]
B --> B3[Consultas otimizadas e rápidas]
C --> C1[Um arquivo por vez]
C --> C2[Backup ineficiente]
```
---

## SGBD
Sistema Gerenciador de Banco de Dados.
> POSTGRESQL: SGBD OpenSource  muito completo.
---
#### Primeiro começamos att os pacotes 
```bash
sudo apt upgrade && update -y
```
#### Para instalar o Postgresql:
```bash
sudo apt install -y postgresql
```

