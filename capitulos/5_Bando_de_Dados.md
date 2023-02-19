# Banco de Dados

## Amazon RDS
Amazon RDS (Relational Database Service) é um serviço gerenciador de banco de dados relacionais na nuvem da AWS. Ele permite que você crie, execute e dimensione facilmente bancos de dados relacionais na nuvem.

Os benefícios do Amazon RDS incluem:
- Gerenciamento automatizado: O Amazon RDS gerencia automaticamente tarefas de rotina, como aplicação de patches de segurança, backups e monitoramento de desempenho. Isso permite que você se concentre em desenvolver seus aplicativos, em vez de gerenciar a infraestrutura do banco de dados.
- Backup e recuperação: O Amazon RDS oferece backups automáticos e armazenamento em vários locais para proteger seus dados contra perda. Ele também permite que você restaure facilmente um banco de dados a partir de um ponto no tempo.
- Suporte para vários mecanismos de banco de dados: O Amazon RDS suporta vários mecanismos de banco de dados, incluindo MySQL, PostgreSQL, Oracle, SQL Server e MariaDB. Isso oferece flexibilidade para escolher o mecanismo de banco de dados que melhor atende às suas necessidades.
- Escalabilidade: O Amazon RDS permite que você dimensione facilmente seu banco de dados verticalmente ou horizontalmente para lidar com aumento de tráfego e demanda.
- Fácil de usar: O Amazon RDS é fácil de configurar e usar, e oferece uma variedade de opções de configuração para atender às necessidades específicas de seu aplicativo.

### Read Only
AWS RDS (Relational Database Service) é um serviço gerenciado de banco de dados na nuvem da Amazon Web Services (AWS). O modo read-only, ou modo somente leitura, significa que os usuários podem acessar o banco de dados para leitura de informações, mas não podem fazer alterações ou inserções.

O AWS RDS oferece suporte para múltiplas réplicas de leitura, permitindo que vários usuários acessem o banco de dados simultaneamente para leitura de informações, sem afetar a capacidade de gravação no banco de dados principal. Esse modo é útil para casos em que a maioria dos usuários precisam apenas acessar as informações armazenadas no banco de dados, sem precisar alterar ou inserir novos dados.

O modo read-only pode ser ativado ou desativado facilmente no console do AWS RDS. Quando ativo o RDS principal replica de forma assíncrona as alterações para as instâncias read-only

### Automet Backups
O AWS RDS (Relational Database Service) oferece um recurso de backups automáticos para garantir a segurança e a disponibilidade dos dados armazenados em seus bancos de dados na nuvem.

Os backups automáticos são realizados regularmente pelo RDS de forma a assegurar que os dados estejam disponíveis em caso de falhas no sistema, erros humanos ou incidentes de segurança. O recurso é totalmente gerenciado pela AWS e não requer a intervenção do usuário.

Os backups automáticos são realizados de acordo com uma política definida pelo usuário e podem ser agendados para ocorrer diariamente, semanalmente ou mensalmente. Durante o processo de backup, o RDS cria uma imagem do banco de dados, que pode ser usada posteriormente para restaurar o banco de dados em caso de necessidade.

Os backups automáticos são armazenados no Amazon S3 e podem ser retidos por até 35 dias. Isso significa que é possível restaurar o banco de dados em qualquer ponto nos últimos 35 dias.

O recurso de backups automáticos é altamente recomendado para todas as instâncias do RDS, pois garante a disponibilidade dos dados e ajuda a proteger o usuário contra perda de dados e interrupções no serviço.

### IOPS Storage
O AWS IOPS (Input/Output Operations per Second) é um serviço oferecido pela Amazon Web Services (AWS) que permite aos usuários otimizarem o desempenho de suas instâncias de banco de dados que rodam no Amazon RDS (Relational Database Service) ou no Amazon EC2 (Elastic Compute Cloud).

O IOPS Storage é um recurso do Amazon RDS que permite escolher o tipo de armazenamento para seus bancos de dados, com a opção de provisionar o número necessário de operações de entrada e saída por segundo (IOPS) para o seu banco de dados. O IOPS é uma medida de desempenho para armazenamento de dados, e quanto mais IOPS, mais rápido será o desempenho do armazenamento.

Com o IOPS Storage, os usuários podem escolher entre armazenamento padrão ou provisionado. O armazenamento padrão é adequado para cargas de trabalho de banco de dados leves e de baixa intensidade. Já o armazenamento provisionado é adequado para cargas de trabalho de banco de dados que exigem alto desempenho, como bancos de dados com muitas transações de leitura e gravação.

