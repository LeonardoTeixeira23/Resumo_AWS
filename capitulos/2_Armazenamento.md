# Armazenamento

## Object Storage Service (OSS)
Object Storage Service (OSS) é um serviço de armazenamento de objetos oferecido pela Alibaba Cloud. O OSS permite que os usuários armazenem e gerenciem grandes quantidades de dados não estruturados, como imagens, vídeos, arquivos de áudio e outros tipos de conteúdo digital.
O OSS é altamente escalável e pode ser usado para armazenar quantidades ilimitadas de dados com segurança, durabilidade e alta disponibilidade. Ele é projetado para ser altamente durável e tolerante a falhas, com várias cópias de dados armazenados em diferentes locais geográficos para garantir a disponibilidade e a integridade dos dados.
Além disso, o OSS é altamente flexível e oferece recursos avançados, como armazenamento em camadas, compartilhamento de arquivos, criptografia de dados, controle de acesso e muito mais. O OSS é altamente compatível com outras soluções de computação em nuvem da Alibaba Cloud, como o Elastic Compute Service (ECS), Container Service, e funções de servidores.
O OSS pode ser usado para uma ampla gama de aplicativos, desde a hospedagem de sites estáticos até a transmissão de conteúdo de vídeo em larga escala. Ele é usado por empresas de todos os tamanhos e em todos os setores para armazenar e gerenciar grandes quantidades de dados não estruturados.

