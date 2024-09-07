# CriandomaquinasVirtuaisnaAzure
Laboratório Criando máquinas Virtuais na Azure Treinamento Azure DIO 


//CONCEITO DE SLA EM AMBIENTE AZURE(CLOUD)

Os níveis de serviço do Azure (SLA) são os compromissos da Microsoft com a conectividade e o tempo de atividade. Cada serviço tem um SLA diferente, e às vezes, até mesmo SKUs dentro de um mesmo serviço podem ter SLAs diferentes. 
 
O SLA é um acordo vinculativo entre o prestador de serviços e o cliente, que normalmente inclui consequências para o não cumprimento das metas. 
 
Os SLAs geralmente se referem ao tempo de entrega ou nível de desempenho acordado no contrato. Alguns exemplos de métricas usadas para definir um SLA são: Porcentagem de tempo de atividade da rede, Tempo de atividade da capacidade, Disponibilidade de suporte. 
 
Para obter mais informações sobre os Contratos de Nível de Serviço para serviços online, consulte o site da Microsoft.

Tabela representativa do NÌVEL DE SLA por tempo de inatividade semana/mês 

SLA	        Tempo de inatividade por semana	          Tempo de inatividade por mês:


99%	        1,68 hora	                                7,2 horas
99,9%	      10,1 minutos	                            43,2 minutos
99,95%	    5 minutos	                                21,6 minutos
99,99%	    1,01 minuto	                              4,32 minutos


// Segue abaixo o link da documentação, Visão geral dos contratos de nível de serviço
    Benefícios dos contratos de nível de serviço
    Recursos dos contratos de nível de serviço

// https://learn.microsoft.com/pt-br/dynamics365/customer-service/use/overview-service-level-agreements#benefits-of-service-level-agreements

// Segue tutorial/etapa para criação de máquinas virtuais no AZURE

Para criar uma máquina virtual no Azure, é necessário seguir as seguintes etapas: 
 
1o. Primeiro criar conta no portal do AZURE https://portal.azure.com/ 
Obs.: (pode ser criada uma conta gratuita, para utilizar recursos básicos ofertados pelo ambiente, geralmente é uma contra de acesso TRIAL 30 (trinta) dias, para uso de estudos ou uma conta que voc~e só paga o que utilizar pelo recurso, que será debitado na sua fatura do seu cartão

2o. Com a conta criada, acesse AZURE SERVICES / HOME 
Obs.: nas opções de configurações no icone de uma engrenagem que fica no alto, na mesma direção aonde consta seu nome de login (email de acesso) você poderá estar alterando opções como idioma, aparência e etc
Obs.: eu recomendo manter o idioma em inglês por que os serviços ficam mais fácil de se entender quando for realizar a prova de certificação AZ-900

3o. Pesquisar por "máquinas virtuais" Virtual Machines
 
4o. Selecionar "Máquinas virtuais" em "Serviços" 
 
5o. Selecionar "Criar" e, em seguida, "Máquina virtual do Azure" 
 
Obs.: Preencher os detalhes básicos, como nome da máquina virtual, sistema operacional, tamanho e grupo de recursos (recomendo utilizar o documento oficial da MICROSOFT para poder criar sua(s) máquina(s) virtual(is) utilizando as melhores práticas)
link da documentação https://learn.microsoft.com/pt-pt/azure/virtual-machines/windows/quick-create-portal
 
6o. Configurar as opções de rede, discos e gerenciamento 
 
7o. Revisar as configurações e clicar em "Criar" 
 
8o. Na página de rede, é necessário liberar as portas para acesso RDP (conexão remota) e SSH (terminal). Isso evita problemas de firewall na conexão. 
 
Obs.: As Máquinas Virtuais do Azure são oferecidas em vários tipos e tamanhos para atender às necessidades do usuário.

Obs.: Para maiores informações sobre criação de máquinas virtuais (virtual machine), segue documento oficial da MIcrosoft Azure, detalhando todo o processo de criação, link abaixo
https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal
 
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

// Segue tutorial para uma melhor compreensão sobre zonas de disponibilidade

O Azure oferece algumas opções de disponibilidade, incluindo: 

Zonas de disponibilidade = 
São locais físicos exclusivos em uma região do Azure, que protegem os dados e aplicativos contra falhas no datacenter. Cada zona é composta por um ou mais datacenters com energia, resfriamento e rede independentes. 
 
Serviços com redundância de zona = 
Replicam ou distribuem os recursos automaticamente entre as zonas. Por exemplo, os dados são replicados em três zonas para que uma falha em uma zona não afete a disponibilidade dos dados. 
 
Serviços sempre disponíveis =
São resilientes a quedas em toda a região e a paralisações em toda a zona. 
 
Conjuntos de disponibilidade = 
São agrupamentos lógicos de VMs que permitem ao Azure entender como o aplicativo é criado para fornecer disponibilidade e redundância. 
 
O Azure recomenda criar duas ou mais VMs dentro de um conjunto de disponibilidade para atender ao SLA do Azure de 99,95%. 

Obs.: Para maiores informações sobre zonas de disponibilidades, segue documento oficial da MIcrosoft Azure, detalhando todo o contéudo, link abaixo
https://learn.microsoft.com/pt-br/azure/virtual-machines/availability

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

// Segue tutorial para uma melhor compreensão sobre redundância

LRS, ZRS, GRS e GZRS são tipos de redundância de armazenamento do Azure:
LRS (Locally Redundant Storage): Armazenamento com Redundância Local
ZRS (Zone-Redundant Storage): Armazenamento com Redundância de Zona
GRS (Geo-Redundant Storage): Armazenamento com Redundância Geográfica
GZRS (Geo-Zone-Redundant Storage): Armazenamento com Redundância de Zona Geográfica 
 
O GZRS é recomendado para proteger contra desastres regionais, pois replica os dados geograficamente para uma região secundária. O GRS armazena três cópias em uma Availability Zone e três cópias em outra Availability Zone, mas existe um pequeno atraso de atualização entre os dois pares. 
 
O LRS na região secundária protege os dados contra falhas de hardware. 

Obs.: Para atenuar esse risco, a Microsoft recomenda usar o armazenamento com redundância de zona (ZRS), o armazenamento com redundância geográfica (GRS) ou o armazenamento com redundância de zona geográfica (GZRS). Uma solicitação de gravação para uma conta de armazenamento que está usando o LRS ocorre de forma síncrona.

Obs.: Para maiores informações sobre redundância entre regiões, segue documento oficial da MIcrosoft Azure, detalhando todo o contéudo, link abaixo
https://learn.microsoft.com/pt-br/azure/storage/files/files-redundancy
 




