# Computação

## EC2
EC2 (Elastic Compute Cloud) é um serviço de computação em nuvem fornecido pela AWS que permite que os usuários executem instâncias de servidores virtualizados na nuvem. Com o EC2, os usuários podem criar, configurar e gerenciar facilmente instâncias de servidores sob demanda, com escalabilidade rápida e flexível.

O EC2 é altamente escalável e pode ser usado para hospedar aplicativos e serviços de todos os tamanhos, desde pequenos sites e aplicativos até grandes empresas com tráfego e demanda intensos. Com o EC2, os usuários podem selecionar a capacidade de processamento, memória, armazenamento e rede que melhor atende às suas necessidades.

O EC2 oferece várias opções de sistema operacional, incluindo Amazon Linux, Ubuntu, Windows Server, entre outros, e os usuários podem configurar suas instâncias para atender às suas necessidades específicas. Além disso, o EC2 é altamente seguro e oferece recursos avançados de segurança, como criptografia de dados em trânsito e em repouso, controle de acesso e segurança de rede.

O EC2 é usado por empresas de todos os tamanhos e em todos os setores para hospedar aplicativos, sites, serviços e aplicativos móveis na nuvem. Ele oferece uma alternativa econômica e escalável ao provisionamento de servidores em data centers locais e ajuda as empresas a reduzir custos e aumentar a agilidade e a eficiência dos negócios.

### Diferença entre EC2 e S3
EC2 e S3 são serviços diferentes da Amazon Web Services (AWS) que atendem a diferentes necessidades de computação e armazenamento na nuvem.

EC2 (Elastic Compute Cloud) é um serviço de computação em nuvem que fornece capacidade computacional sob demanda. Com o EC2, os usuários podem criar e gerenciar instâncias de máquinas virtuais (VMs) em uma infraestrutura de nuvem altamente escalável e segura.

S3 (Simple Storage Service) é um serviço de armazenamento em nuvem que permite armazenar e recuperar grandes quantidades de dados de forma segura e escalável. O S3 é frequentemente usado para armazenar arquivos estáticos, como imagens, vídeos, arquivos de áudio e backups de banco de dados, entre outros.

Em resumo, enquanto o EC2 fornece recursos de computação sob demanda, o S3 é voltado para armazenamento em nuvem de grande escala. No entanto, é possível usar esses serviços juntos para criar aplicativos escaláveis que combinam recursos de computação e armazenamento em nuvem.

### Tipo de Instância
AWS oferece diversos tipos de instâncias EC2 (Elastic Compute Cloud), cada um com diferentes combinações de CPU, memória, armazenamento e capacidade de rede, projetados para atender a diferentes cargas de trabalho. Aqui estão alguns dos tipos de instâncias EC2 disponíveis:
1. General Purpose Instances: projetadas para aplicativos que exigem uma proporção balanceada de CPU, memória e armazenamento. Exemplos: t2.micro, m5.large.
2. Computer-Optimized Instances: projetadas para cargas de trabalho que exigem alto desempenho de CPU, como aplicativos de computação científica e análise de dados. Exemplos: c5.large, c5n.18xlarge.
3. Memory-Optimized Instances: projetadas para cargas de trabalho que exigem grande quantidade de memória, como bancos de dados e análise de big data. Exemplos: r5.large, x1e.32xlarge.
4. Storage-Optimized Instances: projetadas para cargas de trabalho que exigem alto desempenho de armazenamento, como bancos de dados NoSQL e Hadoop Distributed File System (HDFS). Exemplos: d2.xlarge, i3.large.
5. GPU Instances: projetadas para cargas de trabalho que exigem desempenho de GPU, como aprendizado de máquina e processamento de vídeo. Exemplos: p3.2xlarge, g4dn.xlarge.
6. FPGA Instances: projetadas para cargas de trabalho que exigem aceleração personalizada para cargas de trabalho específicas, como processamento de imagens e análise de dados. Exemplo: f1.2xlarge.

