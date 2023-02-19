# Monitoramento e Gerenciamento

## CloudTrail
Existem dois tipos de AWS CloudTrail:
1. AWS CloudTrail para serviços da AWS: este tipo de CloudTrail registra eventos de chamada de API para serviços da AWS, como Amazon S3, Amazon EC2, Amazon RDS, AWS Lambda, Amazon CloudFront, entre outros. O CloudTrail para serviços da AWS captura informações sobre a atividade do usuário, como quem iniciou a ação, o que foi feito, quando foi feito e qual endereço IP foi usado.
2. AWS CloudTrail para eventos do AWS Organization: este tipo de CloudTrail registra eventos de chamada de API para as contas da AWS em uma organização. Ele captura informações sobre a atividade do usuário, incluindo quem fez a ação, o que foi feito, quando foi feito e qual endereço IP foi usado. Isso pode ajudar a monitorar e rastrear atividades em várias contas AWS e em uma organização AWS.

Ambos os tipos de AWS CloudTrail permitem que os usuários monitorem a atividade da conta da AWS, solucionem problemas de conformidade e auditoria e identifiquem possíveis ameaças à segurança.

## CloudWatch
AWS CloudWatch é um serviço de monitoramento e observabilidade da AWS que coleta e rastreia métricas, logs e eventos em tempo real dos recursos em nuvem da AWS, como instâncias EC2, bancos de dados RDS, Lambda functions, entre outros. Ele fornece insights em tempo real sobre o desempenho dos recursos e permite que os usuários visualizem e analisem dados de monitoramento usando gráficos e alarmes.

Com o CloudWatch, os usuários podem monitorar a utilização de recursos, detectar anomalias e tomar medidas proativas para manter o desempenho e a disponibilidade dos recursos em alta. Além disso, o CloudWatch permite criar alarmes baseados em métricas para notificar quando determinadas condições são atendidas, como um aumento na utilização da CPU ou queda de conexões em um banco de dados.

O CloudWatch também integra com outros serviços da AWS, como o AWS Lambda, permitindo a coleta de logs de aplicativos e a monitoração de funções. Em resumo, o AWS CloudWatch é um serviço essencial para garantir a saúde e o desempenho dos recursos em nuvem da AWS.

## Pricing Calculator
O AWS Pricing Calculator é uma ferramenta da Amazon Web Services (AWS) que permite estimar o custo dos serviços da AWS antes de usá-los. Com o AWS Pricing Calculator, você pode criar estimativas de custos para serviços individuais ou combinações de serviços da AWS.

A ferramenta é útil para ajudar as empresas a entenderem quanto custará a utilização dos serviços da AWS e para planejarem seus orçamentos. Além disso, ela permite comparar os preços dos diferentes serviços da AWS e escolher a opção mais adequada.

Para usar o AWS Pricing Calculator, é necessário selecionar os serviços que você pretende usar e configurá-los de acordo com suas necessidades, como a região onde serão executados, a quantidade de recursos necessários e o tempo de uso. A ferramenta então calcula automaticamente o custo com base nas informações fornecidas.


Vale ressaltar que o AWS Pricing Calculator é apenas uma estimativa e que os preços reais podem variar dependendo de diversos fatores, como a demanda, a região geográfica, o tipo de instância escolhido e outros. Portanto, é sempre importante verificar a fatura real após a utilização dos serviços da AWS para confirmar os custos reais.

### PAYG
AWS Pay-As-You-Go (PAYG) é um modelo de pagamento da Amazon Web Services, em que o usuário paga somente pelos recursos de computação e serviços de nuvem que são utilizados. Essa modalidade de pagamento permite que o usuário tenha acesso aos recursos de computação da AWS sem precisar adquirir servidores e infraestrutura própria, o que reduz custos e aumenta a flexibilidade na gestão de recursos.

O AWS PAYG permite que o usuário pague somente pelo uso dos recursos de computação, como a capacidade de armazenamento, processamento, transferência de dados e outros serviços que são oferecidos pela plataforma de nuvem da Amazon. Dessa forma, o usuário pode reduzir custos ao utilizar os recursos apenas quando for necessário, sem precisar adquirir servidores e infraestrutura própria.

Além disso, o AWS PAYG também oferece a possibilidade de escalabilidade e flexibilidade, permitindo que o usuário aumente ou diminua os recursos de acordo com a demanda de trabalho e evite gastos desnecessários. Com isso, é possível ter mais controle e visibilidade sobre os custos e a gestão de recursos de computação na nuvem.

## AWS Datasync
AWS DataSync é um serviço de transferência de dados da AWS que facilita a transferência de grandes quantidades de dados entre sistemas de armazenamento on-premises e serviços de armazenamento na nuvem, como o Amazon S3, o Amazon EFS, entre outros. Ele permite transferir dados de forma rápida, segura e automatizada, reduzindo os tempos de transferência e minimizando os custos de largura de banda.

