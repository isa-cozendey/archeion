# Mapeamento de Talentos e Habilidades – Archeion

**Projeto:** Archeion (`portarias.gestao`)

**Instituição:** Instituto Federal Catarinense (IFC) – Campus Videira

**Data de Elaboração:** Novembro de 2026

## 1. Objetivo

Identificar as competências técnicas e interpessoais (hard e soft skills) dos membros da equipe de desenvolvimento do **Archeion**, garantindo que a alocação de tarefas na Estrutura Analítica do Projeto (EAP) potencialize os pontos fortes de cada integrante — dividindo as frentes de Engenharia de Software, Backend e Frontend/UI/UX de forma equilibrada.

## 2. Perfil Técnico da Equipe

### 2.1 Hygor Marques

* **Papel Principal:** Desenvolvedor Backend & Engenheiro de Software

* **Foco no Projeto:** Arquitetura de servidor, modelagem e persistência de dados, motor de regras de negócio no backend, segurança (RBAC), trilhas de auditoria, integrações com os sistemas institucionais (Sistema Interno do IFC e SIPAC) e engenharia de requisitos não-funcionais/arquitetura.

* **Competências Técnicas (Hard Skills):**

  * Arquitetura de Software e Modelagem de Banco de Dados Relacional (DER / SQL).

  * Desenvolvimento Backend (APIs RESTful, autenticação, controle de acesso baseado em papéis e processamento de regras de negócio).

  * Integração de Sistemas e Middleware (consumo de APIs institucionais e simulação de serviços).

  * Engenharia de Software (especificação de requisitos não-funcionais, testes de integração e documentação técnica de arquitetura).

  * Controle de versão com Git/GitHub e implantação/infraestrutura em ambiente de produção.

* **Competências Interpessoais (Soft Skills):**

  * Pensamento analítico e resolução de problemas lógicos complexos (como cálculos de carga horária, bloqueios de vigência e segregação de funções).

  * Visão sistêmica de segurança, performance e integridade de dados.

### 2.2 Isadora Cozendey

* **Papel Principal:** UI/UX Designer, Desenvolvedora Frontend & Engenheira de Software

* **Foco no Projeto:** Design de interfaces, prototipação navegável, desenvolvimento completo da camada Frontend (telas, formulários dinâmicos, validações visuais e consumo de APIs), além da engenharia de requisitos funcionais, regras de negócio e gestão documental/testes.

* **Competências Técnicas (Hard Skills):**

  * Desenvolvimento Frontend (construção de interfaces responsivas, componentização, gerenciamento de estado e integração com APIs REST).

  * UI/UX Design (arquitetura de informação, fluxos de usuário, wireframing e prototipação de alta fidelidade no Figma).

  * Engenharia de Software (elicitação e validação de requisitos funcionais, mapeamento de regras de negócio e modelagem de processos).

  * Garantia de Qualidade (QA), testes funcionais, testes de usabilidade e homologação com usuários-chave.

  * Gestão ágil de tarefas (Kanban / EAP) e elaboração de documentação funcional.

* **Competências Interpessoais (Soft Skills):**

  * Comunicação clara e empática com os stakeholders (Gabinete, CGP, Direção Geral e servidores).

  * Organização metodológica e atenção aos detalhes visuais e normativos (conformidade com boletins oficiais do IFC).

## 3. Divisão da Engenharia de Software e Matriz RACI

As atividades de Engenharia de Software são compartilhadas entre a dupla, respeitando a afinidade técnica de cada frente:

* **Engenharia de Software (Frente Hygor):** Arquitetura do sistema, modelagem de banco de dados, requisitos não-funcionais, plano de qualidade/testes de integração e documentação técnica.

* **Engenharia de Software (Frente Isadora):** Elicitação de requisitos funcionais, levantamento de regras de negócio, modelagem de processos (BPM/fluxos), testes funcionais/homologação e documentação funcional.

### Matriz de Responsabilidades (RACI)

* **R (Responsible / Responsável):** Executa a tarefa.

* **A (Accountable / Aprovador):** Responde pela entrega final e validação.

* **C (Consulted / Consultado):** Fornece insumos técnicos ou de negócio antes da execução.

* **I (Informed / Informado):** Acompanha o progresso e os resultados.

| Pacote / Entrega da EAP | Hygor Marques (Backend / Eng. Soft.) | Isadora Cozendey (Frontend / UI/UX / Eng. Soft.) | Stakeholders IFC (Gabinete/CGP/DG) | 
| ----- | ----- | ----- | ----- | 
| **1.1 Levantamento de Requisitos e Regras** | **R** (RNF / Integrações) | **R / A** (RF / Regras de Negócio) | C | 
| **1.2.1 Modelagem de Banco de Dados** | **R / A** | C | I | 
| **1.2.2 Modelagem de Fluxos e Processos** | C | **R / A** | C | 
| **1.2.3 Prototipação de Interfaces (UI/UX)** | C | **R / A** | C | 
| **1.3 Desenvolvimento Backend e Regras** | **R / A** | C | I | 
| **1.3 Desenvolvimento Frontend** | C | **R / A** | I | 
| **1.4 Integrações (IFC / SIPAC)** | **R / A** | C (Consumo na UI) | C | 
| **1.4 Testes (Integração vs. Funcionais)** | **R** (Integração / Segurança) | **R / A** (Funcionais / UI) | I | 
| **1.4 Homologação com Usuários-Chave** | **R** | **R** | **A** | 
| **1.5 Implantação em Produção** | **R / A** | C | C | 
| **1.5 Documentação Técnica e Funcional** | **R** (Técnica / Arquitetura) | **R / A** (Funcional / Manual) | I | 

## 4. Plano de Sinergia e Apoio Mútuo

* **Contrato de APIs (Backend ↔ Frontend):** Antes de iniciar a codificação dos módulos, Hygor e Isadora definem em conjunto os contratos JSON (endpoints, payloads e códigos de erro) para que o desenvolvimento do Frontend e do Backend ocorra em paralelo sem bloqueios.

* **Revisão Cruzada (Peer Review):** Todas as regras de negócio críticas (como limites de carga horária da Nota Técnica 001/2023, bloqueios de vigência e controle de acesso RBAC) são validadas tanto na camada visual (Frontend) quanto na camada de persistência/API (Backend).
