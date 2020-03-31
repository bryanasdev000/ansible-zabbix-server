# Playbook para implantação de Zabbix Server 4.4 com PostgreSQL utilizando a extensão do TimescaleDB.

## HOSTS
Para executar essa playbook será necessário como primeiro passo ajustar o arquivo 'hosts' dentro do diretório "*inventory*" para informar quais serão os servidores que a role executará as tarefas.
É importante definir as maquinas serão **SERVER** e as que serão **DB**, separando-as nos respectivos grupos também, no momento essa playbook só é suportadada para o centOS 7.

> * allhosts:
>
> é o grupo onde deverá conter todas a maquinas que farão parte da execução;
>
> * zabbix_server:
>
> é o grupo que deverá conter a máquina que será o servidor do Zabbix;
>
> * zabbix_db:
>
> é o grupo que deverá conter a máquina que será o banco de dados do Zabbix;


Será preciso também inserir os valores de usuário (FreeIPA) e senha que serão utilizados para se conectar e executar os comandos como sudo, nos parametros:

> ansible_ssh_user
>
> ansible_sudo_pass

## Variáveis
Este ponto é muito importante e **NÃO PODE SER IGNORADO**, aqui você irá definir os padrões de instalação e configuração desejados no projeto, tais como:

* Versão do Zabbix;
* Versão do PostgreSQL
* Usuário e Senha do banco de dados;
* Porta do serviço;
* Time Zone;
* Configuração de HBA do PostgreSQL;


Criado por [Rauny Moreira](https://www.linkedin.com/in/rauny-moreira/).

