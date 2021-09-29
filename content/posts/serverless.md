---
title: "Você sabe o que é Arquitetura Serverless?"
date: 2021-09-28T20:39:07-03:00
draft: false
tags: [serverless, bass, faas, containers]
featuredImage: "/images/arquitetura_serverless.jpg"
featuredImagePreview: "/images/arquitetura_serverless.jpg"
images: [/images/arquitetura_serverless.jpg]
seo:
    images: [/images/arquitetura_serverless.jpg]
---

Mike Roberts define o termo “sem servidor” como confuso, pois com esses aplicativos há tanto processos de servidor quanto hardware em execução, mas a diferença em relação às abordagens normais é que a organização que cria e suporta um aplicativo “sem servidor” não cuida desse hardware ou dos processos . Eles estão terceirizando essa responsabilidade para outra pessoa.

# Backend as a Service (BaaS)
Com cloud estabilizado o controle sobre as virtuais machines foi deixado lado dando inicio a era BaaS, ele é um serviço de computação em nuvem que serve como middleware. O mesmo fornece aos desenvolvedores uma forma para conectar suas aplicações mobile e web a serviços na nuvem a partir de APIs e SDKs. Um exemplo de BaaS e o firebase.

# Function as a Service (FaaS)
A FaaS é muito recente foi disponibilizado inicialmente pela Hook.io em 2014 e seguido por grandes players: Amazon AWS Lambda, Google Cloud Functions, MS Azure Functions, IBM / Apache OpenWhisk e recentemente até Oracle Cloud Fn.
Usando FaaS, seu código é executado em resposta a eventos definidos por você. Porém, os recursos computacionais você não administra ou controla. Deve-se focar na construção de aplicações que respondam mais rápido às mudanças e às novas informações.

# BaaS e FaaS — Vantagens — ( Martin fowler )
Custo de estabilidades reduzidos (paga somente por tempo de execução é memória alocado alocada para função ou quantidade de operações e armazenamento)
Custo operacionais reduzidos ou gratuitos
Custo desenvolvimento reduzidos

# BaaS e FaaS — Desvantagens — ( Martin fowler )
Lock-in de provedores Clouds ( Pode ser resolvido através framework open source como Serverless Framework)
Repetição de lógica na camada cliente (Somente na BaaS)
Sempre stateless

# Diferença entre Serveless e Containers ?
Containers ainda são “pesados” operacionalmente se comparados com Serverless. Você precisa de soluções de gestão como Kubernetes ou Docker Swarm. Porém Containers são mais portáveis.