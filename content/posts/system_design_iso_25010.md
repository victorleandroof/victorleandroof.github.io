---
title: "System_desing_iso_25010"
date: 2025-10-24T17:00:33-03:00
tags: [System Desing, ISO 25010, Arquitetura]
featuredImage: "/images/system_design_iso_25010.png"
featuredImagePreview: "/images/system_design_iso_25010.png"
images: [/images/system_design_iso_25010.png]
seo:
    images: [/images/system_design_iso_25010.png]
draft: false
---

# System Design Interview: Tomada de Decisão Baseada Dados com ISO 25010

Como arquiteto, a elaboração e decisões arquiteturais precisa de uma abordagem que combine análise de dados, considerações de custo, frameworks e padrões fortemente estabelecidos. Este artigo apresenta uma metodologia integrada para system design interviews que utiliza dados como fundamento para decisões, incorpora análise de custos desde o início do processo e aplica o padrão ISO 25010 para garantir qualidade.

## A Nova Era das Decisões Arquiteturais

Grande entidades não podem basear as suas decisões arquiteturais em intuição, gosto pessoais ou sorte. O paradigma atual exige uma abordagem **data-driven** que utiliza métricas quantificáveis, análises de performance e uma norma institucional de qualidade como o ISO 25010.

Extremamente necessário trata os dados como **coração** no processo de tomada de decisão. Isso significa que cada decisão arquitetural deve ser baseada em métricas concretas, análises de performance histórica e projeções baseadas em dados reais.

Os princípios fundamentais incluem:

1. **Decisões baseadas em métricas**: Toda decisão arquitetural suportada por dados concretos
2. **Processamento em tempo real**: Capacidade de adaptar a arquitetura baseada em feedback imediato
3. **Integração de AI/ML**: Componentes de machine learning para insights mais profundos
4. **Abordagem orientada a eventos**: Comunicação entre componentes através de eventos

## ISO 25010: Norma Institucional de Qualidade

O ISO 25010 define oito pilares principais de qualidade:

| **Característica** | **Descrição** | **Aplicação em System Design** |
| --- | --- | --- |
| **Adequação Funcional** | Atendimento aos requisitos funcionais | Validação de features e casos de uso |
| **Confiabilidade** | Manutenção do nível de performance | Estratégias de fault tolerance |
| **Usabilidade** | Facilidade de uso e aprendizado | Design de APIs e interfaces |
| **Eficiência de Performance** | Otimização de recursos | Decisões de scaling e caching |
| **Manutenibilidade** | Facilidade de modificação | Arquitetura de microserviços |
| **Portabilidade** | Transferência entre ambientes | Estratégias de containerização |
| **Compatibilidade** | Interoperabilidade com outros sistemas | Design de APIs e protocolos |
| **Segurança** | Proteção contra acessos não autorizados | Implementação de autenticação/autorização |

Durante uma entrevista de system design, devemos utilizar esses pilares estruturado para avaliar e justificar decisões , garantindo que todos os aspectos de qualidade sejam considerados.

## Fator de Preço nas Decisões Arquiteturais

### Risk and Cost Driven Architecture (RCDA)

Não podemos esquecer preço ha ser pago por essa arquitetura, ou seja, importante para não esquecer e a abordagem RCDA define que a significância arquitetural de uma preocupação pode ser representada pela fórmula:

**AS(C) = Cost(C) + Risk(C)**

Onde:

- **AS(C)** = Significância Arquitetural da preocupação C
- **Cost(C)** = Custo estimado para endereçar a preocupação
- **Risk(C)** = Custo total esperado de "problemas potenciais"

## Colocando em Pratica: Sistema de E-commerce Escalável

Para ajudar compreender os tópicos desse artigo iriamos colocar em pratica um sistema de e-commerce :

**Requisitos:**

- 1M+ usuários durante picos
- 10M+ produtos no catálogo
- 99.9% de disponibilidade
- Processamento de 50K pedidos/hora

## Análise de Requisitos com ISO 25010

| **Característica ISO 25010** | **Requisito Específico** | **Métrica Objetivo** | **Impacto no Custo** |
| --- | --- | --- | --- |
| **Performance** | Latência de resposta | < 200ms (p95) | Cache: $120/mês |
| **Confiabilidade** | Disponibilidade | 99.9% uptime | Multi-AZ: +40% custo |
| **Escalabilidade** | Usuários concorrentes | 1M+ usuários | Auto-scaling: $650/mês |
| **Segurança** | Proteção de dados | Compliance LGPD | WAF + encrypt: $80/mês |
| **Manutenibilidade** | Deploy time | < 30min deploy | CI/CD: $100/mês |

## Arquitetura de Microserviços

**Decisão Data-Driven para Microserviços**:

Com base em análise de coupling e coesão dos domínios de negócio:

1. **Product Service**: $150/mês (alta demanda de CPU para buscas)
2. **User Service**: $80/mês (operações CRUD simples)
3. **Cart Service**: $120/mês (cache intensivo)
4. **Payment Service**: $200/mês (alta segurança, redundância)
5. **Order Service**: $100/mês (processamento assíncrono)