| Recurso | Amazon EC2 | Amazon S3 |
| --- | --- | --- |
| Tipo de serviço | Serviço de computação (IaaS) | Serviço de armazenamento (S3) |
| Capacidade de armazenamento | Armazenamento efêmero em instâncias EC2 | Armazenamento ilimitado de objetos |
| Acesso | Acesso via SSH ou RDP para gerenciamento de instâncias | Acesso através de APIs ou consoles web |
| Uso de dados | Armazenamento de dados em unidades de instância de EBS ou instância temporária de armazenamento local | Armazenamento de objetos como arquivos, imagens, vídeos, etc. |
| Escalabilidade | Escalabilidade vertical (adicionar recursos à instância) e horizontal (adicionar instâncias) | Escalabilidade horizontal (adicionar mais objetos) |
| Custo | Faturamento por hora da instância EC2 e armazenamento EBS | Faturamento por GB de armazenamento e transferência de dados |

### Tipos de Volume
Existem vários tipos de volumes que podem ser usados com o Amazon EC2, incluindo:
1. Amazon Elastic Block Store (EBS): É um serviço de armazenamento de blocos de dados que pode ser anexado a uma instância do EC2 para fornecer armazenamento persistente. Os volumes do Amazon EBS são altamente disponíveis, escaláveis e fornecem opções de desempenho para atender às necessidades de diferentes cargas de trabalho.
2. Armazenamento de instâncias: As instâncias do Amazon EC2 também podem ser configuradas para usar o armazenamento local de instâncias, que é armazenamento em disco efêmero anexado fisicamente à instância. O armazenamento de instâncias é ideal para aplicativos que exigem alta taxa de transferência de dados e acesso de baixa latência.
3. Armazenamento S3: Embora o Amazon S3 seja um serviço de armazenamento de objetos, os usuários podem acessar os arquivos armazenados no S3 diretamente de suas instâncias do EC2, como se estivessem armazenados localmente. O armazenamento S3 é ideal para armazenar arquivos que não mudam com frequência e que são acessados com pouca frequência.
4. Armazenamento Glacier: O Amazon Glacier é um serviço de armazenamento em nuvem de baixo custo e altamente durável. Os usuários podem usar o Glacier como um destino de backup para seus dados do EC2 ou para arquivar dados que não são acessados com frequência.

### AMI
AMI (Amazon Machine Image) é uma imagem de máquina pré-configurada, que pode ser usada para criar instâncias do Amazon Elastic Compute Cloud (EC2). É basicamente uma imagem de backup de uma instância EC2, que pode ser usada para lançar novas instâncias EC2 idênticas à instância original.

Uma AMI inclui informações sobre o sistema operacional, as configurações de rede, os aplicativos instalados e outros dados necessários para lançar uma nova instância. Isso permite que os usuários criem e implementem facilmente novas instâncias EC2 que sejam semelhantes às instâncias existentes.

As AMIs podem ser criadas a partir de instâncias EC2 existentes ou criadas do zero, permitindo aos usuários personalizar as imagens para atender às suas necessidades específicas. As AMIs também podem ser compartilhadas entre contas da AWS e, em alguns casos, estão disponíveis publicamente para que qualquer pessoa possa usá-las.

Em resumo, AMIs são imagens de máquinas virtuais que fornecem uma maneira fácil de lançar e replicar instâncias EC2 com configurações específicas. Isso ajuda a simplificar o processo de implantação e escalabilidade de aplicativos na nuvem.

### Spot 
O Amazon EC2 Spot é um serviço da AWS que permite aos usuários aproveitar instâncias EC2 (Elastic Compute Cloud) não utilizadas a preços significativamente reduzidos. O Spot permite que os usuários aproveitem a capacidade ociosa de instâncias EC2 em execução na nuvem da AWS, permitindo que sejam usados a preços mais baixos do que as instâncias On-Demand.

As instâncias Spot são uma forma econômica de executar cargas de trabalho que são tolerantes a falhas e que podem ser interrompidas ou iniciadas em momentos diferentes. Os usuários podem solicitar instâncias Spot para suas cargas de trabalho a um preço que especificam, e a AWS aloca a capacidade de acordo com a oferta de capacidade ociosa disponível.

Os preços Spot flutuam continuamente com base na oferta e demanda de capacidade de instâncias. Quando o preço de uma instância Spot cai abaixo do preço que o usuário especificou, a instância é iniciada e executada até que a capacidade seja necessária por outro cliente com um preço maior. Quando isso acontece, a instância Spot é interrompida, permitindo que a capacidade seja usada por outro cliente.

O Spot pode ser usado para uma variedade de cargas de trabalho, incluindo tarefas de processamento em lote, cargas de trabalho de teste e desenvolvimento, análise de big data, entre outras. Ele pode ser integrado a outros serviços da AWS, como o Amazon EMR (Elastic MapReduce) e o AWS Batch, para criar ambientes de processamento em escala em um custo mais baixo.

