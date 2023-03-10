# Redes

## VPC
VPC (Virtual Private Cloud) é um serviço de rede da AWS que permite que você crie uma nuvem privada virtual na qual você pode lançar recursos da AWS, como instâncias EC2 (Elastic Compute Cloud) e bancos de dados RDS (Relational Database Service). É possível criar e configurar uma VPC para atender às necessidades específicas da sua aplicação ou organização.

Com a VPC, você pode criar um ambiente de rede isolado e seguro na nuvem AWS. É possível definir endereços IP privados, criar sub-redes, configurar tabelas de rotas e definir regras de segurança em um nível granular para controlar o tráfego de entrada e saída da VPC. Além disso, você pode conectar a VPC ao data center local ou a outras redes usando uma conexão de rede privada, como VPN (Virtual Private Network) ou AWS Direct Connect.

A VPC também oferece recursos avançados, como a capacidade de criar instâncias EC2 em várias sub-redes para melhorar a escalabilidade e a resiliência, bem como criar e gerenciar grupos de segurança para controlar o tráfego de entrada e saída	.

A AWS oferece opções flexíveis de configuração da VPC, como criar uma VPC a partir do zero ou usar um modelo pré-configurado. Além disso, é possível usar ferramentas como o Amazon VPC Wizard para configurar rapidamente a VPC com base em configurações comuns.

Em resumo, a VPC da AWS é um serviço de rede que fornece um ambiente de computação em nuvem isolado, seguro e altamente personalizável para permitir que você execute seus aplicativos e serviços na nuvem AWS de maneira eficiente e escalável.

### Route Tables
Route Tables na AWS é um serviço que permite controlar o tráfego de rede dentro de uma rede virtual (VPC) criada na AWS. A tabela de roteamento é um conjunto de regras que determina o tráfego de entrada e saída da VPC, especificando o destino de cada pacote de rede que entra ou sai da VPC.

A tabela de roteamento é uma lista de rotas que define como o tráfego de rede é encaminhado entre a VPC e a internet, ou entre a VPC e outras redes que possam estar conectadas a ela. Cada tabela de roteamento pode ter várias regras de roteamento, e cada regra pode especificar um destino de rede, como um endereço IP ou um intervalo de endereços IP, e o caminho que o tráfego deve seguir para alcançar esse destino, como uma interface de rede ou um gateway da Internet.

Por padrão, cada VPC é criada com uma tabela de roteamento padrão que é aplicada a todas as sub-redes da VPC. No entanto, você pode criar tabelas de roteamento personalizadas para atender às suas necessidades específicas. Por exemplo, você pode criar uma tabela de roteamento separada para lidar com o tráfego de rede de uma sub-rede específica, ou pode criar uma tabela de roteamento separada para lidar com o tráfego de rede de um grupo específico de instâncias.	

Ao configurar uma tabela de roteamento na AWS, você pode definir rotas para direcionar o tráfego de entrada e saída da VPC. Isso permite que você controle o tráfego de rede de maneira granular e eficiente, ajudando a garantir que o tráfego seja encaminhado corretamente e reduzindo a possibilidade de falhas de rede ou problemas de segurança.

### Internet Gateway
Internet Gateway (ou Gateway de Internet) na AWS é um serviço que permite que uma rede privada, criada por meio do Amazon Virtual Private Cloud (VPC), tenha acesso à Internet pública.

Ao criar uma VPC na AWS, ela é criada como uma rede privada isolada da Internet. Isso significa que as instâncias EC2 (Elastic Compute Cloud) e outros recursos dentro da VPC não têm acesso à Internet pública. Para permitir que esses recursos se comuniquem com a Internet, é necessário criar um Internet Gateway e anexá-lo à VPC.

O Internet Gateway é um componente virtual que funciona como um roteador entre a VPC e a Internet pública. Ele permite que as instâncias EC2 e outros recursos dentro da VPC se conectem à Internet e, ao mesmo tempo, protege a VPC de tráfego não autorizado.

Para utilizar o Internet Gateway, é necessário configurar as rotas na tabela de roteamento da VPC para direcionar o tráfego de saída para o Internet Gateway. Isso permitirá que o tráfego gerado pelos recursos da VPC sejam roteados para a Internet pública.

É importante destacar que o uso do Internet Gateway pode implicar em custos adicionais devido ao tráfego de dados que é gerado entre a VPC e a Internet pública. Além disso, é importante configurar a segurança da VPC adequadamente para garantir que apenas o tráfego autorizado tenha acesso à Internet pública.

### Peering Connection
O AWS Peering Connection é uma conexão de rede privada direta entre duas VPCs (Virtual Private Clouds) diferentes dentro do ambiente da Amazon Web Services (AWS). Esse recurso permite que as VPCs comuniquem-se entre si de forma segura, confiável e de alta velocidade, sem precisar passar pela internet pública.

Com o AWS Peering Connection, é possível conectar VPCs dentro da mesma conta AWS ou em diferentes contas. Essa conexão é estabelecida através de um túnel criptografado, garantindo a privacidade e segurança dos dados trocados entre as VPCs.

