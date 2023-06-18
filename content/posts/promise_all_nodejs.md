---
title: "Desvendando o 'Promise.all': Faça Seu Código Node.js Voar Alto e Rápido"
date: 2023-06-18T14:01:34-03:00
draft: false
tags: [nodejs, promises, perfomance, boas_praticas_nodejs, promise.all]
featuredImage: "/images/nodejs_promises.png"
featuredImagePreview: "/images/nodejs_promises.png"
images: [/images/nodejs_promises.png]
seo:
    images: [/images/nodejs_promises.png]
---

Quantas vezes você precisou lidar com múltiplas Promises dentro de um mesmo fluxo, onde nenhuma dependia da outra? E quantas vezes você acabou ignorando ou esquecendo o método estático Promise.all? Neste artigo, vamos explorar a importância dele e garantir que você nunca mais se esqueça de utilizá-lo ou ignorar. Prepare-se para descobrir como esse recurso pode revolucionar a forma como você lida com assincronicidade no seu código Node.js!

## O que é Promises ?

O conceito de Promises foi inicialmente proposto por Daniel P. Friedman, David Wise e Peter Hibbard em 1976. No entanto, foi somente em 2007, com a introdução da biblioteca MochiKit, seguida por Dojo e jQuery, que as Promises fizeram sua primeira aparição no JavaScript. Mais tarde, o time da CommonJS desenvolveu o padrão Promises/A+.

O objetivo fundamental desse conceito é permitir que o código não interrompa o que estamos fazendo. Para ilustrar vamos analisar o seguinte exemplo: imagine que você precise ler quatro arquivos independentes e para cada arquivo lido, você precisa executar uma ação específica. Se você usasse a função **`readFileSync`**, o tempo de execução seria somado, levando em consideração que cada leitura leva cerca de dois segundos. Isso significa que, ao final, você teria um tempo total de oito segundos, pois os arquivos seriam lidos um após o outro. E ai que entra conceito de promises vocês pode fazer leitura de forma assíncrona, conforme o imagem abaixo:

![Exemplo do resultado sync e async](/images/nodejs-sync-vs-async.png)

## Onde entra o Promise.all ?

Agora que temos uma melhor clareza no básico do conceito de Promises, vamos considerar o seguinte cenário utilizando **`async/await`**: imagine que temos uma aplicação que realiza duas chamadas de API, uma para buscar usuários (**`users`**) e outra para buscar grupos (**`groups`**). No final, precisamos mesclar os grupos em que os usuários estão. Suponha que a chamada para buscar usuários leva, em média, 2 segundos para responder, enquanto a chamada para buscar grupos leva cerca de 3 segundos. O processo de mesclagem das duas APIs leva 1 segundo adicional. Ao utilizar **`async/await`**, o tempo total de processamento seria de 6 segundos, uma vez que teríamos que esperar cada Promise ser resolvida sequencialmente.

Agora, vamos imaginar a possibilidade de executar as chamadas para grupos e usuários em paralelo e em seguida receber os resultados de ambas para realizar a mesclagem. Se pudéssemos fazer isso, teríamos um tempo total de processamento de apenas 4 segundos. Essa redução ocorreria porque as duas chamadas de API seriam executadas simultaneamente, aproveitando o tempo máximo de resposta (nesse caso, 3 segundos) e em seguida, o processo de mesclagem seria executado em 1 segundo adicional. Parece mágico, não é? Na verdade, é apenas o **`Promise.all`** em ação, um recurso disponível tanto nos navegadores quanto no Node.js. No entanto, muitos desenvolvedores acabam se esquecendo de utilizá-lo, perdendo a oportunidade de melhorar significativamente a eficiência do seu código.

## Promise.all vs Async/Await

Caso ainda haja dúvidas sobre o ganho de desempenho, criei duas APIs usando o framework Express, as quais estão sendo executadas em containers Docker. Para analisar o consumo de memória, CPU e tempo de resposta, utilizei uma combinação de ferramentas como K6, tshield, Prometheus e Grafana.

Dessa forma, será possível observar visualmente a diferença de consumo de memória, utilização da CPU e tempo de resposta entre as duas abordagens, demonstrando de forma clara o ganho real de desempenho obtido ao utilizar o **`Promise.all`**.

### Ferramentas

![Ferramentas em execução](/images/promise-all-01.png)

### Tempo de Resposta

![Tempo de Resposta](/images/promise-all-02.png)

### Uso de CPU

![Use de CPU](/images/promise-all-03.png)

### Uso de Memoria

![Uso de Memoria](/images/promise-all-04.png)

## Github Links

[Docker com prometheus e grafana](https://github.com/Einsteinish/Docker-Compose-Prometheus-and-Grafana)

[Tshield](https://github.com/diegorubin/tshield)

[Projeto](https://github.com/victorleandroof/article-promise-all)


