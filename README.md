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

### Passo 1 - Permissões e Diretórios

Com o Virtual Box instalado (clique [Aqui](https://www.oracle.com/br/virtualization/solutions/try-oracle-vm-virtualbox/?source=:ad:pas:go:dg:a_lad:71700000086180912-58700007355810352-p65903375090:RC_WWMK220429P00062:PORT&SC=:ad:pas:go:dg:a_lad::RC_WWMK220429P00062:PORT:&gclid=Cj0KCQjwrs2XBhDjARIsAHVymmT-qYVIlQKAP6JNYxqoUaCuaH1PaELOxdzk_V2tUpVbWLa8OdAQZsQaAjqgEALw_wcB&gclsrc=aw.ds) para baixar o Virtual Box), criar uma pasta onde será contida a .iso do S.O. Para isso, deve-se entrar no terminal do linux e digitar o comando `su redes` para entrar no Usuário redes, que contém permissões de administrador.
Depois, seguir os comandos: 
```
sudo mkdir /grupo2
cd /grupo2
mkdir images
cd images
mkdir original
```
Para criar a pasta `grupo2` na raiz e as subpastas `images/original` onde ficará a .iso, e 
```
cd /
mkdir grupo2/VM
mkdir grupo2/VM/914
mkdir grupo2/VM/914/<Prof. Alaelson<3 > # substituir <Prof. Alaelson<3 > pelo nome do integrante
```
 
 depois
`
scp aluno@192.168.101.10:~/Public/iso-images/ubuntu-server-mini.ova /labredes/images/original
`
Para baixar o arquivo .ova do computador do Prof. Alaelson :heart:

Modificando as permissões de arquivos e pastas:
```
sudo chown -R nobody:nogroup /grupo2
sudo chgrp -R redes /grupo2
sudo chmod -R 771 /grupo2 
```

### Passo2 - Rede Ponto a Ponto com Duas Máquinas Virtuais

Instalar a extensão do VirtualBox através dos comandos:
```
su redes
sudo apt install virtualbox-ext-pack
```
No Virtual Box, selecionar a opção Importar Appliance, dentro da opção Arquivo (Figura 1)

#figura 1

e criar uma VM com o .ova (Figura 2)

#figura2

Depois, instalar o net-tools no terminal de ambas as máquinas:
`
sudo apt install net-tools -y
`
Para que a VMs utilizem a mesma rede interna é necessário acessar as configurações de Rede de cada VM e selecionar o modo rede interna e definir o nome da rede, vamos escolher grupo2 como nome da nossa rede virtual. Utilize o mesmo nome nas duas VMs (Figura3).

#figura 3

