# API 1 — Os Python On

<p align="center">
  <strong>1º Semestre • 2024-2</strong><br>
  Portal web educativo dedicado ao ensino da metodologia ágil Scrum com módulos de estudo e questionários interativos<br>
  Papel no Scrum: <strong>Scrum Master (com atuação em desenvolvimento fullstack)</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Institui%C3%A7%C3%A3o-Fatec%20SJC-blue?style=for-the-badge" alt="Fatec SJC">
  <img src="https://img.shields.io/badge/Categoria-Aplica%C3%A7%C3%A3o%20Web-informational?style=for-the-badge" alt="Aplicação Web">
  <img src="https://img.shields.io/badge/Papel-Scrum%20Master-orange?style=for-the-badge" alt="Scrum Master">
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
| **Período Letivo** | 1º Semestre (2024-2) |
| **Nome do Projeto** | Os Python On |
| **Natureza da Solução** | Portal web educativo e interativo |
| **Papel Exercido** | Scrum Master |
| **Foco de Atuação** | Facilitação ágil, apoio ao PO, frontend (HTML/CSS/JS), backend (Flask), refatoração e correção de formulários |
| **Equipe** | Os Python On |
| **Metodologia** | Framework Scrum dividido em três sprints com entregas incrementais |
| **Status** | Concluído e apresentado na Feira de Soluções da Fatec SJC |

---

<a id="parceiro"></a>

## Parceiro e Contexto

| Item | Informação |
|---|---|
| **Cliente / Parceiro** | CADI – Centro de Aprendizagem em Desenvolvimento e Integração (Fatec São José dos Campos) |
| **Docente Responsável** | Prof. Antonio Egydio |
| **Objetivo Institucional** | Disponibilizar um recurso didático acessível sobre agilidade e Scrum para estudantes e comunidade externa |

---

<a id="desafio"></a>

## Desafio Proposto

A demanda apresentada pelo CADI consistia em criar um ambiente web claro e didático para introduzir os fundamentos, papéis, eventos e artefatos do framework Scrum a iniciantes, tanto dentro quanto fora da Fatec São José dos Campos. O material não deveria se limitar a definições teóricas, precisando trazer exemplos práticos e recursos visuais que facilitassem a compreensão.

Adicionalmente, o sistema precisava permitir que o estudante testasse os conhecimentos adquiridos ao final de cada etapa de estudo por meio de questionários interativos com feedback imediato.

---

<a id="solucao"></a>

## Solução Desenvolvida

A equipe construiu um **portal educativo sobre Scrum**, estruturado em uma página inicial de apresentação, cinco módulos sequenciais de conteúdo e cinco questionários de múltipla escolha correspondentes a cada módulo. Ao finalizar um teste, o usuário visualiza imediatamente quais questões acertou ou errou, sua pontuação final e a opção de refazer a avaliação.

Inicialmente concebido com páginas estáticas em HTML, CSS e JavaScript, o projeto evoluiu na última sprint para uma aplicação **Python com Flask**, utilizando renderização via templates Jinja2, design responsivo para dispositivos móveis e hospedagem na **AWS**.

### Funcionalidades Entregues

- **Apresentação e Conceitos Base:** Introdução ao Manifesto Ágil e à estrutura geral do Scrum.
- **Trilha de 5 Módulos:**
  - *Módulo 1:* Fundamentos, pilares e papéis do Scrum.
  - *Módulo 2:* Cerimônias e eventos da sprint.
  - *Módulo 3:* Auto-organização, equipes multifuncionais, time-boxing, iteração e gráfico Burndown interativo.
  - *Módulo 4:* Comparativo entre Scrum, Kanban e XP, além de casos reais de adoção.
  - *Módulo 5:* Ferramentas de apoio (Jira, Trello) e agilidade na transformação digital.
- **Avaliações Interativas:** Cinco questionários com cinco questões cada, validação de respostas, exibição de gabarito e reinício de tentativa.
- **Navegação Responsiva:** Menu suspenso, adaptação para telas móveis e seção de dúvidas frequentes (FAQ).

### Estrutura da Aplicação

| Diretório / Arquivo | Função na Arquitetura |
|---|---|
| `app.py` | Servidor Flask responsável pelo roteamento das páginas e módulos |
| `templates/` | Arquivos HTML estruturados com motor de templates Jinja2 |
| `static/style.css` | Folha de estilos global e regras de responsividade |
| `static/js/` | Scripts de interatividade dos questionários, FAQ e menus |
| `static/images/` | Ativos visuais, diagramas e identidade gráfica do portal |

---

<a id="cronograma"></a>

## Cronograma das Sprints

| Marco / Sprint | Período | Escopo Entregue | Status |
|---|---|---|---|
| **Kick-off** | 26/08/2024 a 06/09/2024 | Levantamento inicial do escopo e alinhamento com o Prof. Antonio Egydio | Concluído |
| **Sprint 1** | 09/09/2024 a 29/09/2024 | Definição do backlog, prototipação no Figma, página inicial e primeiros conteúdos | Concluída |
| **Sprint 2** | 07/10/2024 a 27/10/2024 | Desenvolvimento dos módulos intermediários/avançados e implementação dos questionários | Concluída |
| **Sprint 3** | 04/11/2024 a 24/11/2024 | Migração para Flask, ajustes de responsividade, correções e deploy na AWS | Concluída |
| **Feira de Soluções** | 12/12/2024 | Demonstração pública do portal na Fatec São José dos Campos | Concluída |