O Spot é altamente escalável, tolerante a falhas. Com este serviço, os usuários podem economizar significativamente nos custos de infraestrutura de suas cargas de trabalho, aproveitando a capacidade ociosa da nuvem da AWS.

### EC2 Auto Scaling
O Amazon EC2 Auto Scaling é um AWS que permite que os usuários dimensionem automaticamente grupos de instâncias EC2 (Elastic Compute Cloud) para atender a demanda da aplicação. O serviço ajuda a garantir que o número de instâncias em execução seja proporcional à carga de trabalho, evitando a sobrecarga dos servidores ou a ociosidade de recursos.

Com o EC2 Auto Scaling, os usuários podem criar grupos de instâncias EC2 que são dimensionados automaticamente com base em métricas de utilização, como a CPU, memória, tráfego de rede e outras. O serviço permite que os usuários definam políticas de dimensionamento para aumentar ou diminuir o número de instâncias em execução com base em limites mínimos e máximos de capacidade.

O EC2 Auto Scaling também pode ser integrado a outros serviços da AWS, como o Elastic Load Balancing, para garantir que as instâncias sejam adicionadas ou removidas automaticamente com base na carga de trabalho do balanceador de carga. Além disso, o serviço oferece recursos de monitoramento e notificação para alertar os usuários sobre eventos de escalabilidade ou problemas de desempenho.

O EC2 Auto Scaling é altamente escalável, tolerante a falhas e pode ser facilmente configurado por meio do console da AWS, API ou linha de comando. Com este serviço, os usuários podem garantir que sua aplicação seja executada com a capacidade ideal, otimizando o desempenho e reduzindo os custos operacionais.

## Lambda Shared
O AWS Lambda Shared é um recurso da AWS Lambda que permite compartilhar recursos comuns entre diferentes funções do Lambda. Com o AWS Lambda Shared, você pode criar um código compartilhado ou biblioteca de funções que pode ser usado em várias funções sem a necessidade de copiá-las ou mantê-las separadamente. Isso pode ajudar a reduzir o tempo de desenvolvimento e a complexidade do código, além de melhorar a reutilização de código e a colaboração em equipe.

Para usar o AWS Lambda Shared, você pode criar uma camada (layer) que contém o código compartilhado ou uma biblioteca de funções e, em seguida, adicionar essa camada a uma ou mais funções do Lambda. Dessa forma, as funções podem acessar o código compartilhado ou a biblioteca de funções e usar suas funcionalidades em tempo de execução. Além disso, as camadas podem ser versionadas e gerenciadas separadamente, o que torna mais fácil manter e atualizar o código compartilhado em um ambiente distribuído.

Em resumo, o AWS Lambda Shared é uma solução para simplificar o desenvolvimento de funções do Lambda e melhorar a reutilização de código em diferentes projetos. Com ele, é possível compartilhar recursos comuns de forma simples, segura e escalável.

## Severless
AWS Serverless é um modelo de computação em nuvem que permite que os desenvolvedores criem e executem aplicativos sem se preocupar com a infraestrutura de hardware subjacente. Em um ambiente Serverless, a AWS gerencia automaticamente a alocação e a escalabilidade dos recursos de computação, armazenamento e rede, tornando o processo de desenvolvimento e implantação de aplicativos mais rápido e fácil.

O modelo de arquitetura Serverless da AWS é baseado em serviços que permitem que os desenvolvedores se concentrem apenas no código da aplicação, sem precisar lidar com a infraestrutura do servidor. Esses serviços incluem AWS Lambda, que permite executar código sem um servidor; Amazon API Gateway, que gerencia o acesso aos serviços e recursos do AWS; e AWS DynamoDB, que é um banco de dados NoSQL escalável e totalmente gerenciado.

Ao usar o modelo Serverless, os desenvolvedores podem implantar aplicativos rapidamente, escalar automaticamente conforme a demanda e pagar apenas pelos recursos que usam, reduzindo significativamente os custos de infraestrutura. Além disso, a AWS Serverless oferece alta disponibilidade e segurança, com recursos integrados de monitoramento e registro de dados para facilitar a depuração e a análise.

| [Anterior: Redes](./3_Rede.md) | [Proximo: Bando de Dados](./5_Bando_de_Dados.md) |
|:-------------------------------|-------------------------------------------------:|