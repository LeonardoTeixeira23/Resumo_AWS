# Infraestrutura

## AZs e SLA
As Zonas de Disponibilidade (Availability Zones - AZs) da AWS são data centers fisicamente separados que são projetados para serem independentes uns dos outros. Cada AZ tem sua própria infraestrutura de rede, energia e resfriamento, e é isolada de outras AZs para garantir a alta disponibilidade e resiliência de aplicativos e serviços implantados na nuvem da AWS.

O Service Level Agreement (SLA) da AWS para as Zonas de Disponibilidade é de 99,99% de disponibilidade em cada região da AWS. Isso significa que a AWS se compromete a manter cada AZ de uma região disponível e operacional 99,99% do tempo em um ciclo de cobrança mensal. Se a disponibilidade de uma AZ for inferior a 99,99%, a AWS pode oferecer créditos de serviço aos clientes afetados.

O SLA da AWS para as AZs é projetado para garantir a continuidade dos negócios e minimizar o impacto de interrupções no serviço. Os clientes podem usar várias estratégias de implantação, como o balanceamento de carga entre as AZs, para aumentar ainda mais a disponibilidade e resiliência de seus aplicativos e serviços na nuvem da AWS.

Em resumo, as Zonas de Disponibilidade da AWS são projetadas para garantir alta disponibilidade e resiliência de aplicativos e serviços na nuvem da AWS, e a AWS oferece um SLA de 99,99% de disponibilidade para cada AZ em uma região da AWS.

## Private Cloud
Private Cloud na AWS refere-se a um ambiente de computação em nuvem configurado para atender exclusivamente as necessidades de uma única organização ou empresa. Diferentemente do modelo de nuvem pública, onde vários usuários compartilham recursos, a nuvem privada é dedicada a uma organização específica e geralmente é implantada em uma infraestrutura de data center privado.

Na AWS, é possível criar uma nuvem privada utilizando as ferramentas de virtualização como o VMware ou o Hyper-V, por exemplo. Com essas ferramentas, é possível criar máquinas virtuais (VMs) e implantá-las em uma nuvem privada. Além disso, é possível configurar recursos de rede e armazenamento para a nuvem privada.

A AWS oferece diversas soluções de nuvem privada, incluindo o Amazon VPC (Virtual Private Cloud), que permite criar uma nuvem privada na AWS isolada da Internet pública, e o AWS Outposts, que permite a criação de uma nuvem privada dentro do data center da própria organização, fornecendo recursos de computação e armazenamento em nuvem de alta qualidade.

A utilização de uma nuvem privada pode trazer benefícios como maior controle sobre a infraestrutura, personalização e segurança. No entanto, é importante lembrar que o custo de implantação e manutenção de uma nuvem privada pode ser elevado

## Backbone
AWS Backbone é a infraestrutura de rede global da Amazon Web Services (AWS) que interliga todos os seus serviços e regiões. Essa rede é composta por uma série de pontos de presença (PoPs) distribuídos em todo o mundo, conectados por uma rede de fibra óptica privada e de alta velocidade.

A AWS Backbone fornece um alto nível de disponibilidade, escalabilidade e desempenho para todos os serviços da AWS. Com essa infraestrutura, a AWS é capaz de oferecer serviços com baixa latência e alta velocidade de transferência de dados em todo o mundo.

Além disso, a AWS Backbone é responsável por fornecer segurança para os serviços da AWS. A rede é projetada para oferecer proteção contra ataques DDoS e outras ameaças à segurança.

A infraestrutura de rede da AWS também oferece suporte a recursos como o Amazon CloudFront, que é uma rede de entrega de conteúdo (CDN) global, permitindo que os clientes entreguem conteúdo rapidamente para seus usuários finais, independentemente de onde eles estejam localizados.

Em resumo, a AWS Backbone é uma infraestrutura de rede global de alta velocidade e segurança que interliga todos os serviços e regiões da AWS. Ela oferece suporte a uma ampla variedade de recursos e serviços, permitindo que as empresas possam executar suas operações de TI em uma escala global.

## Edge Locations
AWS Edge Locations são pontos de presença (POPs) distribuídos globalmente, localizados em cidades estratégicas ao redor do mundo, que fazem parte da infraestrutura da AWS. Essas localidades servem como uma camada intermediária entre os usuários finais e os serviços da AWS, permitindo a entrega de conteúdo de forma mais rápida e eficiente.

Quando um usuário solicita um conteúdo (como um vídeo ou uma imagem) a partir de um servidor da AWS, o conteúdo pode ser armazenado em cache em um Edge Location próximo ao usuário, o que acelera o tempo de resposta e melhora a experiência do usuário final.