O IOPS Storage permite aos usuários configurar o número de IOPS que seus bancos de dados precisam para obter o melhor desempenho possível. Com isso, é possível provisionar o armazenamento de acordo com as necessidades da aplicação, garantindo um desempenho consistente e previsível, independentemente das flutuações no tráfego de aplicativos.

### General Purpose Storage
O tipo de armazenamento General Purpose (ou propósito geral) pode ser utilizado em ambos os serviços. No Amazon S3, o armazenamento General Purpose é conhecido como Amazon S3 Standard e fornece uma camada de armazenamento altamente disponível, durável e com baixa latência. No Amazon EBS, o armazenamento General Purpose é conhecido como gp2 e fornece armazenamento de bloco de alta performance para as instâncias EC2.

### Magnetic Storage
O Amazon RDS Magnetic Storage é um tipo de armazenamento disponível no serviço de banco de dados relacional da Amazon Web Services (AWS), o RDS. Esse tipo de armazenamento é a opção mais econômica do RDS e é recomendado para aplicações que não exigem alta performance de I/O, ou seja, que não precisam de um alto volume de leitura e gravação de dados no disco.

O Amazon RDS Magnetic Storage utiliza discos magnéticos (hdd) como meio de armazenamento, em vez de unidades de estado sólido (ssd), que são mais rápidas, mas também mais caras. Isso torna o RDS Magnetic Storage uma opção de armazenamento mais acessível para as aplicações que têm menor demanda por performance e/ou possuem restrições orçamentárias.

No entanto, vale lembrar que o uso do RDS Magnetic Storage pode ter um impacto na performance das aplicações que utilizam o banco de dados, especialmente em operações que envolvem leitura e gravação de grandes volumes de dados. Por isso, é importante avaliar as necessidades de performance do seu aplicativo e considerar outras opções de armazenamento oferecidas pelo RDS, como o Provisioned IOPS SSD, caso seja necessário uma maior performance de I/O.

Em resumo, o Amazon RDS Magnetic Storage é uma opção de armazenamento econômica para aplicações com menor demanda por performance e/ou com restrições orçamentárias, mas que ainda precisam de uma infraestrutura de banco de dados confiável e escalável.

### Multi-Master Clusters
Um cluster de banco de dados com múltiplos mestres na Amazon Web Services (AWS) é uma arquitetura que permite a configuração de vários nós de banco de dados mestre para operarem em paralelo e aceitar escritas simultâneas. Isso pode melhorar significativamente o desempenho e a disponibilidade do banco de dados em relação a um cluster de banco de dados convencional com um único nó mestre.

Os clusters de banco de dados com múltiplos mestres estão disponíveis no AWS RDS (Relational Database Service) para MySQL e PostgreSQL. Com a configuração de um cluster de banco de dados com múltiplos mestres, cada nó mestre tem sua própria cópia do banco de dados.

Quando uma gravação é feita em um nó mestre, a transação é replicada automaticamente em todos os outros nós mestre no cluster. Isso significa que várias escritas podem ocorrer simultaneamente, resultando em um melhor desempenho e capacidade de resposta do banco de dados.

Além disso, os clusters de banco de dados com múltiplos mestres podem ajudar a melhorar a disponibilidade do banco de dados. Se um nó mestre falhar, outro nó mestre pode assumir automaticamente e as transações podem continuar sem interrupção. Isso significa que o cluster de banco de dados pode continuar operando mesmo em caso de falha em um ou mais nós.

No entanto, é importante notar que a configuração de um cluster de banco de dados com múltiplos mestres pode ser mais complexa do que a configuração de um cluster de banco de dados convencional com um único nó mestre. A configuração requer conhecimento técnico avançado e experiência em bancos de dados, além de ajustes de configuração para garantir que as transações sejam replicadas de forma confiável em todo o cluster.

### TDE
AWS TDE (Transparent Data Encryption) é um recurso de segurança oferecido pela Amazon Web Services (AWS) que criptografa automaticamente dados em repouso armazenados em bancos de dados RDS (Relational Database Service).

O TDE usa criptografia AES-256 para proteger dados em repouso, incluindo backups, snapshots e réplicas de bancos de dados RDS. Isso ajuda a proteger os dados sensíveis armazenados em bancos de dados, garantindo que apenas usuários autorizados possam acessá-los.

O TDE é transparente para aplicativos e usuários finais, o que significa que não há necessidade de alterar o aplicativo ou a forma de acesso ao banco de dados. O TDE criptografa os dados automaticamente antes de armazená-los e descriptografa-os automaticamente quando são lidos.

