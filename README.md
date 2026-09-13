# Frontend Interview Kit

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
* [Responsividade e Cross-Browser](#responsividade-e-cross-browser)
* [Inteligência Artificial](#inteligência-artificial)
* [Angular, SOLID e arquitetura](#angular-solid-e-arquitetura)
* [Testes e cultura de qualidade](#testes-e-cultura-de-qualidade)
* [APIs, BFF e arquitetura distribuída](#apis-bff-e-arquitetura-distribuída)
* [Liderança técnica e trade-offs](#liderança-técnica-e-trade-offs)
* [Performance e Core Web Vitals](#performance-e-core-web-vitals)

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

## Responsividade e Cross-Browser

### Conte sobre uma situação em que você desenvolveu ou manteve uma interface web que precisava ser responsiva e funcionar de forma consistente em navegadores diferentes.

**Resposta:** Já trabalhei com interfaces responsivas em React, Next.js e Angular, garantindo uma experiência consistente em diferentes resoluções e navegadores. Priorizava CSS e componentes com boa compatibilidade, testava os principais cenários e, quando encontrava diferenças entre navegadores, ajustava o CSS ou o comportamento dos componentes. A componentização e o Design System também ajudavam a manter esses ajustes consistentes em toda a aplicação.

### Dê um exemplo de um ajuste feito em um componente para garantir responsividade e compatibilidade cross-browser.

**Resposta:** Um exemplo foi ajustar componentes que utilizavam Flexbox para diferentes larguras de tela. Em alguns cenários, o conteúdo quebrava ou causava overflow. Ajustei o comportamento usando `flex-wrap`, limites de largura e breakpoints responsivos, além de evitar propriedades CSS com suporte inconsistente. Depois validei em diferentes resoluções e navegadores.

> **Observação:** este exemplo deve ser adaptado a um caso real do projeto caso o entrevistador peça detalhes específicos.

---

## Inteligência Artificial

### Poderia descrever sua experiência prática com Inteligência Artificial? Você já trabalhou na criação de agentes autônomos ou utiliza LLMs no seu dia a dia?

**Resposta:** Tenho experiência prática com IA aplicada ao desenvolvimento de software. Utilizo LLMs como Claude e GPT, além de ferramentas como GitHub Copilot, Cursor e OpenCode, para implementação, refatoração, análise de código, documentação, testes e resolução de problemas.

Também exploro workflows mais agentivos com OpenCode, utilizando modelos de IA para executar tarefas de desenvolvimento de forma mais autônoma, sempre com revisão e validação humana. Ainda não tive como principal responsabilidade a criação de agentes autônomos em produção.

### Conte sobre um caso concreto em que você utilizou IA Generativa no desenvolvimento.

**Resposta:** Um caso concreto foi utilizar IA Generativa para acelerar a implementação de funcionalidades em uma aplicação frontend complexa. Utilizei Claude, Cursor e OpenCode para analisar o contexto do código, estruturar a solução, implementar partes da funcionalidade e revisar possíveis problemas. O principal ganho foi reduzir o tempo gasto em tarefas repetitivas e investigação, permitindo maior foco nas decisões de arquitetura e regras de negócio. O código gerado sempre passou por revisão e validação humana.

### Como você garante a qualidade do código gerado por IA?

**Resposta:** Trato a IA como uma ferramenta de apoio, não como autoridade sobre o código. Forneço contexto e restrições claras, reviso a implementação, executo testes, verifico impactos na arquitetura e faço os ajustes necessários antes de integrar a mudança. Também considero segurança, performance, legibilidade e aderência aos padrões do projeto.

---

## Angular, SOLID e arquitetura

### Conte sobre uma decisão de arquitetura que você tomou em um projeto Angular usando princípios de SOLID ou Clean Architecture.

**Resposta:** Em aplicações Angular, encontrei componentes concentrando muitas responsabilidades, misturando regras de negócio, estado e comunicação com APIs. Uma decisão foi separar essas responsabilidades, mantendo os componentes mais focados na apresentação e levando regras e integrações para serviços específicos.

Considerei manter a estrutura existente, fazer uma refatoração pontual ou criar uma separação mais clara por responsabilidade. Optei pela última abordagem porque facilitava testes, reutilização e manutenção, seguindo principalmente os princípios de Single Responsibility e Dependency Inversion.

> **Observação:** SOLID pode orientar decisões arquiteturais sem significar que o projeto necessariamente utiliza uma implementação formal de Clean Architecture.

---

## Testes e cultura de qualidade

### Conte sobre uma situação em que você liderou ou influenciou o fortalecimento de uma cultura de testes que era limitada.

**Resposta:** Em alguns projetos encontrei cenários em que a cobertura de testes ainda era limitada, principalmente em funcionalidades mais antigas. A abordagem foi começar pelos pontos mais críticos, adicionando testes unitários e de integração e incorporando essas validações ao fluxo de desenvolvimento e CI/CD.

Também incentivei o time a considerar testes durante a implementação, e não apenas depois que a funcionalidade estava pronta, usando code reviews para reforçar esse padrão. A ideia era tornar os testes parte natural do processo, aumentando a confiança nas mudanças e reduzindo regressões.

> **Observação:** quando não houve liderança formal do time, é mais preciso apresentar a experiência como **influência técnica** ou liderança técnica pontual.

### Como você decide o que deve ser coberto por testes unitários, de integração ou E2E?

**Resposta:** Começo pelo risco e pela responsabilidade da funcionalidade. Testes unitários são adequados para regras e comportamentos isolados; integração para validar a interação entre partes relevantes do sistema; e E2E para fluxos críticos do ponto de vista do usuário. Procuro manter a maior parte da cobertura em testes rápidos e usar E2E de forma mais seletiva.

---

## APIs, BFF e arquitetura distribuída

### Você já precisou projetar ou ajustar a comunicação entre serviços em uma arquitetura distribuída, incluindo APIs RESTful?

**Resposta:** Em projetos com React, Vue e Angular, trabalhei bastante na integração com APIs REST e BFFs em arquiteturas distribuídas. Um dos principais desafios era garantir contratos claros, principalmente em fluxos como autenticação, onboarding e KYC.

Minha abordagem era alinhar contratos de entrada e saída, tratar estados de loading e erro, validações e mudanças de versão, além de evitar que regras específicas da API ficassem espalhadas pelos componentes. Quando necessário, centralizava a comunicação em serviços ou camadas específicas.

Isso ajudava a reduzir o acoplamento entre frontend e backend e tornava as integrações mais previsíveis e fáceis de evoluir.

> **Observação:** a experiência descrita é principalmente do lado do frontend e da integração com APIs/BFFs, não do desenvolvimento interno dos microsserviços de backend.

### Como você lida com breaking changes em APIs consumidas por múltiplas aplicações?

**Resposta:** Primeiro procuro evitar mudanças incompatíveis sem planejamento. Quando uma breaking change é necessária, alinho o contrato com os consumidores, avalio versionamento ou compatibilidade retroativa e faço a migração de forma incremental. Testes de contrato e comunicação clara entre os times também ajudam a reduzir o risco.

### Qual é o papel de um BFF em uma arquitetura frontend?

**Resposta:** O BFF pode adaptar os dados e contratos do backend às necessidades específicas do frontend, evitando que a aplicação cliente precise conhecer a complexidade de vários serviços. Isso pode simplificar agregação de dados, autenticação e tratamento de contratos, mas adiciona uma camada que também precisa ser mantida e observada.

---

## Liderança técnica e trade-offs

### Como você equilibra velocidade de entrega e qualidade arquitetural?

**Resposta:** Procuro avaliar o impacto e a vida útil da decisão. Para uma necessidade simples e de curto prazo, evito criar complexidade desnecessária. Quando a decisão afeta vários módulos, times ou futuras evoluções, invisto mais tempo em definir contratos, responsabilidades e uma estrutura sustentável.

Também prefiro evoluir a arquitetura de forma incremental, usando refatorações e melhorias contínuas em vez de tentar resolver todos os problemas de uma vez.

### Como você conduz uma decisão técnica quando existem opiniões diferentes no time?

**Resposta:** Procuro tirar a discussão do campo de preferência pessoal e trazer critérios objetivos, como impacto no produto, complexidade, manutenção, performance, custo e alinhamento com os padrões existentes. Quando necessário, faço um pequeno POC ou comparação das alternativas e documento a decisão para que o time tenha clareza sobre o contexto e os trade-offs.

---

## Performance e Core Web Vitals

### Como você investigaria um problema de LCP, CLS ou INP?

**Resposta:** Primeiro identificaria qual métrica está degradada e em quais páginas, dispositivos e condições isso acontece. Depois analisaria os principais fatores envolvidos: carregamento de recursos e conteúdo para LCP, mudanças inesperadas de layout para CLS e responsividade às interações para INP.

A partir dos dados, aplicaria uma otimização específica e validaria novamente o resultado, evitando otimizações baseadas apenas em percepção.

### Quais estratégias você utilizaria para melhorar a performance de uma aplicação React/Next.js?

**Resposta:** Dependeria do gargalo, mas consideraria code splitting e lazy loading, otimização de imagens e fontes, redução de JavaScript enviado ao cliente, cache, otimização de chamadas às APIs e renderização adequada para cada caso. Em Next.js, também avaliaria quais partes realmente precisam ser executadas no cliente e quais podem permanecer no servidor.

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
* API Contracts
* API Versioning
* BFF
* TypeScript
* Design Patterns
* SOLID
* Clean Code
* Testes automatizados
* Unit Testing
* Integration Testing
* E2E Testing
* Acessibilidade
* Observabilidade
* Performance
* Core Web Vitals
* LCP
* CLS
* INP
* Responsive Design
* Cross-Browser Compatibility
* Lazy Loading
* Code Splitting
* Arquitetura modular
* Sistemas legados
* Strangler Fig Pattern
* Generative AI
* LLMs
* AI-assisted development
* AI agents / agentic workflows
* Cursor
* Claude
* OpenCode
* Technical Leadership
* Architectural Trade-offs

---

# Sobre este repositório

Este projeto nasceu da necessidade de organizar perguntas encontradas em processos seletivos e transformar esse material em uma fonte de consulta que também possa ser útil para outras pessoas da comunidade Front-end.

As perguntas podem ter sido originalmente formuladas por empresas, plataformas de recrutamento ou processos seletivos específicos. O objetivo aqui não é reproduzir um processo seletivo específico, mas organizar os conceitos e conhecimentos técnicos abordados nessas avaliações.

Contribuições, correções e sugestões são bem-vindas.
