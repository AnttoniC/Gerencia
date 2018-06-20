# Zabbix – Ferramenta de Monitoramento  
<br>

![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/zab2.jpg)

## Equipe
[Antonio Carlos](https://github.com/AnttoniC/Seguranca-da-Informacao)<br>
[Jefté de Sousa](https://github.com/bassebete/information-security)

## Introdução ao Zabbix
O Zabbix oferece portabilidade a diversos sistemas operacionais desde Linux,Solaris,HP-UX,AIX,FreeBSD,OpenBSD,NetBSD,Mac OS X,Windows,e outros.Disponibilizando agentes aos mais diversos sistemas operacionais,permitindo o monitoramento entre diferentes plataformas.<br>

Entretanto existe uma dependência em relação à estrutura do Zabbix, visto que o mesmo foi projetado com o intuito de ser uma ferramenta Open Source, seu servidor necessariamente deve ser hospedado em uma máquina com o Linux ou Mac OS, visto que não existe um pacote do servidor disponível para as versões do Windows.

## Preparação do Ambiente
Laboratório da E.E.E.P.Maria Cavalcante Costa

![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/am1.jpeg)

Preparamos as máquinas do laboratório da E.E.E.P.Maria Cavalcante Costa para rodar o Zabbix agente no windows, já que a maioria das aulas eram feita nesses sistema.<br> 
Primeiramente verificamos quantas redes as máquinas do laboratório estavam usando. Logo após fazermos isso configuramos algumas dependência que seriam necessária para fazer o monitoramento do laboratório.


## Instalação e Configuração
A primeira coisa que fizemos foi a instalação do servidor zabbix através do virtualbox.<br>

Servidor Zabbix: O servidor é responsável pela coleta e o armazenamento dos dados monitorados. Como já vimos o servidor deve ser necessariamente hospedado em uma máquina com o sistema operacional baseado na família do Unix (Linux ou Mac OS).<br>

Depois fizemos as instalações do agente zabbix no windows no laboratório.<br>
Agente Zabbix: O agente é responsável por repassar todas as informações que foram coletadas do sistema operacionais em qual está rodando para o servidor. O agente permanece instalado na máquina e rodando como daemon ou serviço, e assim que o servidor solicita alguma requisição o agente processa a requisição e retorna os dados solicitados.

## Etapa 1 - Baixar o Pacote do Zabbix Agente
[link para download](https://www.zabbix.com/download_agents)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/ins0.png)

## Etapa 2 - Configuração do Zabbix Agente
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/Ins1.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/Ins2.png)

## Etapa 3 - Liberar Porta(10050) no Firewall 

![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/por2.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/por3.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/por4.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/por5.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/por6.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/por7.png)

## Etapa 5 - Configuração do Zabbix Agente
`# instalar`
`zabbix_agentd.exe -c zabbix_agentd.conf -i`

`# iniciar serviço`
`zabbix_agendt.exe -s`

`# parar serviço`
`zabbix_agentd.exe -x`

![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/ins4.png)

## Monitorando Windows via Agente

A seguir veremos algumas das telas de monitoramento dos dados coletados pelo servidor.
Tela ininial e Grupo de host:<br>
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/n1.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/n2.png)

Uso de processamento da CPU e da Memória:<br>
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/gr2.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/gr03.png)

Uso do tráfego na rede e capacidade de processamento da CPU:<br>
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/tra.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/gr00.png)

Tela com as opções de monitoramento dos hosts:
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/gr7.png)
![img](https://github.com/AnttoniC/Gerencia/blob/master/Img/gr7.png)