Para ativar o TDE, basta selecionar a opção "Enable Encryption" ao criar um novo banco de dados RDS ou habilitá-lo em um banco de dados existente. Uma vez ativado, a chave de criptografia é gerenciada pela AWS e armazenada em um ambiente seguro e altamente disponível.

O uso do AWS TDE é uma das formas de garantir a segurança dos dados armazenados em bancos de dados RDS, juntamente com outras práticas recomendadas de segurança, como controle de acesso baseado em função (RBAC), monitoramento de logs e atualizações regulares do software.

### Standby Replica
A Standby Replica é uma instância de banco de dados que está configurada para replicar todos os dados e alterações feitas no banco de dados principal. É uma réplica de leitura que está pronta para assumir o papel de banco de dados principal em caso de falha do banco de dados principal ou em caso de manutenção planejada.

A Standby Replica é criada com o objetivo de garantir a disponibilidade contínua do banco de dados principal e minimizar a interrupção dos serviços em caso de falhas ou interrupções. Quando uma falha é detectada na instância principal, a Standby Replica pode ser promovida para o papel de principal, permitindo que os usuários continuem a acessar e atualizar o banco de dados sem interrupções significativas.

A Standby Replica pode ser configurada como uma instância adicional em uma zona de disponibilidade diferente da instância principal, proporcionando maior resiliência em caso de falhas de zona. Além disso, a Standby Replica pode ser utilizada para fins de backup, permitindo que os dados sejam restaurados a partir de uma versão anterior, se necessário.

É importante destacar que a Standby Replica é uma instância de réplica de leitura, ou seja, ela não pode ser usada para fazer atualizações ou inserções no banco de dados. Ela serve apenas como uma cópia de segurança e como uma opção de failover em caso de problemas com a instância principal.

## AWS DynamoDB
SQL (Structured Query Language) e NoSQL (Not Only SQL) são dois tipos diferentes de bancos de dados. Embora ambos sejam usados ​​para armazenar e recuperar dados, existem algumas diferenças fundamentais entre eles:

- Modelo de dados: O SQL é baseado em um modelo de dados relacional, onde os dados são organizados em tabelas com linhas e colunas. Já o NoSQL é baseado em um modelo de dados não relacional, onde os dados são armazenados em documentos, pares de chave-valor, grafos ou outras estruturas.
- Estrutura: O SQL é altamente estruturado, o que significa que a estrutura dos dados é definida antecipadamente e segue um esquema rígido. O NoSQL é mais flexível, permitindo que os dados sejam adicionados, modificados ou removidos sem precisar alterar o esquema.
- Escalabilidade: O SQL é geralmente dimensionado verticalmente, o que significa que o hardware é atualizado para lidar com mais dados ou tráfego. O NoSQL é dimensionado horizontalmente, o que significa que os dados são distribuídos em vários servidores para lidar com mais tráfego ou armazenar mais dados.
- Desempenho: O SQL é adequado para operações de leitura complexas, como junções e agregações. O NoSQL é mais adequado para operações de gravação em larga escala e leituras simples.
- Segurança: O SQL tem recursos de segurança integrados, como controle de acesso baseado em funções e autenticação. O NoSQL pode ter recursos de segurança limitados, embora muitos provedores de banco de dados NoSQL ofereçam opções de segurança avançadas.
- Custo: O SQL geralmente tem custos iniciais mais altos devido à necessidade de comprar hardware e software de banco de dados, além de exigir especialistas em banco de dados para gerenciar o ambiente. O NoSQL é geralmente mais barato, pois é baseado em serviços em nuvem gerenciados.

Em resumo, SQL e NoSQL são tipos diferentes de bancos de dados, cada um com suas próprias vantagens e desvantagens. A escolha entre SQL e NoSQL dependerá dos requisitos do projeto, como o modelo de dados, a escalabilidade, o desempenho e o orçamento.

### NoSQL
Bancos de dados NoSQL (Not Only SQL) são sistemas de gerenciamento de banco de dados que diferem dos bancos de dados relacionais tradicionais, que utilizam linguagem SQL (Structured Query Language) para realizar consultas e manipulação de dados.

Os bancos de dados NoSQL são projetados para lidar com grandes volumes de dados, com alta escalabilidade e desempenho, além de oferecerem flexibilidade na modelagem de dados e esquemas. Eles geralmente usam uma abordagem de armazenamento de dados não tabular, baseada em documentos, grafos ou colunas, para permitir a fácil expansão e manipulação de dados não estruturados ou semiestruturados.