O AWS DataSync é projetado para suportar uma ampla gama de casos de uso, como backup, recuperação de desastres, migração de dados, compartilhamento de dados entre locais e muito mais. Ele oferece recursos avançados, como criptografia de dados em trânsito e em repouso, transferência de dados delta para reduzir a quantidade de dados transferidos, integração com IAM (Identity and Access Management), suporte para protocolos de transferência de dados padrão do setor, como NFS e SMB, e muito mais.

Em resumo, o AWS DataSync é uma ferramenta poderosa para simplificar a transferência de grandes quantidades de dados entre sistemas de armazenamento on-premises e serviços de armazenamento na nuvem, proporcionando maior eficiência, segurança e redução de custos.

## Life Cycle Hooks
AWS Lifecycle Hooks é um recurso disponível no AWS Elastic Compute Cloud (EC2) que permite aos usuários configurar scripts para serem executados automaticamente quando ocorre uma transição de estado em uma instância do EC2. As transições de estado incluem inicialização, terminação e paralisação.

Por meio do AWS Lifecycle Hooks, é possível adicionar scripts personalizados em pontos específicos do ciclo de vida de uma instância, permitindo que os usuários gerenciem os processos de inicialização, finalização e paralisação da instância de maneira mais eficiente. O recurso ajuda a garantir que os processos sejam concluídos com êxito antes da transição de estado da instância, minimizando os riscos de interrupção ou perda de dados.

Os usuários podem criar ganchos personalizados para executar ações personalizadas, como executar um script específico ou enviar uma mensagem para um serviço de notificação, quando uma instância é iniciada ou encerrada. Isso pode ajudar a gerenciar a carga de trabalho do servidor e a melhorar a eficiência da instância.

Em resumo, AWS Lifecycle Hooks é uma ferramenta útil que ajuda a gerenciar as transições de estado das instâncias do EC2 e automatizar tarefas personalizadas para garantir a eficiência e segurança de suas aplicações em nuvem.

## Well-Architected
O AWS Well-Architected é um conjunto de melhores práticas e diretrizes desenvolvidas pela Amazon Web Services para ajudar os clientes a criar arquiteturas seguras, eficientes e confiáveis na nuvem. O serviço oferece um framework que ajuda as organizações a avaliar e aperfeiçoar as arquiteturas de suas aplicações e sistemas, garantindo que eles estejam alinhados aos principais princípios de segurança, confiabilidade, eficiência, desempenho e custo-efetividade.

O AWS Well-Architected fornece uma metodologia para avaliar, planejar e otimizar arquiteturas de nuvem de acordo com cinco pilares: excelência operacional, segurança, eficiência de custos, desempenho e resiliência. O serviço também oferece ferramentas e recursos para ajudar os clientes a implementar essas melhores práticas, incluindo relatórios de avaliação, orientação de especialistas em AWS, e acesso a ferramentas de automatização e monitoramento.

Em resumo, o AWS Well-Architected é uma ferramenta poderosa para ajudar as organizações a criar e manter infraestruturas de nuvem seguras, escaláveis, eficientes e confiáveis, maximizando o valor dos investimentos em nuvem.

### Os 6 pilares 
O AWS Well-Architected é um framework da Amazon Web Services (AWS) que ajuda os usuários a criar, projetar e manter arquiteturas de nuvem seguras, escaláveis, eficientes e resilientes. O framework é baseado em 6 pilares que fornecem diretrizes para projetar, construir e operar soluções na nuvem:
1. Segurança: garante a proteção dos dados e sistemas, seguindo as melhores práticas de segurança e compliance.
2. Confiabilidade: garante que os sistemas estejam sempre disponíveis e resistentes a falhas.
3. Eficiência de desempenho: garante que os recursos sejam usados de maneira eficiente para reduzir custos e maximizar a performance.
4. Excelência operacional: garante a automação e a gestão eficiente de operações de TI para aumentar a eficácia e reduzir custos.
5. Otimização de custos: garante que os recursos sejam usados de maneira econômica e que os custos sejam gerenciados com eficácia.
6. Arquitetura: garante que a arquitetura da solução seja escalável, flexível, e atenda às necessidades de negócios e de usuários.

Cada pilar contém um conjunto de práticas recomendadas e orientações para ajudar os usuários a criar e manter soluções na nuvem bem arquitetadas. O AWS Well-Architected pode ser usado como um guia para avaliar arquiteturas existentes ou para projetar novas soluções na nuvem.

| Pilar | Descrição |
| --- | --- |
| Excelência operacional | Foco em executar e monitorar sistemas para entregar valor ao negócio e aos clientes com eficiência e rapidez. Inclui a utilização de automação, melhoria contínua e práticas de gerenciamento de incidentes |
| Segurança | Foco em proteger informações e sistemas. Inclui o uso de controles de segurança, práticas de gerenciamento de identidade e acesso, criptografia e auditorias regulares |
| Confiabilidade | Foco em garantir que sistemas e aplicativos funcionem de maneira confiável e com capacidade de recuperação em caso de falhas. Inclui a utilização de tolerância a falhas, backup e recuperação de desastres |
| Eficiência de desempenho | Foco em utilizar recursos de forma eficiente para atender aos requisitos de desempenho e capacidade do sistema. Inclui a utilização de monitoramento e otimização de recursos, escalabilidade e uso de tecnologias adequadas |
| Otimização de custos | Foco em otimizar o uso de recursos e minimizar custos. Inclui o uso de monitoramento de custos, planejamento de capacidade e seleção de serviços e recursos adequados para o negócio |
| Arquitetura | Foco em criar sistemas flexíveis, escaláveis, seguros e eficientes. Inclui a utilização de padrões arquiteturais adequados, design modular, integração e desacoplamento de componentes e gerenciamento de mudanças |