Além disso, os Edge Locations também são usados para serviços como Amazon CloudFront, Amazon Route 53 e AWS Global Accelerator, permitindo a entrega de conteúdo de forma global, escalável e segura. Em resumo, os Edge Locations da AWS são essenciais para melhorar a performance e a disponibilidade dos serviços em nuvem da AWS em todo o mundo.

## PoP
Em termos de AWS, PoP significa Point of Presence, que se refere a um local físico onde a AWS possui equipamentos de rede e infraestrutura para fornecer serviços de nuvem aos seus clientes.

A AWS possui PoPs em diversas localidades ao redor do mundo, incluindo América do Norte, Europa, Ásia, Austrália, América Latina, Oriente Médio e África. Esses PoPs são essenciais para permitir que os clientes da AWS acessem os serviços em suas regiões geográficas com baixa latência e alta disponibilidade.

Os PoPs da AWS geralmente incluem servidores, roteadores e outros equipamentos de rede que gerenciam o tráfego de dados e garantem que os serviços da AWS estejam disponíveis e funcionando adequadamente para os usuários finais. Além disso, os PoPs podem incluir recursos de cache, como o Amazon CloudFront, que armazena em cache conteúdo web e distribui esse conteúdo a partir do local mais próximo ao usuário final, reduzindo a latência e melhorando o desempenho.

Em resumo, os PoPs são pontos de presença física da AWS que fornecem recursos de infraestrutura de rede e computação, permitindo que os clientes da AWS acessem os serviços em suas regiões com baixa latência e alta disponibilidade.

## IaaS
AWS IaaS (Infrastructure as a Service) é um modelo de serviço em nuvem da AWS que oferece recursos de infraestrutura, como servidores virtuais, armazenamento, redes, entre outros, como um serviço sob demanda. Com a AWS IaaS, os usuários podem configurar e gerenciar seus próprios recursos de infraestrutura de forma rápida e escalável, sem precisar investir em hardware ou manutenção. A AWS IaaS oferece uma ampla gama de serviços, incluindo EC2 (Elastic Compute Cloud), EBS (Elastic Block Store), VPC (Virtual Private Cloud), Route 53 (serviço de DNS gerenciado), entre outros. Com o modelo IaaS, os usuários têm controle total sobre o ambiente de infraestrutura, desde a escolha do sistema operacional até as configurações de rede e segurança. Isso permite que as empresas adaptem seus ambientes de infraestrutura de acordo com suas necessidades específicas, aumentando a flexibilidade e reduzindo os custos operacionais.

## PaaS
AWS PaaS (Platform as a Service) é um modelo de serviço de nuvem em que a plataforma de desenvolvimento e implantação é fornecida como um serviço gerenciado na nuvem. Isso significa que os desenvolvedores podem criar, implantar e executar aplicativos em uma infraestrutura gerenciada pelo provedor de serviços em nuvem, sem ter que gerenciar o hardware ou o software subjacente.

A AWS oferece diversos serviços de PaaS, como o AWS Elastic Beanstalk, que permite implantar e gerenciar aplicativos na nuvem de maneira fácil e rápida, sem se preocupar com a infraestrutura subjacente. Outros exemplos incluem o AWS Lambda, que permite executar códigos sem servidor, o AWS App Runner, que automatiza o processo de criação, implantação e execução de aplicativos em contêineres, e o AWS Amplify, que oferece uma plataforma de desenvolvimento completa para criar aplicativos móveis e da web.

Em resumo, o AWS PaaS é uma abordagem que oferece às empresas uma maneira mais rápida e eficiente de desenvolver, implantar e gerenciar aplicativos em nuvem, sem ter que se preocupar com a infraestrutura subjacente. Isso permite que as empresas se concentrem mais em inovar e desenvolver novos recursos para seus aplicativos, em vez de se preocupar com a manutenção da infraestrutura.

## SaaS
AWS SaaS (Software as a Service) é um modelo de negócio em que uma empresa oferece seus aplicativos e serviços hospedados na nuvem como um serviço para seus clientes. Com o AWS SaaS, os desenvolvedores e empresas podem criar, implantar e gerenciar seus aplicativos de forma rápida e escalável na infraestrutura da AWS, sem precisar se preocupar com a complexidade da gestão de infraestrutura e da escalabilidade de recursos.

Os clientes podem acessar esses aplicativos e serviços por meio de um navegador web ou de aplicativos específicos, geralmente pagando por uma assinatura mensal ou anual. Alguns exemplos de SaaS populares na AWS são o Salesforce, Microsoft Office 365, Dropbox e Slack.

Em resumo, o AWS SaaS é um modelo de negócio que permite às empresas oferecer seus aplicativos e serviços na nuvem de forma escalável, eficiente e rentável, tornando mais fácil para os clientes utilizá-los sem se preocupar com a infraestrutura por trás.


|               [Proximo: Armazenamento](./2_Armazenamento.md) |
|-------------------------------------------------------------:|