**Total infraestrutura base**: $650/mês

## Estratégia de Dados Híbrida

**Análise Cost-Benefit por Tipo de Dados**:

1. **PostgreSQL (RDS Multi-AZ)** - Dados transacionais
    - Custo: $180/mês
    - Justificativa: ACID compliance, backup automático
    - ISO 25010: Alta confiabilidade e integridade
2. **Redis Cluster** - Cache distribuído
    - Custo: $120/mês
    - Justificativa: Sub-ms latency, reduz 70% load no DB
    - ISO 25010: Performance otimizada
3. **DynamoDB** - Sessões de usuário
    - Custo: $50/mês (pay-per-use)
    - Justificativa: Auto-scaling, global tables
    - ISO 25010: Alta disponibilidade

## Implementação de Monitoramento Data-Driven

**Métricas de Negócio Coletadas**:

- Taxa de conversão por página de produto
- Valor médio do pedido por categoria
- Tempo médio de sessão por usuário
- Taxa de abandono do carrinho por etapa

**Métricas Técnicas (Alinhadas ao ISO 25010)**:

- Latência por endpoint (p50, p95, p99)
- Utilização de CPU/Memória por serviço
- Taxa de erro por API
- Throughput de transações por segundo

## Decisões Arquiteturais Baseadas em Dados

## Sharding Strategy

**Análise de Performance vs Custo**:

- **Crescimento projetado**: 100TB em 2 anos
- **Opção single DB**: $2,400/mês (RDS XL)
- **Opção sharded**: $800/mês (3x RDS Medium)
- **Decisão**: Sharding por categoria de produto baseado em análise de queries

## Cache Strategy

**Dados coletados durante 30 dias**:

- 80% das consultas são para os mesmos 20% de produtos
- Cache hit rate atual: 65%
- Custo de cache miss: +150ms latência média

**Implementação**:

- Cache L1 (local): Hot products (TTL 1 min)
- Cache L2 (Redis): Warm products (TTL 5 min)
- **ROI calculado**: 40% redução latência, 25% redução custos DB

## Resultados Mensuráveis (ISO 25010)

## Performance

- **Baseline**: Latência p95 = 800ms
- **Pós-otimização**: Latência p95 = 180ms
- **Impacto financeiro**: 15% aumento conversão = +$50K/mês de revenue

## Manutenibilidade

- **Deploy time**: 2h → 15min (-92%)
- **MTTR**: 45min → 8min (-82%)
- **Developer productivity**: +30% features/sprint

## Confiabilidade

- **Uptime alcançado**: 99.95% (target: 99.9%)
- **Error rate**: 0.01% (target: 0.1%)
- **Customer satisfaction**: +25% NPS improvement

## Estratégias de Otimização Contínua

## Feedback Loop Automatizado

1. **Coleta automática** de métricas performance/custo via observabilidade
2. **Análise semanal** de tendências e detecção de anomalias
3. **Decisões arquiteturais** baseadas em dados históricos e projeções
4. **A/B testing** para validação de mudanças antes do rollout
5. **Refinamento contínuo** dos modelos de ML para previsão

## Auto-Scaling Inteligente

Implementação baseada em múltiplas dimensões:

- **Métricas de negócio**: Pedidos/minuto, usuários ativos
- **Métricas técnicas**: CPU, memória, latência, queue depth
- **Projeções de custo**: Budget limits por serviço
- **Machine learning**: Predição de picos baseada em histórico e sazonalidade

## Framework de Entrevista: Aplicação Prática

## Estrutura Sugerida

1. **Clarificação de requisitos** (5 min)
    - Aplicar lens do ISO 25010 para requisitos não-funcionais
    - Estabelecer constraints de custo e performance
2. **Estimativa de capacidade** (10 min)
    - Cálculos data-driven: QPS, storage, bandwidth
    - Projeções de crescimento baseadas em dados
3. **Design high-level** (15 min)
    - Justificar decisões com análise custo-benefício
    - Mapear componentes às características do ISO 25010
4. **Deep dive** (10 min)
    - Detalhar componente crítico com métricas
    - Apresentar trade-offs com dados concretos
5. **Scaling e otimização** (5 min)
    - Estratégias baseadas em monitoring e feedback

Para o componente de cache, escolhemos Redis Cluster porque nossa análise de 30 dias mostra que 80% das queries são para 20% dos produtos. Com TTL de 1 minuto, projetamos 90% hit rate, resultando em latência p95 de 50ms vs 200ms sem cache. O custo de $120/mês se paga com a redução de 60% na carga do banco principal, além de melhorar nossa métrica de Performance do ISO 25010.

![system_design_ex1.png](/images/system_design_ex1.png)

## Conclusão

Esta abordagem integrada de system design, junto com análise data-driven, consciência de custos e o ISO 25010, representa a evolução das práticas arquiteturais modernas. Ao fundamentar decisões em dados concretos e métricas de qualidade estabelecidas, os arquitetos podem criar sistemas verdadeiramente escaláveis, sustentáveis e alinhados aos objetivos de negócio.