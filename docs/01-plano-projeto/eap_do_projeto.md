# Estrutura Analítica do Projeto (EAP / WBS) – Archeion

**Projeto:** Archeion
**Instituição:** Instituto Federal Catarinense (IFC) – Campus Videira  
**Referência Atual:** Novembro de 2026  

---

##  Visão Hierárquica (Árvore de Entregas)

```text
1.0 Archeion (portarias.gestao)
├── 1.1 Levantamento e Validação de Requisitos (KAN-8) [Mar/2026 – Jul/2026] 
│   ├── 1.1.1 Levantar processos atuais das portarias (KAN-13)
│   ├── 1.1.2 Levantar regras de negócio (KAN-14)
│   ├── 1.1.3 Levantar categorias de portarias (KAN-15)
│   ├── 1.1.4 Levantar perfis e níveis de acesso (KAN-16)
│   ├── 1.1.5 Levantar integrações necessárias (KAN-17)
│   ├── 1.1.6 Levantar requisitos funcionais (KAN-18)
│   ├── 1.1.7 Levantar requisitos não funcionais (KAN-19)
│   └── 1.1.8 Validar os requisitos com os responsáveis (KAN-20)
│
├── 1.2 Modelagem e Prototipação (KAN-9) [Ago/2026 – Nov/2026] 
│   ├── 1.2.1 Modelar banco de dados (KAN-21)
│   ├── 1.2.2 Modelar fluxo de solicitação, emissão e assinatura de portarias (KAN-22)
│   ├── 1.2.3 Prototipar interfaces do sistema (KAN-23)
│   └── 1.2.4 Validar protótipos e modelos (KAN-24)
│
├── 1.3 Desenvolvimento do Sistema (KAN-10) [A definir] 
│   ├── 1.3.1 Implementar autenticação e gerenciamento de usuários (KAN-25)
│   ├── 1.3.2 Implementar integração com cadastro usando e-mail institucional (KAN-26)
│   ├── 1.3.3 Implementar módulo de solicitação (KAN-27)
│   ├── 1.3.4 Implementar módulo de emissão (KAN-28)
│   ├── 1.3.5 Implementar módulo de composição (KAN-29)
│   ├── 1.3.6 Implementar módulo de validação (KAN-30)
│   ├── 1.3.7 Implementar controle de vigência (KAN-31)
│   ├── 1.3.8 Implementar controle do ciclo de vida (KAN-32)
│   ├── 1.3.9 Implementar módulo de assinatura (KAN-33)
│   ├── 1.3.10 Implementar módulo de retificação e renovação (KAN-34)
│   ├── 1.3.11 Implementar módulo de alertas (KAN-35)
│   ├── 1.3.12 Implementar módulo de relatórios (KAN-36)
│   └── 1.3.13 Implementar auditoria e rastreabilidade (KAN-37)
│
├── 1.4 Integração e Homologação (KAN-11) [A definir] 
│   ├── 1.4.1 Integrar com o sistema interno do IFC (simulação) (KAN-38)
│   ├── 1.4.2 Integrar com o SIPAC (simulação) (KAN-39)
│   ├── 1.4.3 Realizar testes funcionais (KAN-40)
│   ├── 1.4.4 Realizar testes de integração (KAN-41)
│   ├── 1.4.5 Testar regras de negócio (KAN-42)
│   ├── 1.4.6 Testar perfis e permissões (KAN-43)
│   ├── 1.4.7 Testar auditoria e rastreabilidade (KAN-44)
│   ├── 1.4.8 Corrigir problemas identificados (KAN-45)
│   └── 1.4.9 Realizar homologação com usuários-chave (KAN-46)
│
└── 1.5 Implantação e Encerramento (KAN-12) [A definir] 
    ├── 1.5.1 Preparar ambiente de produção (KAN-47)
    ├── 1.5.2 Implantar o sistema (KAN-48)
    ├── 1.5.3 Validar o ambiente de produção (KAN-49)
    ├── 1.5.4 Elaborar documentação técnica (KAN-50)
    ├── 1.5.5 Elaborar documentação funcional (KAN-51)
    └── 1.5.6 Encerrar o projeto (KAN-52)
```

---

## 📋 Dicionário da EAP e Cronograma Detalhado

### Pacote 1.1 – Levantamento e Validação de Requisitos (`KAN-8`)
**Período:** Março/2026 a Julho/2026 | **Status:**  Concluído

| Código EAP | ID Tarefa | Atividade / Pacote de Trabalho | Período / Data | Responsável Principal | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1.1.1** | `KAN-13` | Levantar processos atuais das portarias | 02/03/2026 – 20/03/2026 | Isadora Cozendey |  Concluído |
| **1.1.2** | `KAN-14` | Levantar regras de negócio | 23/03/2026 – 17/04/2026 | Isadora Cozendey |  Concluído |
| **1.1.3** | `KAN-15` | Levantar categorias de portarias | 20/04/2026 – 01/05/2026 | Isadora Cozendey |  Concluído |
| **1.1.4** | `KAN-16` | Levantar perfis e níveis de acesso | 04/05/2026 – 15/05/2026 | Hygor Marques |  Concluído |
| **1.1.5** | `KAN-17` | Levantar integrações necessárias | 18/05/2026 – 05/06/2026 | Hygor Marques |  Concluído |
| **1.1.6** | `KAN-18` | Levantar requisitos funcionais | 08/06/2026 – 26/06/2026 | Isadora Cozendey |  Concluído |
| **1.1.7** | `KAN-19` | Levantar requisitos não funcionais | 29/06/2026 – 10/07/2026 | Hygor Marques |  Concluído |
| **1.1.8** | `KAN-20` | Validar os requisitos com os responsáveis | 13/07/2026 – 31/07/2026 | Hygor & Isadora |  Concluído |

