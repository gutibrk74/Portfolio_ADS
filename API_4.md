# API 4 — EchoCAD

<p align="center">
  <strong>4º Semestre • 2026-1</strong><br>
  Automatização de memoriais de cálculo, orçamentos SINAPI e especificações técnicas a partir de plantas CAD (.DXF) com IA<br>
  Papel no Scrum: <strong>Desenvolvedor (Backend, Extração DXF e IA)</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Institui%C3%A7%C3%A3o-Fatec%20SJC-blue?style=for-the-badge" alt="Fatec SJC">
  <img src="https://img.shields.io/badge/Categoria-Web%20%2B%20CAD%20%2B%20IA-informational?style=for-the-badge" alt="Web + CAD + IA">
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
| **Período Letivo** | 4º Semestre (2026-1) |
| **Nome do Projeto** | EchoCAD — Automatização de Documentos Técnicos de Obras |
| **Natureza da Solução** | Aplicação web fullstack com processamento geométrico de plantas CAD e geração documental com IA |
| **Papel Exercido** | Desenvolvedor (Backend, Processamento DXF e Inteligência Artificial) |
| **Foco de Atuação** | Criação e correção de rotas FastAPI, extração de dados de arquivos DXF (`ezdxf`) e apoio no módulo de IA |
| **Equipe** | Equipe Echo |
| **Metodologia** | Framework Scrum com backlog priorizado, DoR, DoD e revisão via pull requests |
| **Status** | Concluído e apresentado na Feira de Soluções da Fatec SJC |

---

<a id="parceiro"></a>

## Parceiro e Contexto

| Item | Informação |
|---|---|
| **Organização Parceira** | Exército Brasileiro — Guarnição de Caçapava |
| **Contexto Operacional** | Engenharia militar e elaboração de documentação técnica para licenciamento e licitação de obras |
| **Objetivo da Parceria** | Reduzir o tempo operacional e minimizar falhas humanas no levantamento manual de plantas arquitetônicas |

---

<a id="desafio"></a>

## Desafio Proposto

Para viabilizar o licenciamento e abrir processos licitatórios de obras, a equipe de engenharia do **Exército Brasileiro (Guarnição de Caçapava)** precisa elaborar um conjunto rigoroso de documentos técnicos — entre eles **memoriais de cálculo**, **planilhas orçamentárias** e **especificações técnicas** em conformidade com as normas da ABNT.

Tradicionalmente, esse levantamento é executado de forma manual a partir da leitura de plantas em CAD: engenheiros medem áreas, perímetros e ambientes, calculam quantitativos de materiais, pesquisam composições de custos na tabela **SINAPI** e redigem os textos normativos. Trata-se de um fluxo demorado, repetitivo e sujeito a inconsistências de contagem. O desafio proposto à equipe foi automatizar essa cadeia a partir do envio digital da planta CAD.

---

<a id="solucao"></a>

## Solução Desenvolvida

Desenvolvemos o **EchoCAD**, uma plataforma web conteinerizada que recebe uma planta baixa no formato **DXF** e automatiza a geração dos documentos de engenharia da obra.

No backend, construído em **Python com FastAPI**, o sistema realiza a leitura estrutural do arquivo DXF por meio da biblioteca **ezdxf**, identificando camadas, entidades geométricas e ambientes para calcular os quantitativos. Com esses dados extraídos, o sistema preenche automaticamente uma planilha **XLSX** de memorial de cálculo vinculada aos custos de insumos da tabela **SINAPI**. Paralelamente, modelos de linguagem — **Groq (Llama 3.3 70B)** em nuvem ou **Ollama (Qwen 2.5)** localmente — redigem as especificações técnicas referenciando as normas NBR aplicáveis, exportadas em formato **DOCX**.

### Funcionalidades Entregues

