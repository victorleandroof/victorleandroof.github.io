---
title: "Quarkus vs. Spring Boot: A Batalha dos Frameworks Java "
date: 2023-08-06T13:47:07-03:00
draft: false
tags: [quarkus, springboot, java, frameworks]
featuredImage: "/images/springboot_vs_quarkus/capa.png"
featuredImagePreview: "/images/springboot_vs_quarkus/capa.png"
images: [/images/springboot_vs_quarkus/capa.png]
seo:
    images: [/images/springboot_vs_quarkus/capa.png]
---

Se você é um desenvolvedor Java em busca do framework perfeito para dar vida ao seu projeto, este artigo é feito sob medida para você! Neste guia, exploraremos as principais diferenças entre Quarkus e Spring Boot, os dois gigantes do desenvolvimento Java, mostrarei insights valiosos para ajudá-lo a tomar a decisão mais acertada. 

## O que é Spring Boot ?

O Spring Boot é uma ferramenta que simplifica o desenvolvimento de aplicativos Java, fornecendo uma configuração automática baseada em convenções. Ele reduz a quantidade de código de configuração manual, permitindo que os desenvolvedores se concentrem mais na lógica de negócios. Através do ecossistema Spring, o Spring Boot oferece recursos poderosos para criar aplicações corporativas de forma eficiente.

### Pontos Positivos:

1. Facilidade de Configuração: O Spring Boot facilita a configuração ao adotar uma abordagem de convenção sobre configuração. Isso significa que muitas configurações são definidas automaticamente com base nas dependências utilizadas, simplificando o processo de configuração e acelerando o desenvolvimento.
2. Integrações Prontas: O Spring Boot oferece uma ampla variedade de integrações prontas para uso. Isso possibilita que os desenvolvedores adicionem facilmente funcionalidades específicas às suas aplicações, como acesso a bancos de dados, autenticação, segurança e muito mais.
3. Ecossistema Spring: O Spring Boot é construído sobre o ecossistema Spring, famoso e consolidado no desenvolvimento Java. Isso proporciona aos desenvolvedores uma vasta gama de recursos, documentação e uma comunidade ativa para suporte.
4. Agilidade no Desenvolvimento: Com o Spring Boot, o desenvolvimento se torna mais ágil. Com recursos prontos para uso e menos configuração manual, os desenvolvedores podem se concentrar na lógica de negócio, aumentando a produtividade.

### Pontos Negativos:

1. Curva de Aprendizado: A curva de aprendizado do Spring Boot pode ser desafiadora para desenvolvedores iniciantes, pois é necessário ter familiaridade com o ecossistema Spring e seus conceitos relacionados. No entanto, o Spring Boot facilita muitas tarefas e oferece um grande potencial uma vez que se domina esses conhecimentos.
2. Overhead de Dependências: O Spring Boot, sendo uma ferramenta abrangente e flexível, pode apresentar overhead devido às múltiplas dependências incluídas. Isso pode afetar o tamanho da aplicação e o tempo de inicialização, dependendo do projeto.
3. Flexibilidade Limitada: Em certas ocasiões, a abordagem pré-configurada do Spring Boot pode restringir a flexibilidade de configuração. Caso o projeto possua requisitos muito específicos, pode ser necessário contornar as convenções do Spring Boot.
4. Necessidade de Atualizações: O ecossistema Spring é atualizado regularmente para manter sua relevância e segurança. Portanto, os desenvolvedores devem estar preparados para acompanhar as atualizações do framework e suas dependências, a fim de garantir a estabilidade e segurança do projeto.

## O que é Quarkus ?

O Quarkus é uma estrutura que segue uma abordagem semelhante ao Spring Boot, mas se destaca por oferecer artefatos menores e um tempo de inicialização extremamente rápido, além de ser eficiente em termos de recursos. É otimizado para ambientes em nuvem, serverless e em containers, proporcionando agilidade e desempenho no desenvolvimento Java. Além disso, integra-se perfeitamente com os frameworks Java mais populares, tornando a experiência de desenvolvimento suave e familiar para os desenvolvedores. Sua versatilidade é uma escolha atraente para projetos de todos os tamanhos, desde pequenas aplicações até sistemas corporativos complexos.

### Pontos Positivos:

1. Tempo de inicialização rápido: O Quarkus proporciona uma inicialização extremamente rápida, ideal para aplicações em nuvem e microsserviços, permitindo escalabilidade eficiente.
2. Eficiência de recursos: O Quarkus, com sua abordagem otimizada, consome menos recursos em comparação com outros frameworks, resultando em menor uso de memória e tempos de resposta mais ágeis.
3. Tamanho reduzido de artefatos: O Quarkus produz artefatos menores, tornando as aplicações mais leves e facilitando a implantação e distribuição.
4. Suporte a nativo: O Quarkus oferece suporte à compilação nativa, permitindo a criação de binários nativos que reduzem o tempo de inicialização e o tamanho dos artefatos de forma significativa.
5. Integração com o ecossistema Java: O Quarkus é compatível com os frameworks e bibliotecas Java mais populares, o que facilita a integração com as ferramentas e tecnologias já utilizadas pelos desenvolvedores.

### Pontos Negativos:

1. Curva de aprendizado: O Quarkus, como uma tecnologia nova, pode demandar algum tempo para se familiarizar com seus conceitos e características únicas.
2. Limitações em projetos complexos: Em projetos altamente complexos ou com requisitos muito específicos, o Quarkus pode apresentar algumas limitações em comparação a frameworks mais consolidados e experientes.
3. Compatibilidade com algumas bibliotecas: O Quarkus é compatível com a maioria das bibliotecas Java, porém algumas podem não ser totalmente suportadas, requerendo ajustes ou adaptações.
4. Ciclo de vida do ecossistema: O ecossistema do Quarkus, uma tecnologia emergente, está em constante evolução, o que pode causar mudanças frequentes que impactam a estabilidade das aplicações.
5. Documentação em desenvolvimento: A documentação do Quarkus está em constante evolução, porém, em alguns casos, pode faltar recursos detalhados para lidar com cenários complexos ou específicos.

## Comparação

Criei duas APIs usando o framework Spring e Quarkus, as quais estão sendo executadas em containers Docker. Para analisar o consumo de memória, CPU e tempo de resposta, utilizei uma combinação de ferramentas como K6, Prometheus e Grafana.

Dessa forma, será possível observar visualmente a diferença de consumo de memória, utilização da CPU e tempo de resposta entre as duas abordagens, demonstrando de forma clara o ganho real de desempenho.

### Ferramentas

![Ferramentas](/images/springboot_vs_quarkus/ferramentas.png)

### Tempo de Resposta

![Tempo de Resposta](/images/springboot_vs_quarkus/tempo-resposta.png)

### Uso de CPU

![Uso de CPU](/images/springboot_vs_quarkus/uso-de-cpu.png)

### Uso de Memoria

![Uso de Memoria](/images/springboot_vs_quarkus/uso-de-memoria.png)

## Github Links

[Docker com prometheus e grafana](https://github.com/Einsteinish/Docker-Compose-Prometheus-and-Grafana)

[Projeto](https://github.com/victorleandroof/article-spring-vs-quarkus)