---

### Pacote 1.2 – Modelagem e Prototipação (`KAN-9`)
**Período:** Agosto/2026 a Novembro/2026 | **Status:** 🔄 Em Andamento

| Código EAP | ID Tarefa | Atividade / Pacote de Trabalho | Período / Data | Responsável Principal | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1.2.1** | `KAN-21` | Modelar banco de dados | 03/08/2026 – 04/09/2026 | Hygor Marques |  Concluído |
| **1.2.2** | `KAN-22` | Modelar fluxo de solicitação, emissão e assinatura de portarias | 07/09/2026 – 02/10/2026 | Isadora Cozendey |  Concluído |
| **1.2.3** | `KAN-23` | Prototipar interfaces do sistema | 05/10/2026 – 13/11/2026 | Isadora Cozendey |  Em Andamento |
| **1.2.4** | `KAN-24` | Validar protótipos e modelos | 16/11/2026 – 30/11/2026 | Hygor & Isadora |  Pendente |

---

### Pacote 1.3 – Desenvolvimento do Sistema (`KAN-10`)
**Período:** A definir | **Status:**  Pendente

| Código EAP | ID Tarefa | Atividade / Pacote de Trabalho | Período / Data | Responsável Principal | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1.3.1** | `KAN-25` | Implementar autenticação e gerenciamento de usuários | A definir | Hygor Marques |  Pendente |
| **1.3.2** | `KAN-26` | Implementar integração com cadastro usando e-mail institucional | A definir | Hygor Marques |  Pendente |
| **1.3.3** | `KAN-27` | Implementar módulo de solicitação | A definir | Hygor Marques |  Pendente |
| **1.3.4** | `KAN-28` | Implementar módulo de emissão | A definir | Hygor Marques |  Pendente |
| **1.3.5** | `KAN-29` | Implementar módulo de composição | A definir | Hygor Marques |  Pendente |
| **1.3.6** | `KAN-30` | Implementar módulo de validação | A definir | Hygor Marques |  Pendente |
| **1.3.7** | `KAN-31` | Implementar controle de vigência | A definir | Hygor Marques |  Pendente |
| **1.3.8** | `KAN-32` | Implementar controle do ciclo de vida | A definir | Hygor Marques |  Pendente |
| **1.3.9** | `KAN-33` | Implementar módulo de assinatura | A definir | Hygor Marques |  Pendente |
| **1.3.10** | `KAN-34` | Implementar módulo de retificação e renovação | A definir | Hygor Marques |  Pendente |
| **1.3.11** | `KAN-35` | Implementar módulo de alertas | A definir | Hygor Marques |  Pendente |
| **1.3.12** | `KAN-36` | Implementar módulo de relatórios | A definir | Hygor Marques |  Pendente |
| **1.3.13** | `KAN-37` | Implementar auditoria e rastreabilidade | A definir | Hygor Marques |  Pendente |

---

### Pacote 1.4 – Integração e Homologação (`KAN-11`)
**Período:** A definir | **Status:**  Pendente

| Código EAP | ID Tarefa | Atividade / Pacote de Trabalho | Período / Data | Responsável Principal | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1.4.1** | `KAN-38` | Integrar com o sistema interno do IFC (simulação) | A definir | Hygor Marques |  Pendente |
| **1.4.2** | `KAN-39` | Integrar com o SIPAC (simulação) | A definir | Hygor Marques |  Pendente |
| **1.4.3** | `KAN-40` | Realizar testes funcionais | A definir | Isadora Cozendey |  Pendente |
| **1.4.4** | `KAN-41` | Realizar testes de integração | A definir | Hygor Marques |  Pendente |
| **1.4.5** | `KAN-42` | Testar regras de negócio | A definir | Isadora Cozendey |  Pendente |
| **1.4.6** | `KAN-43` | Testar perfis e permissões | A definir | Isadora Cozendey |  Pendente |
| **1.4.7** | `KAN-44` | Testar auditoria e rastreabilidade | A definir | Hygor Marques |  Pendente |
| **1.4.8** | `KAN-45` | Corrigir problemas identificados | A definir | Hygor Marques |  Pendente |
| **1.4.9** | `KAN-46` | Realizar homologação com usuários-chave | A definir | Hygor & Isadora |  Pendente |

---

### Pacote 1.5 – Implantação e Encerramento (`KAN-12`)
**Período:** A definir | **Status:** ⏳ Pendente

| Código EAP | ID Tarefa | Atividade / Pacote de Trabalho | Período / Data | Responsável Principal | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1.5.1** | `KAN-47` | Preparar ambiente de produção | A definir | Hygor Marques |  Pendente |
| **1.5.2** | `KAN-48` | Implantar o sistema | A definir | Hygor Marques |  Pendente |
| **1.5.3** | `KAN-49` | Validar o ambiente de produção | A definir | Hygor & Isadora |  Pendente |
| **1.5.4** | `KAN-50` | Elaborar documentação técnica | A definir | Hygor Marques |  Pendente |
| **1.5.5** | `KAN-51` | Elaborar documentação funcional | A definir | Isadora Cozendey |  Pendente |
| **1.5.6** | `KAN-52` | Encerrar o projeto | A definir | Hygor & Isadora |  Pendente |
