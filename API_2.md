# API 2 — DeepCode

<p align="center">
  <strong>2º Semestre • 2025-1</strong><br>
  Aplicação desktop com assistente de Inteligência Artificial executado localmente para análise e correção de código<br>
  Papel no Scrum: <strong>Product Owner (PO)</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Institui%C3%A7%C3%A3o-Fatec%20SJC-blue?style=for-the-badge" alt="Fatec SJC">
  <img src="https://img.shields.io/badge/Categoria-Desktop%20%2B%20IA%20Local-informational?style=for-the-badge" alt="Desktop + IA Local">
  <img src="https://img.shields.io/badge/Papel-Product%20Owner-orange?style=for-the-badge" alt="Product Owner">
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
| **Período Letivo** | 2º Semestre (2025-1) |
| **Nome do Projeto** | DeepCode |
| **Natureza da Solução** | Aplicação desktop para suporte ao desenvolvimento com IA local |
| **Papel Exercido** | Product Owner (PO) |
| **Foco de Atuação** | Gestão de backlog, alinhamento com cliente, definição de fluxo/UI e apoio na lógica de integração com Ollama |
| **Equipe** | DeepCode |
| **Metodologia** | Framework Scrum com três sprints, revisões com cliente e acompanhamento via Jira |
| **Status** | Concluído e apresentado na Feira de Soluções da Fatec SJC |

---

<a id="parceiro"></a>

## Parceiro e Contexto

| Item | Informação |
|---|---|
| **Cliente / Parceiro** | CADI – Centro de Aprendizagem em Desenvolvimento e Integração (Fatec São José dos Campos) |
| **Docente Responsável** | Prof. Giuliano Bertoti |
| **Objetivo Institucional** | Criar uma ferramenta local de apoio à identificação e correção de erros em códigos de programação |

---

<a id="desafio"></a>

## Desafio Proposto

O objetivo do segundo semestre foi desenvolver um ambiente desktop capaz de auxiliar programadores e estudantes na detecção e correção de falhas em trechos de código, reduzindo o tempo gasto em depuração e organizando o histórico de consultas realizadas.

Um requisito central estabelecido pelo cliente era a **privacidade e autonomia local**: o código inserido pelo usuário não poderia trafegar para APIs externas na nuvem, exigindo que o processamento de Inteligência Artificial fosse executado integralmente na máquina local.

---

<a id="solucao"></a>

## Solução Desenvolvida

A equipe desenvolveu o **DeepCode**, uma aplicação desktop construída em **Java e JavaFX** integrada ao motor de modelos locais **Ollama** (utilizando o modelo **Qwen 2.5 Coder**). O usuário insere um trecho de código em Python na interface, aciona a análise e recebe o diagnóstico com explicações e sugestões de correção geradas localmente.

As respostas geradas pelo modelo podem ser nomeadas e armazenadas em um banco de dados **MySQL**, permitindo que o usuário consulte, filtre ou remova análises anteriores por meio de um painel lateral de histórico.

### Funcionalidades Entregues

- **Editor de Entrada:** Campo dedicado à inserção de código com validação de entrada vazia e limpeza rápida.
- **Processamento com IA Local:** Comunicação HTTP com o servidor Ollama local utilizando `Modelfile` customizado para análise de exercícios e scripts.
- **Visualização de Diagnóstico:** Tela dedicada à exibição da resposta da IA com registro de data e hora, opção de nova consulta e salvamento.
- **Gestão de Histórico:** Persistência em MySQL com listagem em menu lateral, filtro por título e exclusão com confirmação.
- **Feedback Visual:** Barra de status informando o andamento das requisições e operações.

### Estrutura da Aplicação

| Módulo / Classe | Responsabilidade |
|---|---|
| `gui/Main.java` | Controlador principal da interface gráfica em JavaFX e navegação entre telas |
| `gui/application.css` | Estilização visual, layout e animações da interface |
| `ia/IA.java` | Camada de comunicação HTTP e tratamento JSON com o serviço local Ollama |
| `dao/HistoricoDAO.java` | Operações CRUD de persistência do histórico no MySQL |
| `factory/ConnectionFactory.java` | Gerenciamento de conexões JDBC com o banco de dados |
| `Modelfile` | Definição de parâmetros e instruções do modelo Qwen 2.5 Coder no Ollama |

---

<a id="cronograma"></a>

## Cronograma das Sprints

| Marco / Sprint | Período | Escopo Entregue | Status |
|---|---|---|---|
| **Kick-off** | 24/02/2025 a 28/02/2025 | Apresentação do desafio pelo Prof. Giuliano Bertoti e levantamento inicial | Concluído |
| **Sprint 1** | 10/03/2025 a 30/03/2025 | Prototipação de telas, estrutura inicial e primeira comunicação com o Ollama | Concluída |
| **Sprint 2** | 07/04/2025 a 27/04/2025 | Separação do fluxo entre tela de envio e resposta e refinamento da interação com a IA | Concluída |
| **Sprint 3** | 05/05/2025 a 25/05/2025 | Persistência do histórico no MySQL, filtro lateral e vídeo tutorial de instalação | Concluída |
| **Feira de Soluções** | 29/05/2025 | Apresentação pública da aplicação desktop em funcionamento | Concluída |