- **Upload e Validação CAD:** Recebimento de plantas no formato `.DXF` com verificação de integridade.
- **Extração Geométrica Automatizada:** Leitura de layers, polígonos, dimensões e elementos arquitetônicos via `ezdxf`.
- **Memorial de Cálculo e Custos SINAPI:** Geração de planilha Excel estruturada por etapas da obra com preços de referência.
- **Especificações Técnicas Assistidas por IA:** Redação automatizada de texto técnico normativo (ABNT/NBR) exportado em `.DOCX`.
- **Acompanhamento em Tempo Real e Histórico:** Monitoramento das etapas de processamento, consulta de projetos salvos e gestão de chaves de API criptografadas por usuário.

### Estrutura da Aplicação

| Camada / Módulo | Responsabilidade |
|---|---|
| **Backend (`FastAPI`)** | Gerenciamento de rotas REST, autenticação JWT, upload, orquestração do processamento e persistência |
| **Motor de Extração CAD (`ezdxf`)** | Leitura do arquivo `.DXF`, filtragem de camadas e extração de medidas e entidades |
| **Gerador de Memorial (`openpyxl`)** | Cruzamento de quantitativos com base SINAPI e montagem da planilha `.XLSX` |
| **Gerador de Especificações (`IA + python-docx`)** | Chamadas aos LLMs (Groq/Ollama) e exportação do documento técnico `.DOCX` |
| **Frontend (`React + Vite + TS`)** | Interface de envio de plantas, acompanhamento de progresso, histórico e normas técnicas |
| **Banco de Dados (`MariaDB`)** | Armazenamento de usuários, projetos, metadados de plantas e documentos gerados |
| **Infraestrutura (`Docker Compose`)** | Orquestração dos serviços de frontend, backend, banco de dados e modelos locais |

---

<a id="cronograma"></a>

## Cronograma das Sprints

| Marco / Sprint | Período | Escopo Entregue | Status |
|---|---|---|---|
| **Sprint 1** | 16/03/2026 a 05/04/2026 | Extração inicial de dados DXF, cálculo básico do memorial e estrutura base da interface | Concluída |
| **Sprint 2** | 13/04/2026 a 03/05/2026 | Integração com IA para especificações técnicas, persistência de projetos e cadastro de normas | Concluída |
| **Sprint 3** | 11/05/2026 a 31/05/2026 | Consolidação das rotas, autenticação, exportação completa (XLSX/DOCX) e ajustes finais | Concluída |
| **Feira de Soluções** | 25/06/2026 | Apresentação oficial e demonstração prática para avaliadores e parceiros | Concluída |

---

<a id="repositorio"></a>

## Repositório e Demonstração