---

<a id="repositorio"></a>

## Repositório e Demonstração

- **Código-fonte no GitHub:** [Os-Python-On/API-OsPythonOn](https://github.com/Os-Python-On/API-OsPythonOn)
- **Vídeo de Demonstração:** [Assistir no YouTube](https://youtu.be/m6xBKumPmh0)

---

<a id="tecnologias"></a>

## Stack Tecnológica

| Camada | Ferramentas Utilizadas | Papel no Projeto |
|---|---|---|
| **Backend** | Python, Flask, Jinja2 | Estruturação das rotas e renderização dinâmica das páginas |
| **Frontend** | HTML5, CSS3, JavaScript | Marcação semântica, layout responsivo e lógica dos quizzes |
| **Visualização** | Chart.js, Remixicon | Renderização do gráfico Burndown interativo e iconografia |
| **Design e Planejamento** | Figma, Jira | Prototipação das telas e gestão do quadro Scrum |
| **Infraestrutura e Versionamento** | AWS, Git, GitHub | Hospedagem em nuvem e controle de versão colaborativo |

---

<a id="contribuicoes"></a>

## Minhas Contribuições

No primeiro semestre, assumi a responsabilidade de **Scrum Master** da equipe *Os Python On*, atuando simultaneamente como suporte direto ao Product Owner e como desenvolvedor em diversas frentes técnicas do sistema:

- **Facilitação Ágil e Gestão (Scrum Master):** Conduzi as reuniões de planejamento, acompanhamento diário e revisão das sprints, mantendo o quadro de tarefas atualizado no Jira, removendo impedimentos de integração entre os membros e auxiliando o Product Owner no refinamento e detalhamento das histórias de usuário.
- **Desenvolvimento Frontend e Backend:** Atuei de forma transversal no código da aplicação, auxiliando na construção e ajuste de páginas HTML/CSS/JavaScript e apoiando a estruturação das rotas em Python/Flask durante a transição do site estático para a aplicação web dinâmica.
- **Refatoração e Correção de Formulários:** Realizei revisões e refatorações no código para melhorar a organização dos scripts e corrigi erros de funcionamento e validação nos formulários dos questionários interativos, garantindo que o cálculo de acertos e o retorno visual funcionassem corretamente para o usuário.

---

<a id="skills"></a>

## Hard Skills e Soft Skills

<details>
  <summary><strong>Hard Skills Desenvolvidas</strong></summary>

<br>

| Competência | Nível | Evidência Prática |
|---|---|---|
| **Scrum e Gestão Ágil** | Autonomia | Facilitação das sprints, cerimônias e gestão do quadro no Jira |
| **HTML5 e CSS3** | Autonomia | Estruturação e ajustes visuais das páginas do portal |
| **JavaScript** | Com apoio | Manutenção da lógica dos questionários e correção de falhas nos formulários |
| **Python e Flask** | Com apoio | Apoio nas rotas e na organização dos templates na Sprint 3 |
| **Refatoração e Debugging** | Autonomia | Identificação e correção de bugs nos testes interativos |
| **Git e GitHub** | Com apoio | Controle de versão, commits e integração de código em equipe |

</details>

<br>

<details>
  <summary><strong>Soft Skills Desenvolvidas</strong></summary>

<br>

| Competência | Aplicação no Projeto |
|---|---|
| **Facilitação e Liderança Servidora** | Apoiei o ritmo do time como Scrum Master e ajudei a destravar gargalos técnicos |
| **Comunicação** | Mantive o alinhamento constante entre o Product Owner, os desenvolvedores e o cliente |
| **Visão Sistêmica** | Atuei tanto na organização das entregas quanto no código frontend e backend conforme a necessidade |
| **Resolução de Problemas** | Diagnostiquei e corrigi falhas nos formulários de quiz antes das entregas de sprint |

</details>

---

<a id="aprendizados"></a>

## Reflexões e Aprendizados

O API 1 foi uma experiência singular por unir teoria e prática de forma imediata: enquanto desenvolvíamos um portal para ensinar Scrum, vivenciávamos cada cerimônia, artefato e papel do framework na construção do próprio produto.

Atuar como Scrum Master logo no primeiro semestre ensinou-me a importância da comunicação transparente, do acompanhamento contínuo das tarefas e do apoio mútuo dentro da equipe. Ao mesmo tempo, colocar a mão na massa no frontend, no backend em Flask e na correção de bugs consolidou minha base de programação web e mostrou como a refatoração e os testes são indispensáveis para entregar um sistema confiável.

---

<div align="center">

| Página Inicial | Projeto Anterior | Próximo Projeto |
|---|---|---|
| [README](./README.md) | — | [API 2 • DeepCode](./API_2.md) |

</div>