| Característica | Banco de dados SQL | Banco de dados NoSQL |
| --- | --- | --- |
| Estrutura de dados | Possui estrutura de dados rigidamente definida | Possui estrutura de dados flexível |
| Escalabilidade | Escalabilidade vertical limitada | Escalabilidade horizontal fácil e sem limites |
| Consultas | Suporta consultas SQL complexas | Não suporta consultas SQL complexas |
| Armazenamento | Normalmente usa tabelas com linhas e colunas | Normalmente usa documentos, pares de chave-valor ou famílias de colunas |
| Transações | Suporta transações ACID (Atomicidade, Consistência, Isolamento, Durabilidade) | Normalmente suporta apenas transações básicas (por exemplo, inserção e exclusão de documentos) |
| Adequação para aplicativos | Bons para aplicativos que precisam garantir a integridade dos dados e/ou executar consultas complexas | Bons para aplicativos que exigem alta escalabilidade e/ou precisam armazenar grandes quantidades de dados não estruturados |
| Exemplos de serviços AWS | Amazon RDS, Amazon Aurora | Amazon DynamoDB, Amazon DocumentDB, Amazon Keyspaces |

### NoSQL Tipos
1. Bancos de Dados de Documentos: Os bancos de dados de documentos armazenam dados em documentos semiestruturados, como JSON ou XML, onde cada documento representa uma instância de um objeto. Eles permitem que os desenvolvedores armazenem dados com estrutura variável, em que cada documento pode ter um esquema diferente. Isso os torna adequados para aplicativos que precisam de flexibilidade no esquema de dados e escalabilidade. Alguns exemplos incluem MongoDB, Couchbase e Amazon DocumentDB.
2. Bancos de Dados de Colunas: Os bancos de dados de colunas armazenam dados em colunas em vez de linhas, permitindo melhor desempenho em operações de leitura e agregação. Eles são ideais para cenários em que o tempo de resposta é crítico, e quando há grande volume de dados e consulta de dados em larga escala. Exemplos incluem Apache Cassandra e Amazon Keyspaces.
3. Bancos de Dados de Grafos: Os bancos de dados de grafos armazenam dados em nós e arestas, permitindo a modelagem de dados complexos com relacionamentos. Eles são adequados para aplicativos que precisam de análise de dados, detecção de padrões, recomendadores e análise de redes sociais. Exemplos incluem Neo4j e Amazon Neptune.
4. Bancos de Dados Chave-Valor: Os bancos de dados chave-valor armazenam dados como pares chave-valor, permitindo acesso rápido aos dados. Eles são ideais para aplicativos que exigem escalabilidade, desempenho e baixa latência, como armazenamento em cache de sessões de usuários, gerenciamento de sessões e dados de perfil de usuário. Exemplos incluem Amazon DynamoDB e Redis.
5. Bancos de Dados de Objetos: Os bancos de dados de objetos armazenam objetos diretamente, sem que haja a necessidade de mapear para um modelo relacional. Eles são ideais para aplicativos que exigem escalabilidade, desempenho e baixa latência, como armazenamento em cache, gerenciamento de sessões, dados de perfil de usuário e outras aplicações. Exemplos incluem Oracle NoSQL Database e Amazon S3.
6. Bancos de Dados de Tempo de Série: Os bancos de dados de tempo de série armazenam dados em que cada registro possui um carimbo de data/hora. Eles são ideais para aplicativos que geram dados em tempo real, como sensores, servidores de IoT, dados de log e aplicações financeiras. Exemplos incluem Amazon Timestream e InfluxDB.

### Parallel Scan
A AWS Parallel Scan é um recurso disponível no Amazon DynamoDB que permite a leitura simultânea de várias partições de uma tabela em paralelo, aumentando a eficiência das operações de leitura e permitindo o processamento mais rápido de grandes volumes de dados.

Existem dois tipos de AWS 
1. Parallel Scan: Standard Parallel Scan: nesse tipo de operação, cada processo de varredura paralela é executado em uma thread separada e pode ser configurado para ler de uma ou mais partições em uma tabela do DynamoDB. Isso permite a leitura simultânea de várias partições e pode melhorar significativamente o tempo de leitura de grandes quantidades de dados.
2. Segment Parallel Scan: nesse tipo de operação, o DynamoDB divide a tabela em segmentos e atribui a cada processo de varredura paralela um segmento específico para ler. Cada processo de varredura paralela é executado em uma instância separada, o que permite escalar verticalmente a operação de leitura de grandes volumes de dados. Essa técnica é especialmente útil quando se trata de tabelas com muitas partições ou quando é necessário processar grandes volumes de dados em um curto espaço de tempo.


| [Anterior: Computação](./4_Computacao.md) | [Proximo: Monitoramento e Gerenciamento](./6_Monitoramento_e_Gerenciamento.md) |
|:----------------------------|-------------------------------------------------------------------------------:|