- **Código-fonte no GitHub:** [EquipeEcho/EchoCAD](https://github.com/EquipeEcho/EchoCAD)
- **Demonstração Sprint 1 (MVP):** [Assistir no YouTube](https://youtu.be/TYSAJDFz9T0)
- **Demonstração Sprint 3 (Sistema Completo):** [Assistir no YouTube](https://www.youtube.com/watch?v=uGvk_viRp7I)

---

<a id="tecnologias"></a>

## Stack Tecnológica

| Camada | Ferramentas Utilizadas | Papel no Projeto |
|---|---|---|
| **Backend e APIs** | Python, FastAPI, Pydantic | Endpoints REST, validação de esquemas e regras de negócio |
| **Processamento CAD** | ezdxf, NetworkX | Leitura de arquivos DXF e extração de entidades geométricas |
| **Geração Documental** | pandas, openpyxl, python-docx | Construção das planilhas SINAPI (.XLSX) e especificações (.DOCX) |
| **Inteligência Artificial** | Groq (Llama 3.3 70B), Ollama (Qwen 2.5) | Geração automatizada das especificações técnicas normativas |
| **Banco de Dados** | MariaDB, SQLAlchemy, Alembic | Persistência relacional e versionamento de schema |
| **Frontend** | React, TypeScript, Vite, React Router | Interface web, visualização de resultados e histórico |
| **Segurança e Infraestrutura** | JWT, bcrypt, Fernet, Docker, Docker Compose | Autenticação, criptografia de chaves e execução em contêineres |

---

<a id="contribuicoes"></a>

## Minhas Contribuições

No quarto semestre, concentrei minha atuação no **desenvolvimento backend em Python e FastAPI**, trabalhando diretamente no núcleo de processamento de arquivos CAD e na organização das rotas da API:

- **Implementação e Correção de Rotas no FastAPI:** Desenvolvi endpoints da aplicação e realizei a revisão estrutural das rotas do backend, identificando e **corrigindo problemas de rotas duplicadas** que geravam conflitos de mapeamento e comportamento inesperado nas requisições da API.
- **Extração de Dados de Arquivos DXF (`ezdxf`):** Participei ativamente da implementação e ativação do módulo responsável por ler os arquivos de plantas CAD no formato `.DXF`, percorrendo camadas (*layers*) e entidades geométricas para extrair de forma funcional e confiável os dados necessários aos cálculos do memorial.
- **Apoio no Módulo de Inteligência Artificial:** Colaborei na integração e nos ajustes do serviço de geração de especificações técnicas com IA (Groq/Ollama), auxiliando na passagem dos dados extraídos da planta para a geração dos textos normativos.

---

<a id="skills"></a>

## Hard Skills e Soft Skills

<details>
  <summary><strong>Hard Skills Desenvolvidas</strong></summary>

<br>

| Competência | Nível | Evidência Prática |
|---|---|---|
| **Python e FastAPI** | Autonomia | Criação de endpoints, organização de roteadores e correção de rotas duplicadas |
| **Leitura de Arquivos CAD (`ezdxf`)** | Autonomia | Extração funcional de camadas e entidades geométricas de plantas `.DXF` |
| **Integração com LLMs (Groq / Ollama)** | Com apoio | Apoio na alimentação de contexto e geração de especificações técnicas com IA |
| **SQLAlchemy e Bancos Relacionais** | Com apoio | Integração dos endpoints com a persistência de dados no MariaDB |
| **Docker e Ambientes Linux/Windows** | Com apoio | Execução e testes dos serviços conteinerizados em ambiente local |
| **Git e GitHub** | Autonomia | Uso de branches de feature, resolução de conflitos e pull requests |

</details>

<br>

<details>
  <summary><strong>Soft Skills Desenvolvidas</strong></summary>

<br>

| Competência | Aplicação no Projeto |
|---|---|
| **Investigação e Depuração** | Identifiquei e eliminei conflitos de rotas duplicadas no FastAPI e destravei a extração DXF |
| **Compreensão de Domínio** | Estudei conceitos de plantas CAD, layers e documentação de obras para validar os dados extraídos |
| **Trabalho Colaborativo** | Integrei o pipeline de extração CAD com os módulos de planilha SINAPI e interface frontend |
| **Persistência Técnica** | Atuei na estabilização da leitura de arquivos DXF até tornar a extração operacional no fluxo principal |

</details>

---

<a id="aprendizados"></a>

## Reflexões e Aprendizados

O EchoCAD representou o desafio técnico mais complexo da graduação até o momento, pois exigiu lidar com um formato de arquivo especializado da engenharia civil (`.DXF`) e transformar geometrias brutas em insumos estruturados para orçamentos e documentos normativos.

Atuar no backend com FastAPI, resolver conflitos de rotas duplicadas e viabilizar a extração de dados das plantas CAD consolidou minha segurança no desenvolvimento de APIs em Python. Além disso, trabalhar em uma demanda real do Exército Brasileiro evidenciou a importância da confiabilidade dos dados extraídos na origem, já que qualquer imprecisão na leitura da planta impacta diretamente tanto os cálculos orçamentários quanto o texto gerado pela Inteligência Artificial.

---

<div align="center">

| Página Inicial | Projeto Anterior | Próximo Projeto |
|---|---|---|
| [README](./README.md) | [API 3 • EntrenovaFlix](./API_3.md) | — |

</div>
