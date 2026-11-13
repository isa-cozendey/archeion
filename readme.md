# Archeion

> **Sistema de Gestão e Automação do Ciclo de Vida de Portarias Institucionais**  
> Instituto Federal Catarinense (IFC) – Campus Videira

![Status do Projeto](https://img.shields.io/badge/Status-Em%20Modelagem%20e%20Prototipa%C3%A7%C3%A3o-blue)
![Instituição](https://img.shields.io/badge/IFC-Campus%20Videira-green)

---

## Sobre

O Archeion é uma solução de software desenvolvida para digitalizar, centralizar e controlar todo o ciclo de vida das portarias institucionais do IFC – Campus Videira — abrangendo desde a solicitação inicial até a assinatura eletrônica, publicação oficial, acompanhamento de vigência, retificações, revogações e arquivamento.

### Objetivos Principais
* **Centralização e Rastreabilidade:** Reunir o histórico completo de portarias, processos associados e alterações em um ambiente único e auditável.
* **Automação de Validações:** Aplicar regras de negócio institucionais automaticamente (controle de carga horária, segregação de funções, cotas de representação e prazos de mandato).
* **Redução de Erros Operacionais:** Puxar dados cadastrais de servidores diretamente da base institucional, evitando falhas de digitação (SIAPE, setor, carga horária).
* **Gestão Proativa de Prazos:** Emitir alertas automáticos para vencimentos de mandatos, entrega de relatórios de GTs/bancas e irregularidades de representação.
* **Integração Institucional:** Conectar-se ao **Sistema Interno de Cadastro do IFC** (validação de dados) e ao **SIPAC** (protocolo, armazenamento e publicação oficial).

---

## Perfis de Acesso (RBAC)

* **Diretor Geral (DG):** Nível máximo de acesso; realiza a assinatura eletrônica das portarias (incluindo substitutos legais) e acessa relatórios gerenciais sensíveis.
* **Emissor (Gabinete / CGP):** Realiza a triagem de solicitações, cadastro, edição, validação técnica e tramitação das portarias.
* **Requerente (Servidores / Geral):** Solicita a emissão de novas portarias e acompanha o andamento das suas demandas.
* **Consultor:** Acesso de leitura às informações e portarias autorizadas.

---

## Estrutura do Repositório

```text
/archeion
│
├── .github/                  # Templates de Issues, PRs e workflows
├── docs/                     # Documentação completa de Engenharia de Software
│   ├── 01-plano-projeto/     # Termo de Abertura, Plano de Projeto, EAP e Cronograma
│   ├── 02-requisitos/        # Requisitos Funcionais, Não-Funcionais e Regras de Negócio
│   ├── 03-modelagem/         # Diagramas UML, DER (Banco de Dados) e Arquitetura
│   ├── 04-interfaces/        # Especificação de telas e fluxos de navegação
│   └── 05-aceitacao/         # Critérios de aceitação e planos de teste
│
├── src/                      # Código-fonte da aplicação (Backend e Frontend)
├── prototypes/               # Wireframes, fluxos e exports do Figma
└── landing-page/             # Página web de apresentação institucional do sistema
```

---

## Cronograma de Marcos

| Marco | Fase | Período Previsto | Status |
| :--- | :--- | :--- | :--- |
| **Marco 1** | Levantamento e Validação de Requisitos | Mar/2026 – Jul/2026 |  Concluído |
| **Marco 2** | Modelagem e Prototipação | Ago/2026 – Nov/2026 |  Em Andamento |
| **Marco 3** | Desenvolvimento do Sistema | A definir |  Pendente |
| **Marco 4** | Integração (IFC / SIPAC) e Homologação | A definir |  Pendente |
| **Marco 5** | Implantação e Encerramento | A definir |  Pendente |

---

## Equipe do Projeto

| Nome | Papel / Responsabilidade |
| :--- | :--- |
| **Hygor Marques** | Desenvolvimento & Arquitetura de Software |
| **Isadora Cozendey** | UI/UX Design & Engenharia de Software |

---

## Documentação

Toda a documentação técnica e gerencial encontra-se organizada na pasta [`/docs`](./docs):
* [Plano_de_Projeto](./docs/01-plano-projeto/plano-de-projeto.md)
* [Termo de Abertura do Projeto (TAP)](./docs/01-plano-projeto/termo_de_abertura_do_projeto.md)
* [EAP do Projeto](./docs/01-plano-projeto/eap_do_projeto.md)
* [Mapeamento de Talentos e Habilidades](./docs/01-plano-projeto/mapeamento_de_talentos_e_habilidades.md)
* [Critérios de aceitação do Projeto](./docs/01-plano-projeto/criterios_de_aceitacao.md)
* [Requisitos Funcionais e Não-Funcionais](./docs/02-requisitos/requisitos_funcionais_e_n_o_funcionais.md)
* [Regras de Negócio](./docs/02-requisitos/regras_de_negocios.md)
