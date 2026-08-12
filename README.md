# Frontend Interview Questions

Banco de perguntas técnicas e conceituais de Front-end encontradas em processos seletivos, com respostas e breves explicações.

O objetivo deste repositório é servir como **material de consulta e estudo**, ajudando profissionais de Front-end a se prepararem para entrevistas técnicas e processos seletivos.

> **Nota:** algumas questões de processos seletivos são propositalmente simplificadas. As respostas aqui representam a alternativa mais adequada dentro do contexto apresentado pela questão, mas determinados temas podem ter abordagens diferentes em projetos reais.

---

## Índice

* [Consumo de APIs REST](#consumo-de-apis-rest)
* [CSS moderno](#css-moderno)
* [Acessibilidade](#acessibilidade)
* [Redux](#redux)
* [Experiência centrada no usuário](#experiência-centrada-no-usuário)
* [Estados assíncronos no React](#estados-assíncronos-no-react)
* [Design System](#design-system)
* [Arquitetura Front-end](#arquitetura-front-end)
* [Micro Frontends](#micro-frontends)
* [Observabilidade e qualidade](#observabilidade-e-qualidade)
* [Sistemas legados](#sistemas-legados)
* [Componentes reutilizáveis](#componentes-reutilizáveis)

---

## Consumo de APIs REST

### Qual é a sequência correta para consumir uma API REST em uma aplicação frontend?

* [x] Fazer a chamada à API
* [x] Tratar a resposta recebida
* [x] Atualizar o estado da aplicação com os dados
* [ ] Ignorar erros de resposta
* [ ] Exibir os dados diretamente sem formatação

**Resposta:** Fazer a chamada → tratar a resposta → atualizar o estado.

Em uma aplicação real, também é importante tratar estados de loading, erro e dados vazios, além de adaptar ou normalizar os dados antes de apresentá-los na interface.

---

## CSS moderno

### Qual das seguintes opções é considerada uma boa prática de estilização usando CSS moderno?

* [x] Utilizar SASS ou LESS para modularização
* [ ] Criar estilos inline para cada elemento
* [x] Definir tokens e temas para consistência
* [ ] Escrever CSS sem organização
* [x] Reutilizar classes de forma coerente ao longo do projeto

**Resposta:** SASS/LESS, tokens e temas e reutilização coerente de estilos.

> Observação: atualmente, CSS Modules, CSS-in-JS e recursos nativos de CSS também podem ser utilizados para modularização. A escolha depende da arquitetura e das necessidades do projeto.

---

## Acessibilidade

### Como você abordaria a inclusão de princípios de acessibilidade em sua aplicação?

* [x] Usar ARIA para melhorar a navegação
* [x] Incluir navegação via teclado
* [ ] Focar apenas em estética visual
* [x] Testar a aplicação com usuários que possuem deficiências
* [ ] Ignorar as diretrizes de acessibilidade

**Resposta:** ARIA, navegação por teclado e testes com usuários.

Além disso, é importante priorizar HTML semântico e utilizar ARIA quando necessário, seguindo diretrizes como WCAG.

---

## Redux

### Ao trabalhar com Redux, qual é uma prática correta para gerenciar o estado da aplicação?

* [ ] Manter estados globais para cada componente
* [x] Usar ações para descrever mudanças de estado
* [ ] Modificar o estado diretamente
* [x] Usar reducers para atualizar o estado com imutabilidade

**Resposta:** Actions descrevem mudanças e reducers atualizam o estado seguindo o princípio da imutabilidade.

Em projetos modernos, o **Redux Toolkit** é normalmente recomendado para simplificar essa implementação.

---

## Experiência centrada no usuário

### Qual dessas técnicas é considerada uma boa prática na construção de experiências centradas no usuário?

* [ ] Utilizar jargões complexos para demonstrar expertise
* [x] Recolher feedback dos usuários e iterar rapidamente
* [ ] Focar apenas em designs vistosos, sem funcionalidade
* [ ] Ignorar a acessibilidade na interface
* [ ] Desenvolver sem considerar as necessidades do usuário

**Resposta:** Recolher feedback dos usuários e iterar rapidamente.

Uma abordagem centrada no usuário envolve ciclos contínuos de pesquisa, validação, análise de dados e melhoria do produto.

---

## Estados assíncronos no React

### Ao trabalhar com estados assíncronos em uma aplicação React, qual é a ordem correta para gerenciar dados que vêm de uma API?

* [x] Realizar o fetch dos dados assim que o componente renderizar
* [x] Modelar os dados adequadamente e tratar estados de carregamento e erro
* [ ] Não se preocupar com tratamento de erro, apenas renderizar os dados
* [x] Usar uma biblioteca de gerenciamento de estado para cache dos dados

**Resposta:** Buscar os dados → modelar/tratar os estados → utilizar uma solução de cache quando necessário.

> **Observação:** a terceira opção não é obrigatória em todos os casos. Bibliotecas como TanStack Query são especialmente úteis para gerenciamento de **server state**, oferecendo cache, sincronização, refetch e controle do ciclo de vida dos dados.

---

## Design System

### Qual é a técnica correta para implementar um Design System em uma equipe de desenvolvimento?

* [x] Documentar componentes reutilizáveis e suas variações
* [ ] Ignorar a consistência visual entre os componentes
* [ ] Usar componentes apenas quando necessário, sem padrão definido
* [x] Incluir guidelines de acessibilidade nos documentos do Design System

**Resposta:** Documentação de componentes e variações + guidelines de acessibilidade.

Um Design System vai além de uma biblioteca de componentes: envolve padrões, documentação, tokens, acessibilidade e governança para garantir consistência entre produtos e times.

---

## Arquitetura Front-end

### Com quais práticas de arquitetura Front-end você possui experiência prática?

* [x] Componentização
* [x] Lazy Loading
* [x] State Management
* [x] Design Patterns
* [ ] Clean Code
* [ ] SOLID
* [x] Micro Frontend

**Resposta recomendada para uma pergunta especificamente sobre arquitetura:**

* Componentização
* State Management
* Design Patterns
* Micro Frontend

**Lazy Loading** pode ser considerado uma prática arquitetural dependendo do contexto, especialmente quando relacionado à estratégia de carregamento e divisão da aplicação.

Já **Clean Code** e **SOLID** são princípios de qualidade e design de software mais amplos. Eles influenciam diretamente a arquitetura, mas não são, por si só, arquiteturas Front-end.

---

## Micro Frontends

### Em um cenário de construção de componentes de interface com foco em micro frontends, quais tecnologias e abordagens são mais adequadas para garantir a reutilização e o isolamento entre eles?

* [x] Utilizar Module Federation para compartilhar dependências e carregar componentes dinamicamente.
* [x] Adotar Single-SPA para orquestrar a montagem e o ciclo de vida dos micro frontends.
* [ ] Implementar todos os componentes em um único pacote monolítico para simplificar o gerenciamento.
* [ ] Depender exclusivamente de iframes para isolar os componentes de negócio.
* [ ] Priorizar a integração via WebSockets para a comunicação entre os micro frontends.

**Resposta:** Module Federation e Single-SPA.

### Por quê?

**Module Federation** permite compartilhar dependências e carregar módulos dinamicamente entre aplicações.

**Single-SPA** atua como uma solução de orquestração, permitindo controlar a montagem e o ciclo de vida de diferentes micro frontends.

WebSockets são uma tecnologia de comunicação em tempo real, não uma estratégia de arquitetura para reutilização e isolamento de Micro Frontends.

---

## Observabilidade e qualidade

### Ao integrar um novo componente de interface com a plataforma existente, qual o fluxo correto para garantir a observabilidade e a qualidade das entregas?

* [x] Implementar testes automatizados (unitários e de integração) e configurar métricas de monitoramento.
* [x] Documentar a API utilizada pelo componente e os contratos de eventos.
* [ ] Realizar o deploy em produção sem testes prévios para agilizar a entrega.
* [ ] Utilizar apenas logs de console para depuração e monitoramento.
* [ ] Deixar a responsabilidade da observabilidade para o time de SRE sem envolvimento direto do frontend.

**Resposta:** Testes automatizados + métricas de monitoramento + documentação dos contratos.

A observabilidade é uma responsabilidade compartilhada. O time de Front-end também deve instrumentar suas aplicações e acompanhar métricas relevantes.

---

## Sistemas legados

### Qual a principal estratégia para lidar com sistemas legados de interface ao introduzir novos componentes?

* [x] Estrangular gradualmente as funcionalidades legadas conforme os novos componentes são implementados e validados.
* [ ] Substituir o sistema legado por completo de uma vez, sem uma abordagem incremental.
* [ ] Manter o sistema legado ativo e paralelo aos novos componentes indefinidamente.
* [ ] Integrar os novos componentes diretamente no código do sistema legado sem refatoração.
* [ ] Descontinuar o sistema legado sem um plano de migração.

**Resposta:** Migração gradual das funcionalidades legadas.

Essa abordagem é conhecida como **Strangler Fig Pattern**: novas funcionalidades são construídas sobre a nova arquitetura enquanto partes do sistema antigo são gradualmente substituídas.

---

## Componentes reutilizáveis

### Na construção de componentes de interface reutilizáveis, quais aspectos são fundamentais para assegurar a qualidade e a aderência aos padrões da plataforma?

* [x] Seguir os padrões de componentização definidos pela plataforma.
* [x] Implementar testes automatizados para garantir o comportamento esperado dos componentes.
* [ ] Utilizar ferramentas de IA para geração de código sem validação humana.
* [ ] Priorizar apenas a funcionalidade, negligenciando a segurança e a observabilidade.
* [ ] Utilizar tecnologias não suportadas pela plataforma para garantir a inovação.

**Resposta:** Seguir os padrões de componentização + testes automatizados.

A qualidade de um componente reutilizável também envolve aspectos como acessibilidade, segurança, observabilidade, documentação, manutenção e compatibilidade com a plataforma.

---

# Conceitos para estudar

Além das questões, alguns temas aparecem repetidamente em processos seletivos de Front-end:

* Componentização
* Design Systems
* Micro Frontends
* Module Federation
* Single-SPA
* State Management
* Server State
* TanStack Query
* REST APIs
* BFF
* TypeScript
* Design Patterns
* SOLID
* Clean Code
* Testes automatizados
* Acessibilidade
* Observabilidade
* Performance
* Lazy Loading
* Code Splitting
* Arquitetura modular
* Sistemas legados
* Strangler Fig Pattern

---

# Sobre este repositório

Este projeto nasceu da necessidade de organizar perguntas encontradas em processos seletivos e transformar esse material em uma fonte de consulta que também possa ser útil para outras pessoas da comunidade Front-end.

As perguntas podem ter sido originalmente formuladas por empresas, plataformas de recrutamento ou processos seletivos específicos. O objetivo aqui não é reproduzir um processo seletivo específico, mas organizar os conceitos e conhecimentos técnicos abordados nessas avaliações.

Contribuições, correções e sugestões são bem-vindas.
