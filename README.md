# Projeto do 2º Bimestre
## Introdução

Este repositório contém os passos a serem executados para a criação de Máquinas Virtuais pelo VirtualBox e a interconexão entre 8 máquinas virtuais por cabeamento Ethernet, criando um ambiente de rede virtualizada e permitindo o acesso de cada máquina virtual a partir de um Host

### Tabela de Informações

| Rede       |Máscara         | Gateway      | Broadcast    |
|------------|----------------|--------------|--------------|
|192.168.14.0|255.255.255.240 | 192.168.14.16| 192.168.14.31|

|Grupo 2     | Hostnames                  | FQDN                 | Apelidos    | EndereçosIPs                  |
| -----------| ---------------------------|----------------------|-------------| ------------------------------|
| Iago       |iago1<br> iago2             |grupo2-914.ifalara.net|ig1<br> ig2  |192.168.14.21<br>192.168.14.22 |
| Jhonathan  |jhonathan1<br> jhonathan2   |grupo2-914.ifalara.net|jh1<br> jh2  |192.168.14.19<br> 192.168.14.20|
| Joellen    |joellen1<br> joellen2       |grupo2-914.ifalara.net|joe1<br> joe2|192.168.14.17<br> 192.168.14.18|
| Josenilton |josenilton1<br> josenilton2 |grupo2-914.ifalara.net|jos1<br> jos2|192.168.14.23<br> 192.168.14.24|

| Memória | Processadores | Espaço em disco | Sistema Operacional |
|---------|---------------|-----------------|---------------------|
| 512MB   |      1        |      10GB       | Ubuntu (64-bit)     |

## Tutorial

### Passo 1

Com o Virtual Box instalado (clique [Aqui](https://www.oracle.com/br/virtualization/solutions/try-oracle-vm-virtualbox/?source=:ad:pas:go:dg:a_lad:71700000086180912-58700007355810352-p65903375090:RC_WWMK220429P00062:PORT&SC=:ad:pas:go:dg:a_lad::RC_WWMK220429P00062:PORT:&gclid=Cj0KCQjwrs2XBhDjARIsAHVymmT-qYVIlQKAP6JNYxqoUaCuaH1PaELOxdzk_V2tUpVbWLa8OdAQZsQaAjqgEALw_wcB&gclsrc=aw.ds) para baixar o Virtual Box)