## S3
O Amazon S3 (Simple Storage Service) é um serviço de armazenamento de objetos na nuvem - AWS. Armazena e recupera grandes quantidades de dados de forma segura e escalável, utilizando uma interface web simples.
O S3 armazena dados como objetos, que podem ser arquivos de qualquer tipo ou tamanho. Esses objetos são armazenados em "buckets", que são como contêineres virtuais que podem ser acessados pela internet. Os buckets podem ser criados e gerenciados pelo usuário, e podem ser configurados para permitir acesso público ou privado.
O S3 oferece várias opções de armazenamento (S3 Standard, S3 Intelligent-Tiering, S3 Standard-Infrequent Access (S3 Standard-IA), S3 One Zone-Infrequent Access (S3 One Zone-IA), S3 Glacier, S3 Glacier Deep Archive, S3 Outposts.
O S3 também oferece recursos de segurança avançados, como criptografia de dados (SSE-S3, SSE-KMS, SSE-C), autenticação de usuários e controle de acesso (POLÍTICAS S3).
O S3 é amplamente utilizado para armazenar e distribuir conteúdo estático em sites e aplicativos, fazer backup e arquivamento de dados, e também para análise de big data e machine learning.

### Processos internos
Os processos internos do Amazon S3 são gerenciados pela infraestrutura da AWS e são automatizados para garantir disponibilidade e durabilidade dos dados armazenados.
Quando um usuário envia um objeto para o S3, o serviço automaticamente o divide em partes menores, chamadas de blocos, e os distribui em vários servidores em diferentes data centers da AWS. Essa técnica de distribuição de dados é conhecida como "sharding". Cada bloco é armazenado em pelo menos três servidores diferentes para garantir a durabilidade dos dados.
Os objetos no S3 são identificados por uma chave única, que é usada para recuperar o objeto posteriormente. O S3 utiliza o conceito de "consistência eventual" para garantir que os objetos estejam sempre disponíveis para leitura, mesmo que tenham sido atualizados recentemente. Isso significa que, após uma atualização, pode haver um pequeno atraso antes que todas as cópias do objeto estejam em sincronia.
O S3 também utiliza a replicação automática para fazer cópias dos dados em diferentes regiões da AWS para garantir a disponibilidade em caso de falhas em um data center ou região. Além disso, o S3 oferece opções de backup e recuperação de desastres, como a criação de snapshots e a replicação de dados para a AWS Glacier.
Em resumo, os processos internos do Amazon S3 são altamente automatizados e projetados para garantir alta disponibilidade, durabilidade e segurança dos dados armazenados, utilizando técnicas como sharding, replicação e consistência eventual.

### Políticas
As políticas do Amazon S3 são usadas para controlar o acesso aos buckets e objetos armazenados no serviço. As políticas são definidas em formato JSON e podem ser aplicadas em vários níveis, desde o nível de conta da AWS até o nível de objeto específico.
As políticas do S3 podem ser usadas para permitir ou negar o acesso a um bucket ou objeto para um ou mais usuários, grupos ou papéis da AWS. Isso inclui a definição de permissões de leitura, gravação e exclusão, bem como a restrição de acesso com base no endereço IP do solicitante.
Além disso, as políticas do S3 podem ser usadas para definir regras de versionamento, criptografia, arquivamento e retenção de objetos. Por exemplo, uma política pode ser usada para especificar que todos os objetos em um bucket devem ser criptografados usando um determinado algoritmo ou chave.
As políticas do S3 são altamente flexíveis e podem ser definidas e gerenciadas por meio do console da AWS, da API ou da linha de comando. A AWS também fornece um conjunto de políticas de exemplo que podem ser usadas como ponto de partida para criar políticas personalizadas.
Em resumo, as políticas do Amazon S3 são usadas para controlar o acesso e definir várias configurações de segurança e gerenciamento de objetos. Elas permitem aos usuários controlar rigorosamente quem pode acessar seus dados armazenados no S3 e como eles podem interagir com esses objetos.

### Encriptação

#### SSE-S3
SSE-S3 (Server-Side Encryption with Amazon S3) é um recurso do Amazon S3 que oferece criptografia automática de dados em repouso nos objetos armazenados no S3.
Ao habilitar a criptografia SSE-S3 em um bucket ou objeto específico, o S3 automaticamente criptografa os dados usando chaves gerenciadas pela AWS antes de serem armazenadas. Isso ajuda a proteger os dados contra acesso não autorizado e garante que os dados permaneçam criptografados enquanto estiverem armazenados no S3.
O SSE-S3 é uma opção de criptografia de dados em repouso no S3 e é uma das várias opções de criptografia disponíveis no serviço, incluindo o SSE-KMS (Server-Side Encryption with AWS KMS) e o SSE-C (Server-Side Encryption with Customer-Provided Keys).

#### SSE-KMS
SSE-KMS (Server-Side Encryption with AWS Key Management Service) é um recurso do Amazon S3 que oferece criptografia de dados em repouso nos objetos armazenados no S3 usando chaves de criptografia gerenciadas pelo serviço AWS KMS (Key Management Service).
Ao habilitar a criptografia SSE-KMS em um bucket ou objeto específico, o S3 criptografa automaticamente os dados usando uma chave de criptografia gerenciada pelo AWS KMS antes de serem armazenados. Isso ajuda a proteger os dados contra acesso não autorizado e garante que os dados permaneçam criptografados enquanto estiverem armazenados no S3.
O AWS KMS permite que as empresas gerenciem suas próprias chaves de criptografia mestra, que são usadas para criptografar as chaves de criptografia de dados usadas pelo S3. Com isso, as empresas podem controlar o acesso às suas chaves e garantir a conformidade com requisitos de conformidade e regulamentações.

#### SSE-C
SSE-C (Server-Side Encryption with Customer-Provided Keys) é um recurso do Amazon S3 que permite aos clientes criptografar objetos no S3 usando suas próprias chaves de criptografia.
Ao habilitar a criptografia SSE-C em um bucket ou objeto específico, o cliente fornece sua própria chave de criptografia, que é usada pelo S3 para criptografar os dados antes de serem armazenados. Isso ajuda a proteger os dados contra acesso não autorizado e garante que os dados permaneçam criptografados enquanto estiverem armazenados no S3.
A criptografia SSE-C é diferente da criptografia SSE-S3 e SSE-KMS, que usam chaves gerenciadas pela AWS para criptografar os dados. Com a criptografia SSE-C, o cliente é responsável por gerar, gerenciar e proteger suas próprias chaves de criptografia.
Ao usar a criptografia SSE-C, o cliente tem controle total sobre suas chaves de criptografia e pode manter a conformidade com requisitos de conformidade e regulamentações, como a Lei Geral de Proteção de Dados (LGPD) ou a Lei Geral de Proteção de Dados Pessoais (LGPD).

| Recurso          | SSE-S3                  | SSE-KMS                                                     | SSE-C                                                       |
|------------------|------------------------|-------------------------------------------------------------|-------------------------------------------------------------|
| Chave de criptografia gerenciada pelo cliente | Não                      | Sim                                                         | Sim                                                         |
| Tipo de chave de criptografia | Chave de criptografia AES-256  | Chave de criptografia AES-256 gerenciada pelo AWS Key Management Service (KMS) | Chave de criptografia AES-256 gerenciada pelo cliente |
| Gerenciamento de chave de criptografia | AWS gerencia a chave de criptografia | Cliente ou AWS gerencia a chave de criptografia | Cliente gerencia a chave de criptografia                      |
| Preços           | Sem custo adicional     | Custo adicional baseado no uso do AWS KMS e das operações de chave | Sem custo adicional                                         |

### Configurações
O Amazon S3 oferece uma ampla gama de configurações para personalizar a funcionalidade e o comportamento do serviço. Algumas das configurações mais importantes incluem:
1. Gerenciamento de acesso: o S3 permite controlar o acesso aos buckets e objetos armazenados usando políticas de acesso, permissões de usuários, grupos e papéis do IAM.
2. Criptografia: o S3 oferece várias opções de criptografia, incluindo o SSE-S3, SSE-KMS e SSE-C, que permitem criptografar objetos armazenados no bucket.
3. Versionamento: o versionamento do S3 permite rastrear as alterações em um objeto e recuperar versões anteriores, se necessário. Isso é útil para proteger os dados contra exclusões acidentais ou maliciosas.
4. Lifecycle: as configurações de ciclo de vida permitem que os objetos sejam movidos automaticamente para classes de armazenamento de custo mais baixo ou excluídos após um determinado período de tempo.
5. Logging: o S3 pode registrar atividades de acesso em logs, o que é útil para fins de auditoria e conformidade.
6. Transferência de dados: o S3 permite configurar a transferência de dados em massa para importar ou exportar grandes quantidades de dados de e para o S3.
7. Integrações com outros serviços: o S3 pode ser integrado com outros serviços da AWS, como o AWS Lambda, para processar objetos armazenados no S3.
8. Gerenciamento de versão do bucket: permite habilitar o versionamento do bucket para rastrear as alterações feitas em todos os objetos armazenados no bucket.
9. Política de ciclo de vida: permite criar regras de ciclo de vida que definem quando objetos podem ser movidos para outras classes de armazenamento, excluídos ou arquivados.
10. Controle de acesso baseado em objeto: permite criar políticas de controle de acesso baseadas em objeto para controlar o acesso a objetos específicos em um bucket.
11. Cross-Region Replication (CRR): permite replicar automaticamente objetos entre buckets em diferentes regiões do S3 para proteger contra interrupções de serviços.
12. Transfer Acceleration: permite acelerar a transferência de dados de e para o S3 usando uma rede de entrega de conteúdo (CDN) global.
13. Configurações de segurança: incluem a capacidade de configurar políticas de segurança avançadas para proteger os dados armazenados no S3, como políticas de segurança de rede, autenticação de usuário e criptografia de chave de cliente.

### Wide Range Storage Classes
O Amazon S3 oferece uma ampla gama de classes de armazenamento para atender às necessidades de diferentes casos de uso e requisitos de custo e desempenho. Algumas das classes de armazenamento disponíveis no Amazon S3 incluem:
1. S3 Standard: projetado para armazenamento de dados frequente e acesso imediato.
2. S3 Intelligent-Tiering: projetado para otimizar os custos de armazenamento movendo automaticamente os dados entre duas camadas de acesso com base em padrões de uso.
3. S3 Standard-Infrequent Access (S3 Standard-IA): projetado para armazenamento de dados que não são acessados com frequência, mas exigem acesso rápido quando necessário.
4. S3 One Zone-Infrequent Access (S3 One Zone-IA): projetado para armazenamento de dados que podem ser reproduzidos em uma única zona de disponibilidade.
5. S3 Glacier: projetado para arquivamento de dados de longo prazo com acesso em horas.
6. S3 Glacier Deep Archive: projetado para arquivamento de dados de longo prazo com acesso em horas.
7. S3 Outposts: projetado para armazenamento de dados local em racks de servidores em instalações de clientes.

### Bucket
Um bucket é um contêiner virtual que pode ser usado para armazenar dados no serviço de armazenamento em nuvem da AWS, o Amazon S3. O bucket é uma espécie de diretório que pode conter vários objetos, como arquivos de texto, imagens, vídeos, arquivos de áudio e outros tipos de dados.
Os buckets são usados para organizar e gerenciar os objetos no S3. Cada bucket tem um nome único globalmente, que é usado para identificar o bucket na URL de acesso do objeto. Os buckets também podem ser criados em qualquer região da AWS e podem ser configurados para permitir ou negar o acesso público.
Os objetos em um bucket são armazenados e replicados em diferentes servidores em vários data centers da AWS, garantindo alta disponibilidade e durabilidade dos dados. Além disso, o S3 oferece recursos de segurança avançados, como a criptografia de dados em repouso e em trânsito, controle de acesso e monitoramento de acesso a objetos.
Os buckets do S3 são amplamente utilizados para armazenamento e distribuição de conteúdo estático em sites e aplicativos, backup e arquivamento de dados, análise de big data e machine learning, entre outros usos.
Em resumo, um bucket na AWS é um contêiner virtual que é usado para armazenar e organizar objetos no serviço de armazenamento em nuvem da AWS, o Amazon S3. Cada bucket tem um nome único globalmente e pode ser configurado com opções de segurança avançadas.

#### Key
No contexto da AWS, "key" em um bucket se refere a um identificador único para um objeto armazenado em um bucket S3. A chave é composta por um nome e um caminho que especifica a localização do objeto dentro do bucket. A chave é usada para identificar e acessar objetos em um bucket S3, e ela é usada como parte da URL que os usuários usam para acessar o objeto na web. A chave é importante para a organização e gerenciamento de objetos em um bucket S3, e deve ser escolhida cuidadosamente para evitar conflitos ou problemas de desempenho.

#### Policy
A política de bucket (bucket policy) é um recurso do Amazon S3 que permite aos usuários especificar permissões de acesso a um bucket e aos objetos armazenados nele. Essa política é escrita em formato JSON e pode ser usada para conceder ou negar permissões de acesso a usuários, grupos de usuários ou a serviços da AWS.
A política de bucket é útil para gerenciar o acesso a objetos em um bucket S3, permitindo que os usuários controlem quem pode acessar o bucket e como o acesso pode ser feito. Por exemplo, a política de bucket pode ser usada para conceder permissões de leitura ou gravação a um usuário específico ou a um grupo de usuários, ou para restringir o acesso a um intervalo de endereços IP específicos.
Ao criar uma política de bucket, é importante entender os princípios básicos de segurança da AWS, como o controle de acesso baseado em função (RBAC) e o modelo de segurança de responsabilidade compartilhada. Além disso, é recomendável testar e revisar regularmente a política de bucket para garantir que ela esteja funcionando corretamente e cumprindo as necessidades de segurança e conformidade da organização.

#### Objetos
Objetos são as entidades fundamentais armazenadas no Amazon S3. É necessário conceder explicitamente permissões a outras pessoas para acessar seus objetos. Cada objeto possui dados, uma chave e metadados. A chave do objeto (ou nome da chave) identifica exclusivamente o objeto em um bucket.
O Amazon S3 mantém um conjunto de metadados do sistema e do usuário para cada objeto e processa os metadados do sistema conforme necessário para o gerenciamento de armazenamento.
O Amazon S3 tem uma estrutura plana em vez de uma hierarquia como você pode ver em um sistema de arquivos. No entanto, o console suporta o conceito de pasta como um meio de agrupar objetos, usando um prefixo de nome compartilhado para objetos na mesma pasta.
Use esta página para ver todos os objetos em um bucket ou pasta, criar uma pasta ou fazer o upload de um objeto. Você pode abrir, baixar, excluir e copiar a URL de objetos selecionados. Você também pode realizar ações de objeto como calcular tamanho, copiar, restaurar, editar e consultar com S3 Select.

#### Propriedades

Na guia Propriedades do bucket, você pode editar as configurações do bucket para atender ao seu caso de uso.
Proteja seu armazenamento
Para salvar várias cópias distintas de seus dados e recuperar facilmente tanto de ações de usuário não intencionais quanto de falhas de aplicativo, habilite a Versioning do Amazon S3. A Versioning do S3 é necessária para habilitar outras opções de proteção de dados para o Amazon S3, incluindo o Object Lock do S3 e a Replicação do S3.
Proteja seu armazenamento
Para criptografar automaticamente e proteger ainda mais os novos objetos que são adicionados ao seu bucket, habilite a criptografia padrão com chaves gerenciadas pelo Amazon S3 ou chaves do AWS Key Management Service.
Arquive objetos raramente acessados
Para objetos que são raramente acessados por longos períodos de tempo, crie uma configuração de Arquivo do S3 Intelligent-Tiering que ativa um ou ambos os níveis de acesso de arquivo do S3 Intelligent-Tiering. Depois de ativar um ou ambos os níveis de acesso de arquivo, o S3 Intelligent-Tiering move automaticamente os objetos com base em quão frequentemente eles são acessados. Objetos que não foram acessados por 90 dias consecutivos são movidos para o nível de Acesso do Arquivo. Objetos que não foram acessados por 180 dias consecutivos são movidos para o nível de Acesso do Arquivo Profundo.

### Monitore o Acesso ao Bucket e Eventos
Configure ferramentas de registro para monitorar e controlar como seus recursos S3 estão sendo usados. Para obter registros detalhados das solicitações feitas ao seu bucket, habilite o registro de acesso do servidor. Para registrar as ações tomadas por um usuário, uma função ou em seu bucket do S3, configure eventos de dados do AWS CloudTrail no console do CloudTrail. Para iniciar fluxos de trabalho que usam o Amazon Simple Notification Service (Amazon SNS), o Amazon Simple Queue Service (Amazon SQS) e o AWS Lambda quando ocorre uma alteração em seus recursos do S3, crie uma notificação de evento.
Para obter informações adicionais sobre o uso do seu bucket, recomendamos que você vá para a página S3 Storage Lens e configure um painel e habilite métricas gratuitas. Depois de fazer isso, você pode visualizar seu painel padrão a partir da página da lista de Buckets.
Atenda aos requisitos de conformidade
Com o Object Lock do S3, você pode armazenar objetos no Amazon S3 usando um modelo de gravação uma vez e leitura muitas vezes (WORM). Para atender aos requisitos de retenção de conformidade de dados, você pode usar o Object Lock para impedir que um objeto seja excluído ou sobrescrito por um tempo fixo ou indefinidamente. Você pode configurar o Object Lock para se aplicar a todos os objetos no bucket ou apenas a certos objetos.
Explore outras opções
Use o seu bucket do S3 para hospedar um site estático. Habilite a Transferência Acelerada para transferências de arquivos rápidas e seguras em longas distâncias. Habilite o Pagador de Solicitação para compartilhar dados sem incorrer em cobranças associadas a outros acessando os dados.

## EBS
Amazon Elastic Block Store (EBS) é um serviço de armazenamento de blocos de alta performance para uso com instâncias do Amazon Elastic Compute Cloud (EC2). Ele fornece volumes de armazenamento persistente que podem ser anexados a uma instância do EC2 e usados como um disco rígido padrão.
O Amazon EBS oferece vários tipos de volumes de armazenamento, incluindo:
SSDs provisionados (gp2): projetado para cargas de trabalho que exigem um desempenho consistente de IOPS (operações de entrada/saída por segundo) com baixa latência.
Throughput otimizado HDDs (st1): projetado para cargas de trabalho que exigem alto throughput de leitura/gravação e acesso frequente a grandes conjuntos de dados.
HDDs de capacidade (sc1): projetado para cargas de trabalho que exigem alto throughput de leitura/gravação e acesso a grandes volumes de dados, com requisitos de custo mais baixos.
Cold HDDs (sc1): projetado para cargas de trabalho que exigem acesso a dados menos frequentes, com requisitos de custo mais baixos.
O Amazon EBS permite criar e modificar volumes de armazenamento, anexá-los a instâncias do EC2 e fazer backups e snapshots para proteger os dados armazenados. Ele também oferece recursos de criptografia de dados em repouso e replicação de volumes para garantir a disponibilidade contínua dos dados armazenados.
Em resumo, o Amazon Elastic Block Store é um serviço de armazenamento de blocos altamente escalável e confiável que ajuda a fornecer armazenamento persistente para as instâncias do EC2 da AWS.
Os EBS Elastic Volumes são uma funcionalidade adicional do serviço EBS que permite alterar o tamanho e o tipo de volume sem interromper a instância EC2. Com os EBS Elastic Volumes, é possível aumentar ou diminuir o tamanho do volume e alterar o tipo de armazenamento (por exemplo, de SSD para HDD) sem precisar parar a instância EC2 ou fazer backup e restauração dos dados. Isso proporciona maior flexibilidade e facilidade na gestão de armazenamento, permitindo que os usuários ajustem rapidamente a capacidade e o desempenho do armazenamento para atender às necessidades de suas aplicações.

### Benefícios
O Amazon Elastic Block Store (EBS) oferece uma variedade de benefícios para usuários que precisam de armazenamento em bloco confiável e escalável em nuvem. Aqui estão alguns dos benefícios mais importantes do Amazon EBS:
1. Disponibilidade: O EBS oferece alta disponibilidade e durabilidade para seus volumes de armazenamento em bloco. Os dados são replicados automaticamente em várias zonas de disponibilidade para ajudar a evitar a perda de dados e interrupções de serviços.
2. Escalabilidade: O EBS é altamente escalável e pode ser facilmente dimensionado verticalmente ou horizontalmente para atender às necessidades em constante evolução de seus aplicativos. Você pode adicionar, expandir e excluir volumes sem interromper suas instâncias EC2.
3. Desempenho: O EBS fornece volumes de armazenamento de alto desempenho com diferentes tipos de volume, incluindo SSD, HDD e provisioned IOPS, permitindo que você selecione o tipo de volume mais adequado para suas cargas de trabalho.
4. Segurança: O EBS permite criptografar dados em repouso em volumes usando chaves gerenciadas pela AWS. Isso ajuda a garantir a privacidade e a proteção dos dados do usuário.
5. Flexibilidade: O EBS é altamente flexível e fornece vários recursos, como snapshots, elastic volumes, replicação cruzada de regiões e provisioned IOPS, para atender às necessidades de diferentes tipos de aplicativos.
6. Integração com outros serviços AWS: O EBS é integrado com outros serviços AWS, como Amazon EC2, Amazon RDS, Amazon Redshift e Amazon EMR, permitindo que você crie soluções de armazenamento altamente escaláveis e confiáveis para seus aplicativos.

### Features
Alguns dos recursos e funcionalidades do EBS incluem:
1. Snapshots: permitem criar uma cópia de backup de um volume EBS para armazenamento no Amazon Simple Storage Service (S3).
2. Volume Types: fornece diferentes tipos de volumes de armazenamento com características específicas de desempenho, durabilidade e custo, incluindo SSD, HDD, Cold HDD e Magnetic.
3. Elastic Volumes: permite alterar o tamanho e o tipo de volume sem interromper a instância EC2, fornecendo maior flexibilidade e facilidade na gestão de armazenamento.
4. Encryption: permite criptografar os dados armazenados nos volumes EBS usando chaves gerenciadas pela AWS.
5. Cross-Region Replication: permite replicar automaticamente os snapshots de volumes EBS para outra região da AWS para fins de backup e recuperação de desastres.
6. Fast Snapshot Restore: permite restaurar rapidamente os snapshots EBS, melhorando a disponibilidade de aplicativos e reduzindo o tempo de inatividade.
7. Provisioned IOPS: permite provisionar IOPS (operações de entrada/saída por segundo) para volumes de armazenamento que exigem alta performance de I/O.
8. Multi-Attach: permite anexar um volume EBS a várias instâncias EC2 simultaneamente, o que é útil para cargas de trabalho compartilhadas ou de alta disponibilidade.

### Snapshot
Um snapshot é uma cópia do estado de um volume do EBS em um determinado ponto no tempo. Ele captura o estado do volume do EBS, incluindo todos os dados e metadados, como permissões e atributos. Os snapshots do EBS são armazenados no Amazon S3, o que garante durabilidade e disponibilidade dos dados.
Os snapshots do EBS são uma maneira eficiente de fazer backup e restaurar volumes do EBS, além de serem uma ferramenta útil para criar novos volumes do EBS a partir de um ponto de partida conhecido. Por exemplo, se você precisa criar uma nova instância do Amazon EC2 que seja semelhante a uma instância existente, você pode usar um snapshot do EBS dessa instância para criar um novo volume do EBS e, em seguida, usar esse volume para criar uma nova instância do EC2.
Os snapshots do EBS também são usados para criar backups incrementais. Quando um snapshot é criado, apenas os blocos modificados desde o último snapshot são copiados, o que economiza tempo e espaço em disco. Além disso, os snapshots do EBS podem ser copiados para outras regiões do AWS para fins de recuperação de desastres ou para serem usados como base para volumes do EBS em outras regiões.
Em resumo, o snapshot do EBS é uma ferramenta importante para fazer backup e restaurar volumes do EBS, criar novos volumes do EBS a partir de um ponto de partida conhecido e para criar backups incrementais de seus dados do EBS.

### DLM
O Amazon Data Lifecycle Manager (DLM) é um serviço que ajuda a gerenciar automaticamente a criação, retenção e exclusão de snapshots de volumes do EBS. Com o DLM, você pode definir políticas de ciclo de vida para os seus snapshots, o que pode ajudar a garantir que os dados estejam disponíveis quando você precisar deles e também reduzir os custos de armazenamento.
O Amazon DLM oferece vários recursos, incluindo:
1. Programação flexível: você pode definir políticas de ciclo de vida para seus snapshots, com a opção de programar a execução dessas políticas de acordo com as suas necessidades.
2. Políticas personalizadas: você pode criar políticas de ciclo de vida personalizadas que atendam às suas necessidades específicas, como a definição de uma programação para a criação e retenção de snapshots, bem como a exclusão automática de snapshots antigos.
3. Controle granular: você pode definir políticas de ciclo de vida para diferentes volumes, dependendo de suas necessidades específicas de armazenamento.
4. Integração com AWS Backup: o Amazon DLM é totalmente integrado com o AWS Backup, permitindo que você crie e gerencie políticas de ciclo de vida para seus snapshots de EBS através de uma única interface.
5. Redução de custos: com a programação de políticas de ciclo de vida, você pode automatizar a exclusão de snapshots antigos, ajudando a reduzir os custos de armazenamento.
Em resumo, o Amazon DLM ajuda a automatizar o gerenciamento de snapshots de EBS, proporcionando maior flexibilidade, personalização e controle granular sobre as políticas de ciclo de vida. Isso pode ajudar a garantir a disponibilidade de dados quando você precisar deles, bem como reduzir os custos de armazenamento.

### FSR
Fast Snapshot Restore (FSR) é um recurso da AWS que permite a restauração rápida de snapshots do Amazon Elastic Block Store (EBS).
Com o FSR, os snapshots EBS são armazenados em caches em uma instância EC2 dedicada e podem ser restaurados em questão de segundos, em vez de minutos, o que é o tempo necessário para restaurar os snapshots tradicionalmente. Isso ajuda a melhorar a disponibilidade de aplicativos e reduzir o tempo de inatividade, pois os volumes EBS podem ser restaurados rapidamente a partir de snapshots sem a necessidade de esperar por um longo processo de restauração.
O FSR pode ser ativado para cada snapshot EBS individualmente ou em lote usando as APIs da AWS ou o console de gerenciamento. É importante notar que o FSR está disponível apenas em algumas regiões da AWS e pode ser cobrado pelo uso do recurso.

## EFS
O Amazon Elastic File System (EFS) é um serviço de armazenamento de arquivos gerenciado pela AWS que fornece armazenamento de arquivos altamente escalável e acessível para cargas de trabalho baseadas em nuvem. Com o EFS, as empresas podem armazenar e acessar arquivos diretamente de suas instâncias EC2, compartilhando dados entre várias instâncias, sem a necessidade de gerenciar a infraestrutura de armazenamento subjacente.
O EFS é projetado para ser altamente escalável, com capacidade de se adaptar dinamicamente ao crescimento de dados e de armazenar petabytes de arquivos. Ele também oferece alta disponibilidade, com redundância de dados multi-az (disponível em várias zonas de disponibilidade), tornando-o uma solução adequada para aplicativos com requisitos críticos de tempo de atividade. Além disso, o EFS é altamente seguro, permitindo o controle de acesso baseado em políticas e criptografia de dados em repouso e em trânsito.
O EFS pode ser usado em uma ampla gama de casos de uso, incluindo sites, aplicativos móveis, análise de big data, processamento de mídia e desenvolvimento de software. Com o EFS, as empresas podem aproveitar os benefícios do armazenamento de arquivos na nuvem, incluindo a flexibilidade, escalabilidade e economia de custos, sem a necessidade de gerenciar a infraestrutura subjacente.

### EFS IA
AWS EFS IA (Amazon Elastic File System Infrequent Access) é um serviço da AWS que fornece armazenamento de arquivos acessível pela Internet, que é escalável, seguro e altamente disponível. Ele oferece aos usuários um armazenamento de dados eficiente e econômico, com acesso a arquivos frequentes e não frequentes, em um único sistema de arquivos.
O Amazon EFS IA é uma opção de armazenamento mais barata para arquivos que não são acessados ​​com frequência, como backups, arquivos de log, arquivos de vídeo e outros tipos de dados menos usados. Ele usa a mesma infraestrutura de armazenamento de dados do Amazon EFS padrão, porém com a capacidade de reduzir os custos de armazenamento em até 85% em comparação com o Amazon EFS padrão.
Em resumo, o AWS EFS IA é um serviço de armazenamento de arquivos altamente escalável, seguro e econômico, que permite aos usuários acessar arquivos frequentes e não frequentes de um sistema de arquivos compartilhado e reduzir significativamente os custos de armazenamento de dados.

### Perfomance modes
O AWS EFS Performance Modes são modos de desempenho que podem ser selecionados ao criar um sistema de arquivos do EFS. Existem dois modos de desempenho disponíveis: "General Purpose" (Uso geral) e "Max I/O" (Máximo de E/S).
O modo "General Purpose" é adequado para a maioria das cargas de trabalho e oferece um equilíbrio entre o desempenho de leitura e gravação. Já o modo "Max I/O" é projetado para cargas de trabalho intensivas em leitura e gravação, como grandes bancos de dados ou aplicativos de processamento de vídeo. Ele oferece um desempenho de leitura e gravação mais alto, mas com um custo maior de operação.
Ao selecionar o modo de desempenho correto para o seu sistema de arquivos do EFS, você pode garantir que seus aplicativos e cargas de trabalho tenham o desempenho ideal e eficiente.

### Troughput modes
O EFS oferece opções de throughput modes (modos de taxa de transferência) que determinam a velocidade e o desempenho com que os dados são transferidos para e a partir do sistema de arquivos. Existem dois tipos de throughput modes no AWS EFS: o modo "Provisioned" e o modo "Bursting".
No modo "Provisioned", o usuário escolhe uma taxa de transferência predefinida e paga um preço fixo para manter essa taxa constante. Esse modo é ideal para aplicativos com requisitos de desempenho consistentes e previsíveis.
No modo "Bursting", a taxa de transferência é determinada pela quantidade de dados armazenados no EFS. Quando o sistema de arquivos está ocioso, ele acumula créditos de burst que podem ser usados para aumentar a taxa de transferência em momentos de pico de uso. Esse modo é mais adequado para aplicativos com requisitos de desempenho variáveis e que podem lidar com atrasos ocasionais.
Em resumo, os throughput modes no AWS EFS são uma forma flexível e escalável de gerenciar a taxa de transferência de dados em um sistema de arquivos na nuvem, permitindo que os usuários escolham a opção mais adequada para suas necessidades específicas.

### EFS Containers
O AWS EFS (Elastic File System) Containers é um serviço da AWS que oferece uma solução de armazenamento de arquivos escalável e flexível para containers em ambientes de computação em nuvem. Com o EFS Containers, é possível armazenar dados de aplicativos de containers em um sistema de arquivos compartilhado, permitindo que vários containers acessem e compartilhem os mesmos arquivos simultaneamente. Isso facilita a criação de aplicativos altamente disponíveis e tolerantes a falhas, além de permitir que os desenvolvedores criem, implantem e gerenciem aplicativos de containers de forma mais eficiente. O EFS Containers é integrado com o Amazon Elastic Container Service (ECS) e o Kubernetes, permitindo que os usuários gerenciem facilmente o armazenamento de arquivos para seus aplicativos de containers em ambientes de nuvem AWS.

### EFS, fFSx, FSx for Lustre
AWS EFS (Amazon Elastic File System) é um serviço de armazenamento em nuvem totalmente gerenciado que fornece um sistema de arquivos compartilhado para uso com instâncias do Amazon EC2 (Elastic Compute Cloud). Ele é escalável, elástico e fornece acesso de leitura e gravação para múltiplas instâncias de EC2, permitindo que vários usuários acessem os mesmos arquivos simultaneamente.
AWS FSx (Amazon FSx) é um serviço gerenciado de armazenamento de arquivos nativo na nuvem que oferece um sistema de arquivos Windows e Linux totalmente compatível com o servidor, projetado para execução em instâncias do Amazon EC2. Ele é dimensionável, seguro e fornece acesso a arquivos de alta performance.
O FSx para Lustre é uma opção adicional do serviço FSx que permite a execução de aplicativos de alto desempenho que requerem acesso a sistemas de arquivos de alta performance. O FSx para Lustre é um sistema de arquivos distribuído e paralelo que é altamente escalável e projetado para aplicações que exigem altas taxas de transferência de dados, como computação de alto desempenho (HPC), modelagem e simulação, processamento de imagens e vídeo, entre outros. Ele é executado no cluster Lustre, que é um sistema de arquivos de código aberto usado por organizações de todo o mundo para executar aplicações de HPC.
| Recurso | Amazon EFS | Amazon FSx para Windows File Server | Amazon FSx para Lustre |
| --- | --- | --- | --- |
| Tipo de serviço | Serviço de armazenamento de arquivos | Serviço de armazenamento de arquivos | Serviço de armazenamento de arquivos |
| Protocolos suportados | NFS | SMB | Lustre |
| Escalabilidade | Escalabilidade automática, sem limites de capacidade | Escalabilidade vertical (adicionar mais armazenamento) e horizontal (adicionar mais instâncias) | Escalabilidade vertical (adicionar mais armazenamento) e horizontal (adicionar mais instâncias) |
| Recursos compartilhados | Compartilhamento de arquivos em vários sistemas de arquivos | Compartilhamento de arquivos em vários sistemas de arquivos | Compartilhamento de arquivos em vários sistemas de arquivos |
| Acesso | Acesso de arquivos simultâneo de várias instâncias | Acesso de arquivos simultâneo de várias instâncias | Acesso de arquivos simultâneo de várias instâncias |
| Integração com o Active Directory | Não | Sim | Sim |
| Casos de uso recomendados | Compartilhamento de arquivos entre várias instâncias EC2 | Migração de aplicativos do Windows para a nuvem | Processamento de dados em paralelo, HPC, simulações e análises de big data |
| Custo | Faturamento por GB de armazenamento e transferência de dados | Faturamento por hora da instância EC2 e armazenamento | Faturamento por hora da instância EC2 e armazenamento |

### Instance Store
O Instance Store é um serviço de armazenamento temporário oferecido pela AWS que fornece armazenamento local para as instâncias EC2 (Elastic Compute Cloud) na nuvem da AWS. Ao contrário do Amazon EBS (Elastic Block Store) e do Amazon EFS (Elastic File System), o Instance Store oferece armazenamento temporário diretamente associado a uma instância EC2 e, portanto, não é persistente.
O Instance Store é um tipo de armazenamento que é fornecido localmente em uma instância EC2 física e não está disponível para outras instâncias. Ele é projetado para oferecer alta velocidade e baixa latência de leitura e gravação, tornando-o ideal para aplicativos com requisitos de I/O intensivos, como processamento de banco de dados em memória, cache de aplicativos e processamento de big data.
As limitações do Instance Store incluem sua natureza não persistente e não escalável. Uma vez que os dados armazenados no Instance Store são perdidos quando a instância é interrompida ou terminada, ele deve ser usado apenas para dados temporários e descartáveis. O Instance Store também não pode ser ampliado para atender a necessidades de armazenamento adicionais, o que pode ser uma limitação para aplicativos que exigem grande capacidade de armazenamento.
Em resumo, o Instance Store é uma opção de armazenamento local de alta velocidade para dados temporários e não críticos que exigem baixa latência. É importante considerar as limitações da Instance Store ao escolher a opção de armazenamento mais adequada para uma carga de trabalho específica.
| Características | EBS | EFS | Instance Store |
| --- | --- | --- | --- |
| Tipo de armazenamento | Bloco | Arquivo | Temporário |
| Persistência | Persistente | Persistente | Não persistente |
| Capacidade de armazenamento | Até 16 TB | Até petabytes | Limitado pela instância |
| Acesso simultâneo | Apenas um ponto de montagem por vez | Vários pontos de montagem simultâneos | N/A |
| Desempenho | Boa performance | Bom desempenho para acesso aleatório e baixo desempenho para acesso sequencial | Alto desempenho para acesso sequencial |
| Recuperação de desastres | Snapshots e replicação de região | Replicação de região | Não é possível fazer backup e restauração |
| Uso recomendado | Banco de dados, aplicativos críticos | Compartilhamento de arquivos, ambientes de desenvolvimento | Processamento temporário de dados, cache, logs |



