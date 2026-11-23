# API 3 — EntrenovaFlix

<p align="center">
  <strong>3º Semestre • 2025-2</strong><br>
  Plataforma web de diagnóstico organizacional com relatórios gerados por Inteligência Artificial e trilhas corporativas<br>
  Papel no Scrum: <strong>Desenvolvedor (Team Member)</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Institui%C3%A7%C3%A3o-Fatec%20SJC-blue?style=for-the-badge" alt="Fatec SJC">
  <img src="https://img.shields.io/badge/Categoria-Plataforma%20Web%20%2B%20IA-informational?style=for-the-badge" alt="Plataforma Web + IA">
  <img src="https://img.shields.io/badge/Papel-Desenvolvedor-orange?style=for-the-badge" alt="Desenvolvedor">
  <img src="https://img.shields.io/badge/Status-Conclu%C3%ADdo-success?style=for-the-badge" alt="Concluído">
</p>

---

## Navegação Rápida

- [Ficha Técnica do Projeto](#ficha-tecnica)
- [Parceiro e Contexto](#parceiro)
- [Desafio Proposto](#desafio)
- [Solução Desenvolvida](#solucao)
- [Cronograma das Sprints](#cronograma)
- [Repositório e Demonstração](#repositorio)
- [Stack Tecnológica](#tecnologias)
- [Minhas Contribuições](#contribuicoes)
- [Hard Skills e Soft Skills](#skills)
- [Reflexões e Aprendizados](#aprendizados)

---

<a id="ficha-tecnica"></a>

## Ficha Técnica do Projeto

| Atributo | Detalhamento |
|---|---|
| **Período Letivo** | 3º Semestre (2025-2) |
| **Nome do Projeto** | EntrenovaFlix — Diagnóstico Inteligente de Treinamentos e Mercado |
| **Natureza da Solução** | Plataforma web SaaS com diagnóstico empresarial assistido por IA |
| **Papel Exercido** | Desenvolvedor (Team Member) |
| **Foco de Atuação** | Apoio na lógica, estruturação de prompts e tratamento das respostas da IA (OpenAI API) |
| **Equipe** | DeepCode |
| **Metodologia** | Framework Scrum com backlog priorizado, estimativas em pontos e revisões de sprint |
| **Status** | Concluído |

---

<a id="parceiro"></a>

## Parceiro e Contexto

| Item | Informação |
|---|---|
| **Empresa Parceira** | Entrenova |
| **Segmento** | Educação corporativa que combina cinema, entretenimento digital e desenvolvimento de equipes |
| **Objetivo de Negócio** | Mapear gargalos das empresas clientes por meio de um diagnóstico automatizado para recomendar trilhas de capacitação |

---

<a id="desafio"></a>

## Desafio Proposto

A Entrenova buscava validar uma solução digital enxuta capaz de identificar rapidamente as necessidades de treinamento de empresas clientes antes da oferta comercial de suas trilhas educacionais. Para isso, era necessário construir um questionário diagnóstico estruturado pela parceira e transformar as respostas coletadas em um relatório analítico personalizado por meio de Inteligência Artificial.

O sistema precisava atender a dois objetivos simultâneos: entregar valor imediato ao gestor que respondia ao formulário — exibindo gratuitamente uma análise inicial de sua organização — e funcionar como funil de conversão para os planos pagos da plataforma.

---

<a id="solucao"></a>

## Solução Desenvolvida

Desenvolvemos o **EntrenovaFlix**, uma aplicação web construída em **Next.js, React e TypeScript**. Na plataforma, o representante da empresa responde a um diagnóstico dividido em quatro eixos estratégicos: **Pessoas e Cultura**, **Estrutura e Operações**, **Mercado e Clientes** e **Direção e Futuro**.

Os dados são gravados no **Firebase Firestore**, passam por uma etapa de pontuação e são enviados à **API da OpenAI**, que redige o diagnóstico personalizado. O usuário visualiza gratuitamente uma das dimensões avaliadas, pode receber o resumo em PDF por e-mail e, ao contratar um dos planos disponíveis, desbloqueia o relatório completo e o acesso às trilhas de aprendizagem com perfis distintos (Administrador, Gestor e Colaborador).

### Funcionalidades Entregues

- **Autenticação e Perfis de Acesso:** Cadastro e login via Firebase Authentication com controle de permissões por perfil.
- **Formulário Diagnóstico em 4 Dimensões:** Coleta estruturada de respostas com indicadores de progresso e validação de campos.
- **Motor de Diagnóstico com IA:** Integração com a API da OpenAI para gerar análises personalizadas com base na pontuação obtida.
- **Modelo Freemium e Planos:** Liberação gratuita de uma dimensão do relatório e bloqueio estratégico das demais até a contratação.
- **Exportação e Envio por E-mail:** Geração de PDF com PDFKit e disparo automático via Nodemailer.
- **Ambiente de Trilhas e Dashboard:** Área logada com trilhas de conteúdo, indicadores de evolução e gestão de equipe.

### Estrutura da Aplicação

| Diretório / Módulo | Responsabilidade |
|---|---|
| `app/` | Rotas e páginas da aplicação Next.js (landing page, autenticação, diagnóstico, relatório, planos e dashboard) |
| `app/api/gerar-diagnostico/` | Endpoint backend que processa as respostas e consulta a API da OpenAI |
| `app/lib/` | Configuração do Firebase e regras de pontuação das dimensões |
| `components/` | Componentes reutilizáveis da interface, formulário e relatórios |
| `hooks/` | Serviços auxiliares de integração com IA e envio de e-mails |

---

<a id="cronograma"></a>

## Cronograma das Sprints

| Marco / Sprint | Período | Escopo Entregue | Status |
|---|---|---|---|
| **Sprint 1** | 08/09/2025 a 28/09/2025 | Estruturação inicial do formulário diagnóstico e primeira versão do relatório | Concluída |
| **Sprint 2** | 06/10/2025 a 26/10/2025 | Unificação das 4 dimensões, regra de dimensão gratuita, envio de PDF por e-mail e planos | Concluída |
| **Sprint 3** | 03/11/2025 a 23/11/2025 | Fluxo de checkout, desbloqueio completo do relatório, dashboard e gestão de usuários | Concluída |

---

<a id="repositorio"></a>

## Repositório e Demonstração

- **Código-fonte no GitHub:** [API-DeepCode/API3_Entrenova](https://github.com/API-DeepCode/API3_Entrenova)

---

<a id="tecnologias"></a>

## Stack Tecnológica

| Camada | Ferramentas Utilizadas | Papel no Projeto |
|---|---|---|
| **Framework Web** | Next.js, React, TypeScript | Construção das páginas, rotas de API e tipagem estática |
| **Estilização e UI** | Tailwind CSS, shadcn/ui, Radix UI, Recharts | Design responsivo, componentes e gráficos do dashboard |
| **Formulários e Validação** | React Hook Form, Zod | Controle e validação das respostas do diagnóstico |
| **Banco e Autenticação** | Firebase Firestore, Firebase Authentication | Persistência dos diagnósticos e gestão de contas |
| **Inteligência Artificial** | OpenAI API | Geração textual dos relatórios de diagnóstico organizacional |
| **Documentos e Notificações** | PDFKit, Nodemailer | Geração do relatório em PDF e envio por e-mail |
| **Gestão e Versionamento** | Jira, Notion, Figma, Git, GitHub | Organização das sprints, documentação e controle de código |

---

<a id="contribuicoes"></a>

## Minhas Contribuições

No terceiro semestre, atuei como **desenvolvedor** na equipe *DeepCode*, colaborando especificamente na frente de **Inteligência Artificial** do projeto:

- **Apoio na Lógica e Estruturação das Chamadas à IA:** Contribuí nos ajustes da integração com a **API da OpenAI**, auxiliando na organização dos parâmetros enviados a partir das pontuações do diagnóstico para que o modelo recebesse o contexto adequado de cada dimensão avaliada (*Pessoas e Cultura*, *Estrutura e Operações*, *Mercado e Clientes* e *Direção e Futuro*).
- **Refinamento e Validação das Respostas:** Realizei testes com diferentes perfis de respostas simuladas para verificar a coerência dos textos gerados e ajudei a melhorar a formatação e o tratamento do retorno da IA, evitando quebras na exibição do relatório e garantindo uma linguagem objetiva para o gestor.

---

<a id="skills"></a>

## Hard Skills e Soft Skills

<details>
  <summary><strong>Hard Skills Desenvolvidas</strong></summary>

<br>

| Competência | Nível | Evidência Prática |
|---|---|---|
| **Integração com APIs de LLM (OpenAI)** | Com apoio | Ajustes na estruturação de prompts e tratamento das respostas retornadas |
| **TypeScript e Next.js** | Com apoio | Leitura e manutenção de rotas e serviços backend dentro da estrutura Next.js |
| **Validação e Testes de Saída de IA** | Autonomia | Testes de consistência dos relatórios gerados para diferentes cenários de pontuação |
| **Git e GitHub** | Autonomia | Trabalho colaborativo em branches e integração via pull requests |

</details>

<br>

<details>
  <summary><strong>Soft Skills Desenvolvidas</strong></summary>

<br>

| Competência | Aplicação no Projeto |
|---|---|
| **Colaboração em Equipe** | Atuei em conjunto com os colegas responsáveis pelo formulário e pela interface do relatório |
| **Atenção aos Detalhes** | Verifiquei inconsistências nas respostas textuais da IA para melhorar a legibilidade do diagnóstico |
| **Adaptabilidade** | Adaptei-me rapidamente a uma stack moderna baseada em Next.js, TypeScript e serviços em nuvem |

</details>

---

<a id="aprendizados"></a>

## Reflexões e Aprendizados

Participar do desenvolvimento do EntrenovaFlix permitiu observar a diferença prática entre rodar modelos de linguagem localmente — como fizemos no semestre anterior — e consumir uma API comercial em nuvem voltada a um produto B2B real.

Trabalhando nos ajustes e testes da camada de Inteligência Artificial, compreendi que o valor de um recurso de IA em aplicações corporativas depende diretamente da qualidade da estruturação dos dados enviados no prompt e da previsibilidade no tratamento da resposta, garantindo que o texto gerado se integre de forma limpa à interface do usuário.

---

<div align="center">

| Página Inicial | Projeto Anterior | Próximo Projeto |
|---|---|---|
| [README](./README.md) | [API 2 • DeepCode](./API_2.md) | [API 4 • EchoCAD](./API_4.md) |

</div>
