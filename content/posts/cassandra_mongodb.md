---
title: "Cassandra_mongodb"
date: 2021-09-28T22:00:18-03:00
draft: false
tags: [mongodb, cassandra, nosql]
featuredImage: "/images/cassandra_mongodb.jpg"
featuredImagePreview: "/images/cassandra_mongodb.jpg"
images: [/images/cassandra_mongodb.jpg]
seo:
    images: [/images/cassandra_mongodb.jpg]
---


Cassandra e MongoDB são bancos de dados “NoSQL”, mas na verdade são completamente diferentes. Eles têm qualidades e ofertas completamente diferentes. Que tal começarmos com o início dos pré-requisitos … Nenhum desses bancos de dados substitui o RDBMS nem os bancos de dados “ACID”.Portanto, se você tiver uma carga de trabalho baseada em valor em que a padronização e a consistência sejam as necessidades essenciais, nenhum desses bancos de dados funcionará para você. Você está em uma situação ideal ficando com bancos de dados sociais convencionais como MySQL, PostgreSQL, Oracle e assim por diante. Uma vez que temos bases de dados sociais fora do caminho comum, que tal considerarmos os contrastes reais entre o Cassandra e o MongoDB que permitirão que você escolha um deles.

# 1. Modelo de Objeto Expressivo

O MongoDB reforça um modelo de objetos rico e expressivo. Objetos podem ter propriedades e objetos podem ser resolvidos uns nos outros (para vários níveis). Este modelo é excepcionalmente “situado em um objeto” e pode, sem muito esforço, falar com qualquer estrutura de objeto em seu espaço. Você também pode arquivar a propriedade de qualquer objeto em qualquer nível da progressão — isso é surpreendentemente eficaz! Cassandra, então, novamente, oferece uma estrutura de tabela genuinamente costumeira com linhas e segmentos. A informação é mais organizada e cada segmento tem um tipo específico que pode ser indicado em meio à criação.
Decisão: Se a sua área de interesse precisa de um modelo rico de informações, o MongoDB é um ajuste superior para você.

# 2. Índices Secundários

Índices secundários são um dos melhores da linha no MongoDB. Isso simplifica o registro de qualquer propriedade de um objeto guardada no MongoDB, independentemente de estar resolvida. Isso torna extremamente simples a consulta em vista desses índices secundários. Cassandra tem apenas ajuda rápida para índices secundários. Índices secundários também são restritos a segmentos únicos e correlações de correspondência. No caso em que você está em sua maior parte indo para a consulta pela chave essencial, então Cassandra funcionará admiravelmente para você.
Decisão: Se a sua aplicação precisar de índices secundários e precisar de adaptabilidade no modelo de consulta, o MongoDB é um ajuste superior para você.

# 3. Alta Disponibilidade

O MongoDB sustenta um modelo “único mestre”. Isso implica que você tenha um nó mestre e vários nós escravos. Na chance de que o mestre caia, um dos escravos é escolhido como mestre. Este procedimento acontece naturalmente ainda requer investimento, como regra 10–40 segundos. Em meio a esta temporada de nova decisão pioneira, o seu conjunto de reprodução está desativado e não pode ser composto. Isso funciona para a maioria das aplicações no final do dia depende de suas necessidades. Cassandra reforça um modelo “múltiplo mestre”. A passagem de um único nó não influencia a capacidade do grupo, assim você pode obter 100% de tempo de atividade para composições.
Decisão: Se você precisar de 100% de tempo de atividade, Cassandra é um ajuste superior para você.

# 4. Escalabilidade
O MongoDB com seu modelo de “mestre único” pode compor apenas o essencial. Os servidores secundários devem ser utilizados para leitura. Então, basicamente, na chance de que você tenha três conjuntos de reprodução de nó, apenas o mestre está fazendo composições e os outros dois nós são utilizados para leitura. Isto constrange extraordinariamente compõe adaptabilidade. Você pode transmitir vários fragmentos, mas basicamente apenas 1/3 dos seus nós de informação podem fazer composições. Cassandra com seu modelo “multiple master” pode fazer composições em qualquer servidor. Basicamente, sua capacidade de composição é limitada pela quantidade de servidores que você tem no grupo. Quanto mais servidores você tiver no grupo, melhor será dimensionado.
Decisão: Se escalabilidade é seu objetivo, Cassandra é um ajuste superior para você.