---

<a id="repositorio"></a>

## Repositório e Demonstração

- **Código-fonte no GitHub:** [API-DeepCode/API2](https://github.com/API-DeepCode/API2)
- **Tutorial de Instalação e Uso:** [Assistir no YouTube](https://www.youtube.com/watch?v=vB7EBUyKuwA)

---

<a id="tecnologias"></a>

## Stack Tecnológica

| Camada | Ferramentas Utilizadas | Papel no Projeto |
|---|---|---|
| **Linguagem Base** | Java | Estruturação da aplicação desktop e regras de negócio |
| **Interface Gráfica** | JavaFX, CSS | Construção das janelas, componentes visuais e estilização |
| **Inteligência Artificial** | Ollama, Qwen 2.5 Coder | Execução local do modelo de linguagem para análise de código |
| **Comunicação e Parsing** | HTTP Client, org.json | Envio de prompts e leitura das respostas retornadas pelo Ollama |
| **Persistência** | MySQL, JDBC | Armazenamento e consulta das respostas salvas |
| **Prototipação e Gestão** | Figma, Jira, Eclipse, Git/GitHub | Wireframes, gestão do backlog, desenvolvimento e versionamento |

---

<a id="contribuicoes"></a>

## Minhas Contribuições

No API 2, assumi o papel de **Product Owner (PO)** da equipe *DeepCode*, concentrando minha atuação na definição do produto, no alinhamento com o cliente e na lógica central de Inteligência Artificial:

- **Gestão do Produto e Backlog (PO):** Fui responsável por traduzir os requisitos do Prof. Giuliano Bertoti em histórias de usuário claras, priorizar o backlog a cada sprint e validar as entregas nas reuniões de revisão.
- **Apoio na Lógica Central com Ollama:** Como o diferencial técnico do produto era o processamento local de código, acompanhei de perto e colaborei na lógica de integração com o **Ollama**, ajudando a estruturar o envio do código, a definição das instruções do modelo (`Modelfile`) e a validação da qualidade das respostas geradas para garantir que o núcleo do sistema atendesse ao esperado.
- **Definição de Fluxo e Experiência de Uso:** Embora não tenha atuado diretamente na codificação da interface gráfica em JavaFX nem na camada de banco de dados MySQL (conduzidas por outros integrantes da equipe), participei ativamente da definição funcional de como as telas deveriam se comportar — especificando o fluxo entre envio de código, exibição da resposta e organização do histórico.

---

<a id="skills"></a>

## Hard Skills e Soft Skills

<details>
  <summary><strong>Hard Skills Desenvolvidas</strong></summary>

<br>

| Competência | Nível | Evidência Prática |
|---|---|---|
| **Product Ownership e Backlog** | Autonomia | Escrita, priorização e validação de histórias de usuário ao longo das 3 sprints |
| **Integração com LLMs Locais (Ollama)** | Autonomia | Apoio na lógica de requisição, configuração de comportamento do modelo e testes de resposta |
| **Especificação Funcional e UX** | Com apoio | Definição dos fluxos de interação entre usuário, editor e resposta da IA |
| **Arquitetura Cliente-IA Local** | Com apoio | Compreensão da comunicação HTTP/JSON entre aplicação Java e serviço Ollama |
| **Git e GitHub** | Autonomia | Acompanhamento das entregas e organização das branches do repositório |

</details>

<br>

<details>
  <summary><strong>Soft Skills Desenvolvidas</strong></summary>

<br>

| Competência | Aplicação no Projeto |
|---|---|
| **Negociação e Alinhamento** | Intermediei expectativas técnicas e prazos entre o docente cliente e a equipe de desenvolvimento |
| **Tomada de Decisão** | Priorizei o funcionamento sólido da IA local nas primeiras sprints antes de expandir funcionalidades secundárias |
| **Comunicação Assertiva** | Detalhei critérios de aceitação para que a equipe de interface e banco soubesse exatamente o que entregar |
| **Visão de Produto** | Garanti que o requisito de privacidade (execução 100% offline) fosse respeitado em toda a arquitetura |

</details>

---

<a id="aprendizados"></a>

## Reflexões e Aprendizados

Assumir o papel de Product Owner no DeepCode ampliou minha percepção sobre como decisões de escopo impactam diretamente a viabilidade técnica de um software. Como o projeto dependia do desempenho e da precisão de um modelo de linguagem rodando localmente, foi fundamental acompanhar a lógica do Ollama de perto para alinhar o que era tecnicamente viável com as expectativas do cliente.

Também aprendi na prática como dividir responsabilidades em uma equipe multidisciplinar: enquanto colegas assumiram a implementação detalhada do JavaFX e da persistência em MySQL, meu foco esteve em garantir a coesão do fluxo funcional, a priorização correta das entregas e a consistência da inteligência artificial que sustentava o produto.

---

<div align="center">

| Página Inicial | Projeto Anterior | Próximo Projeto |
|---|---|---|
| [README](./README.md) | [API 1 • Os Python On](./API_1.md) | [API 3 • EntrenovaFlix](./API_3.md) |

</div>