O AWS Peering Connection permite que as VPCs compartilhem recursos e serviços, como instâncias EC2, bancos de dados RDS, balanceadores de carga ELB, entre outros. Além disso, a conexão entre as VPCs pode ser facilmente gerenciada através do console de gerenciamento da AWS ou utilizando ferramentas de linha de comando, permitindo que os usuários configurem, monitorem e gerenciem as conexões de forma eficiente.

Em resumo, o AWS Peering Connection é uma solução ideal para empresas que precisam integrar e compartilhar recursos entre VPCs em sua infraestrutura da AWS, de forma privada e segura.

## Security Group
Security groups são um recurso da AWS que fornecem uma camada adicional de segurança para as instâncias do Amazon Elastic Compute Cloud (Amazon EC2), permitindo que você controle o acesso de entrada e saída para as instâncias. Eles funcionam como um firewall virtual para sua instância EC2, permitindo que você controle o tráfego de rede de entrada e saída que é permitido na sua instância.

Cada security group atua como uma política de segurança para uma ou mais instâncias EC2, especificando as portas de entrada permitidas, os protocolos de rede aceitos e os endereços IP de origem autorizados. Isso significa que você pode permitir ou negar o tráfego de entrada ou saída para sua instância com base em uma série de regras de segurança que você definiu.

Os security groups da AWS são criados com base em regras que você define, incluindo o tipo de tráfego permitido (por exemplo, HTTP, SSH, RDP), os intervalos de endereços IP permitidos (por exemplo, de um único endereço IP ou de um intervalo de endereços IP), e as portas permitidas para o tráfego (por exemplo, a porta 80 para o tráfego HTTP).

Cada instância EC2 pode ser associada a um ou mais security groups, e os security groups podem ser aplicados a várias instâncias. É importante notar que os security groups são específicos da região em que foram criados e só se aplicam às instâncias dentro dessa região.

Em resumo, os security groups são uma maneira eficiente de garantir a segurança das suas instâncias EC2, permitindo que você defina políticas de segurança baseadas em regras para controlar o tráfego de entrada e saída.

## NACL
O NACL é um recurso da AWS que permite controlar o tráfego de rede em uma VPC (Virtual Private Cloud) da AWS. Ele age como uma camada adicional de segurança, além das regras de segurança de grupos de segurança. O NACL permite configurar regras de entrada e saída de tráfego de rede para uma ou mais sub-redes dentro da VPC.

Cada NACL é composto por uma lista de regras numeradas em ordem de prioridade. Cada regra contém informações como o tipo de tráfego permitido (por exemplo, HTTP, SSH, RDP), o endereço IP de origem e destino, e a ação a ser tomada em caso de correspondência da regra (por exemplo, permitir ou negar o tráfego).

O NACL é útil para permitir ou bloquear o tráfego de rede em um nível mais granular, dependendo das necessidades de segurança da sua aplicação. No entanto, é importante lembrar que configurar o NACL incorretamente pode bloquear o tráfego legítimo da sua aplicação, portanto, é necessário ter cuidado ao configurá-lo.

## PoP
Em termos de AWS, PoP significa Point of Presence, que se refere a um local físico onde a AWS possui equipamentos de rede e infraestrutura para fornecer serviços de nuvem aos seus clientes.

A AWS possui PoPs em diversas localidades ao redor do mundo, incluindo América do Norte, Europa, Ásia, Austrália, América Latina, Oriente Médio e África. Esses PoPs são essenciais para permitir que os clientes da AWS acessem os serviços em suas regiões geográficas com baixa latência e alta disponibilidade.

Os PoPs da AWS geralmente incluem servidores, roteadores e outros equipamentos de rede que gerenciam o tráfego de dados e garantem que os serviços da AWS estejam disponíveis e funcionando adequadamente para os usuários finais. Além disso, os PoPs podem incluir recursos de cache, como o Amazon CloudFront, que armazena em cache conteúdo web e distribui esse conteúdo a partir do local mais próximo ao usuário final, reduzindo a latência e melhorando o desempenho.

Em resumo, os PoPs são pontos de presença física da AWS que fornecem recursos de infraestrutura de rede e computação, permitindo que os clientes da AWS acessem os serviços em suas regiões com baixa latência e alta disponibilidade.

## Elastic IP
O Elastic IP é um serviço da AWS (Amazon Web Services) que permite aos usuários ter um endereço IP estático e fixo para uma instância EC2 (Elastic Compute Cloud) ou uma interface de rede. Normalmente, quando você inicia uma instância EC2 na AWS, ela recebe um endereço IP público que pode mudar sempre que a instância é parada ou iniciada novamente. Com o Elastic IP, você pode atribuir um endereço IP estático e fixo para sua instância, que permanecerá o mesmo, mesmo que a instância seja interrompida ou iniciada novamente.

O uso do Elastic IP é especialmente importante quando se trata de hospedagem de sites ou aplicativos, pois permite que você mantenha um endereço IP fixo para sua instância, o que facilita a conexão de domínios personalizados, configuração de DNS e outros recursos de rede.

