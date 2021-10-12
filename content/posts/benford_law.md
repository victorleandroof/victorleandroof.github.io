---
title: "A beleza dos padrões numéricos"
date: 2021-10-12T08:40:12-03:00
draft: false
tags: [matemática, lei_benford, benford, padrões, numéricos]
featuredImage: "/images/benford_law.jpg"
featuredImagePreview: "/images/benford_law.jpg"
images: [/images/benford_law.jpg]
seo:
    images: [/images/benford_law.jpg]
---

Será que mundo dos números como dados financeiros, votos, bits em images, amigos em comum em redes sócias tem algum padrão ?


# A magica da lei de benford

Imagine que você tem um monte de números aleatórios, qualquer número entre 1 e 999.999, escolha um número aleatoriamente. Qual é o primeiro digito desse numero se for um ao acaso ele pode ser 2, 4 e 7 ninguém sabe provavelmente a probabilidade é igual, porém não é bem assim, a lei de benford diz que a frequência do numero 1 sempre será de 30,1% , 2 será de 17,6%, 3 será 12,5%, 4 será 9,7%, conforme o exemplo abaixo:

![Exemplo da lei de benford](/images/benford_example.png)

O gráfico possui uma curva de forma logarítmica denominada de curva de benford. Um pouco difícil acreditar nessa loucura de frequência numérica ou ate mesmo pouco improvável de acontecer. Mark Nigrini em  2001 utilizando da lei de benford trouxe a atona uma das maiores fraudes, a empresa Enron estava usando lacunas contábeis para esconder bilhões de dólares de dívidas incobráveis ​​ao mesmo tempo em que inflacionava os ganhos da empresa. Caso tenha interesse compreender como foi aplicado a lei nos dados da empresa segue repositório [click aqui](https://github.com/mauriciomani/ENRON-Benford-s-law). 

# lei de benford aplicada aos dados do SICONV

Utilizando a lei de benford criei uma analise baseado nos dados SICONV ( sistema utilizado para captação de recursos para os Municípios e Entidades do Brasil) selecionei dois deputados sendo eles Jean Wyllys e Eduardo Bolsonaro
em ambos casos a lei de benford foi violada. Porém não podemos afirmar se realmente se ambos estão ou estavam  cometendo um ato de corrupção teria que ter uma analise mais afundo.

![Benford aplicado aos valores do deputado Jean Wyllys](/images/benford_jean_wyllys.png)


![Benford aplicado aos valores do deputado Eduardo Bolsonaro](/images/benford_eduardo_bolsonaro.png)

A Lei de Benford pode reconhecer as probabilidades de frequências altamente prováveis ou altamente improváveis de números em um conjunto de dados, se pararmos para refletir é incrível que uma lei possa encontrar uma ordem matemática mesmo com todo os a casos, e aleatoriedade e confusão da nossas vidas. 

fontes: 

[Election forensics: the second-digit Benford's law test and recent American presidential elections](https://www.researchgate.net/publication/228386443_Election_forensics_the_second-digit_Benford's_law_test_and_recent_American_presidential_elections)

[A Confiabilidade dos Dados Financeiros de Hospitais Filantrópicos Canadenses: Um Estudo Empírico Baseado na Lei de Benford](https://revistas.ufrj.br/index.php/scg/article/download/13290/9112)

[Benford’s Law Applies to Online Social Networks](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0135169)