### Highly Avaliby
AWS Highly Available (ou alta disponibilidade, em português) é um conjunto de práticas e soluções oferecidas pela Amazon Web Services (AWS) para garantir a continuidade dos serviços hospedados na plataforma, mesmo em situações de falhas ou interrupções.

A alta disponibilidade é alcançada por meio da redundância de recursos, replicação de dados e failover automático em caso de problemas. Isso significa que, se um servidor ou componente falhar, outro assume imediatamente, evitando qualquer interrupção ou perda de dados.

A AWS oferece uma ampla variedade de serviços que podem ser utilizados para construir uma infraestrutura altamente disponível, incluindo balanceadores de carga, grupos de autoescalonamento, banco de dados em várias zonas de disponibilidade, replicação de armazenamento, além de ferramentas de monitoramento e recuperação automatizada.

Ao garantir a alta disponibilidade em uma arquitetura de nuvem, as empresas podem oferecer aos seus usuários um serviço mais confiável, reduzir a possibilidade de perda de receita e manter a reputação da marca.

### Design for Failure
AWS Design for Failure é uma prática de design arquitetural na AWS que consiste em projetar e implementar sistemas que possam lidar com falhas de componentes individuais, permitindo que o sistema como um todo continue funcionando sem interrupções. Essa abordagem é baseada no conceito de que as falhas são inevitáveis e que é melhor se preparar para elas do que tentar evitá-las completamente.

Para implementar o AWS Design for Failure, os desenvolvedores da AWS usam técnicas como redundância, balanceamento de carga, monitoramento de desempenho e implementação de serviços em várias regiões geográficas. Com essas práticas, o sistema pode continuar operando mesmo que um ou mais componentes falhem.

A implementação do AWS Design for Failure é importante para garantir alta disponibilidade, escalabilidade e resiliência para aplicações na nuvem da AWS. Com essa abordagem, é possível garantir que o sistema continue operando mesmo em situações adversas, o que reduz o tempo de inatividade, melhora a experiência do usuário e ajuda a evitar perda de negócios.

### Embre Elasticy and Automation
AWS Elasticity and Automation é uma solução que permite gerenciar de forma eficiente e dinâmica a escalabilidade e a automação de recursos na nuvem da AWS. O objetivo do AWS Elasticity é ajustar automaticamente a capacidade dos recursos, como instâncias do EC2, de acordo com a demanda, garantindo que a infraestrutura esteja sempre disponível e com o desempenho esperado. Já o AWS Automation fornece recursos para automatizar tarefas de gerenciamento e manutenção de recursos na nuvem, como backups, atualizações e monitoramento de logs, por exemplo.

Essas soluções da AWS são ideais para empresas que precisam lidar com grandes volumes de tráfego ou processamento de dados, garantindo que a infraestrutura esteja sempre preparada para atender às demandas do negócio. Além disso, a automação de tarefas repetitivas ajuda a reduzir erros e aumentar a eficiência da equipe de TI. Em resumo, a AWS Elasticity and Automation é uma solução poderosa para aumentar a disponibilidade, escalabilidade e eficiência dos recursos na nuvem da AWS.

### Loosely Couple Components
AWS Loosely Coupled Components é um conceito utilizado na arquitetura de soluções em nuvem da AWS, que se refere à construção de sistemas compostos por componentes independentes e que possam operar de forma autônoma, sem depender uns dos outros.

Na prática, isso significa que os componentes de uma solução em nuvem são desenvolvidos e implantados separadamente, sem que haja um forte acoplamento entre eles. Cada componente é responsável por uma função específica e pode ser executado de forma independente, sem afetar o funcionamento dos outros componentes.

Esse modelo de arquitetura traz diversas vantagens, como maior flexibilidade, escalabilidade e resiliência, uma vez que é possível adicionar ou remover componentes conforme a necessidade, sem afetar o restante da solução. Além disso, o uso de componentes independentes facilita a manutenção e a atualização dos sistemas, tornando-os mais eficientes e econômicos.

Em resumo, a utilização de AWS Loosely Coupled Components é uma estratégia importante para criar soluções mais flexíveis, escaláveis e resistentes na nuvem.

| [Anterior: Banco de Dados](./5_Bando_de_Dados.md) | [Proximo: Integração e Seguraça](./7_Integracao_e_Seguranca.md) |
|:--------------------------------|----------------------------------------------------------------:|