O Elastic IP é fácil de configurar na AWS. Você pode alocar um novo endereço IP ou usar um endereço IP existente e associá-lo a uma instância EC2 ou interface de rede. É importante lembrar que a AWS cobra uma pequena taxa horária pelo uso de um endereço IP elástico alocado, a menos que ele esteja associado a uma instância em execução. Portanto, é importante monitorar o uso do Elastic IP e desassociá-lo de instâncias em execução quando não estiver em uso para evitar cobranças desnecessárias.

## ELB
AWS ELB (Elastic Load Balancer) é um serviço da AWS que distribui o tráfego de rede entre instâncias EC2 (Elastic Compute Cloud) ou containers. O ELB ajuda a melhorar a disponibilidade e escalabilidade de aplicações, permitindo que elas sejam executadas em várias instâncias simultaneamente, sem sobrecarregar nenhuma delas. O serviço monitora o tráfego e redireciona as requisições para as instâncias disponíveis, tornando o processo transparente para o usuário final. O AWS ELB também oferece recursos de segurança, como a capacidade de criptografar o tráfego de rede e proteger as instâncias de ataques DDoS (Distributed Denial of Service). Em resumo, o AWS ELB é uma ferramenta essencial para garantir a disponibilidade, escalabilidade e segurança de aplicações na nuvem.

### Listener
AWS ELB Listener é um componente do Elastic Load Balancing (ELB) da AWS que atua como um ponto de entrada para o tráfego de rede que chega ao Load Balancer. O Listener é responsável por receber as solicitações de tráfego e direcioná-las para os recursos de back-end, como instâncias do Amazon EC2, contêineres ou outros serviços web.

O Listener opera em um ou mais protocolos de camada de transporte (como HTTP, HTTPS, TCP, SSL) e portas definidas pelo usuário. Ele também define o comportamento do Load Balancer em relação ao tráfego recebido, como o roteamento de solicitações para diferentes grupos de destino ou distribuição do tráfego por porcentagem, sessão ou endereço IP do cliente.

Em resumo, o AWS ELB Listener é um elemento fundamental para configurar e gerenciar o fluxo de tráfego em um ambiente de infraestrutura na nuvem da AWS, permitindo a distribuição de carga de trabalho e a alta disponibilidade dos aplicativos hospedados em diferentes instâncias ou serviços.

### Tipos
1. Classic Load Balancer: como mencionado anteriormente, é o tipo mais antigo de ELB e suporta balanceamento de carga para aplicações web HTTP/HTTPS e TCP/SSL.
2. Application Load Balancer: como mencionado anteriormente, é um ELB avançado que suporta balanceamento de carga de aplicações web HTTP/HTTPS. Ele roteia tráfego para instâncias EC2 com base em regras definidas em um nível de aplicação, como URL, cabeçalhos de solicitação e cookies.
3. Network Load Balancer: como mencionado anteriormente, é um ELB que suporta balanceamento de carga de camada de rede TCP/UDP. Ele é capaz de lidar com altas taxas de transferência e conexões de baixa latência.
4. Gateway Load Balancer: é um novo tipo de ELB que fornece escalabilidade, disponibilidade e segurança para cargas de trabalho que executam em um ambiente de gateway, como VPN, NAT e firewalls. O Gateway Load Balancer é compatível com AWS Transit Gateway, permitindo a integração fácil de gateways com recursos em diferentes regiões ou contas da AWS.

| Recurso          | Classic Load Balancer (CLB) | Application Load Balancer (ALB) | Network Load Balancer (NLB) | Gateway Load Balancer (GLB) |
|------------------|------------------------------|--------------------------------|------------------------------|------------------------------|
| Tipo de balanceamento de carga | Nível de conexão            | Camada de aplicação            | Camada de transporte          | Camada de rede                |
| Suporte de protocolos | HTTP, HTTPS, TCP, SSL        | HTTP, HTTPS, WebSocket, HTTP/2 | TCP, UDP                      | TCP, UDP, HTTP(S)            |
| Redirecionamento de URL | Não                          | Sim                            | Não                          | Sim                            |
| Roteamento de tráfego | Baseado em regras e recursos | Baseado em regras              | Baseado em regras e recursos | Baseado em regras e recursos |
| Balanceamento de carga de IP | Não                          | Sim                            | Sim                            | Sim                            |
| Suporte de porta | Portas fixas                 | Portas variáveis               | Portas fixas                 | Portas fixas e variáveis       |
| Escalabilidade | Escalabilidade vertical e horizontal (limitada) | Escalabilidade vertical e horizontal | Escalabilidade horizontal | Escalabilidade horizontal |
| Preços           | Cobrado por hora            | Cobrado por hora               | Cobrado por hora             | Cobrado por hora              |

| [Anterior: Aramazenamento](./2_Armazenamento.md) | [Proximo: Computação](./4_Computacao.md) |
|:--------------------------------|---------------------------:|