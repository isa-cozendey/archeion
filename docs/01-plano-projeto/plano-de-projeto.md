[plano_de_projeto.md](https://github.com/user-attachments/files/34826541/plano_de_projeto.md)
# Plano de Projeto – Archeion

**Instituição:** Instituto Federal Catarinense (IFC) – Campus Videira  
**Versão:** 1.0  
**Data de Elaboração:** Novembro de 2026  
**Responsáveis:** Hygor Marques & Isadora Cozendey  

---

## 1. Visão Geral

O projeto Archeion tem como propósito digitalizar, centralizar e automatizar o gerenciamento do ciclo de vida das portarias institucionais do IFC – Campus Videira. Atualmente, o controle manual ou descentralizado acarreta riscos de vencimento de mandatos sem substituição, inconsistências em dados cadastrais de servidores, acúmulo indevido de carga horária e retrabalho operacional entre os setores solicitantes, o Gabinete, a Coordenação de Gestão de Pessoas (CGP) e a Direção Geral (DG).

### 1.1 Objetivos
* **Centralizar** o histórico e a tramitação de todas as portarias em um único sistema institucional.
* **Automatizar** a validação de regras administrativas (prazos, carga horária conforme Nota Técnica 001/2023, segregação de funções e cotas de representação).
* **Integrar** o fluxo de dados ao **Sistema Interno de Cadastro do IFC** (validação de servidores/discentes) e ao **SIPAC** (protocolo, armazenamento e publicação oficial).
* **Garantir** rastreabilidade completa (auditoria) e segurança da informação por meio de controle de acesso baseado em papéis (RBAC).

---

## 2. Declaração de Escopo

### 2.1 O que está incluído no Escopo (In-Scope)
* **Gestão de Usuários e Acessos (RBAC):** Autenticação integrada e perfis específicos (*Diretor Geral*, *Emissor - Gabinete/CGP*, *Requerente* e *Consultor*).
* **Fluxo Completo de Tramitação:** Solicitação, triagem/análise, aprovação/reprovação, emissão, assinatura eletrônica (DG ou substituto legal) e disparo para publicação no SIPAC.
* **Motor de Regras de Negócio:** Validação automática de vigências, composição mínima de comissões, cotas discentes, limites de carga horária semanal e bloqueio de inconsistências na origem.
* **Gestão de Ciclo de Vida:** Controle de estados (*Ativa*, *Vigente*, *Retificada*, *Revogada*), histórico imutável de retificações e baixa automática em substituições.
* **Sistema de Alertas e Notificações:** Avisos proativos de vencimento de mandatos, prazos de entrega de relatórios de GTs/bancas e irregularidades de representação.
* **Módulo de Relatórios:** Relatório gerencial restrito à Diretoria, relatório de contexto individual do servidor e relatórios agrupados por categoria.
* **Documentação e Prototipação:** Especificação de requisitos, modelagem de dados, protótipo navegável e landing page institucional.

### 2.2 O que NÃO está incluído no Escopo (Out-of-Scope)
* Substituição integral do SIPAC ou do sistema institucional de cadastro de servidores.
* Alteração da estrutura interna, banco de dados ou regras nativas dos sistemas institucionais integrados.
* Gestão de contratos como finalidade principal (contratos são apenas referenciados nas portarias de fiscalização).
* Gestão acadêmica, financeira, patrimonial ou de recursos humanos além dos dados estritamente necessários às portarias.
* Disponibilização pública irrestrita de dados funcionais protegidos por sigilo/privacidade.

---

## 3. Partes Interessadas (Stakeholders)

| Stakeholder / Setor | Papel no Projeto | Interesse / Responsabilidade |
| :--- | :--- | :--- |
| **Hygor Marques** | Desenvolvedor & Arquiteto | Desenvolvimento backend/frontend, integrações de API e banco de dados. |
| **Isadora Cozendey** | UI/UX & Engenheira de Software | Levantamento de requisitos, documentação, prototipação e design de interfaces. |
| **Direção Geral (DG)** | Patrocinador / Usuário-Chave | Assinatura eletrônica das portarias, validação gerencial e acesso a relatórios sensíveis. |
| **Gabinete Institucional** | Usuário-Chave (Emissor) | Triagem, emissão, revisão e controle de tramitação das portarias. |
| **CGP** | Usuário-Chave (Emissor) | Validação de dados funcionais, carga horária e regras de pessoal. |
| **DAP e DEPE** | Consultores / Homologadores | Apoio na validação de regras específicas de ensino, pesquisa, extensão e administração. |
| **Servidores e Discentes** | Usuários Finais (Requerentes) | Solicitação de portarias e consulta de documentos vinculados ao seu perfil. |

---

## 4. Cronograma de Marcos (Milestones)

O desenvolvimento está estruturado em 5 grandes marcos evolutivos:

| Marco | Entrega Principal | Período Previsto | Critério de Conclusão |
| :--- | :--- | :--- | :--- |
| **Marco 1** | Levantamento e Validação de Requisitos | Mar/2026 – Jul/2026 | TAP, Requisitos (RF/RNF) e Regras de Negócio aprovados. |
| **Marco 2** | Modelagem e Prototipação | Ago/2026 – Nov/2026 | Arquitetura, DER, fluxos e protótipo navegável validados. |
| **Marco 3** | Desenvolvimento do Sistema | A definir | Módulos principais codificados e testados unitariamente. |
| **Marco 4** | Integração e Homologação | A definir | Integração com IFC/SIPAC funcional e homologada pelos usuários-chave. |
| **Marco 5** | Implantação e Encerramento | A definir | Deploy em produção, treinamento, entrega da documentação e aceite final. |

---

## 5. Gestão de Riscos

Abaixo estão mapeados os principais riscos identificados para o projeto e suas respectivas estratégias de resposta:

| ID | Descrição do Risco | Probabilidade | Impacto | Estratégia de Mitigação / Contingência |
| :--- | :--- | :--- | :--- | :--- |
| **RSK-01** | Indisponibilidade ou demora na liberação das APIs de integração com o SIPAC ou Sistema Interno do IFC. | Média | Alto | Desenvolver camadas de abstração (Mock Services/Adapters) para não travar o desenvolvimento do core e validar contratos de dados antecipadamente. |
| **RSK-02** | Mudanças em normativas institucionais (ex: alteração de tetos de carga horária ou novas categorias de portaria). | Média | Médio | Parametrizar limites de horas, prazos e categorias diretamente no banco de dados (painel administrativo), evitando regras fixas no código (*hardcoded*). |
| **RSK-03** | Vazamento ou acesso indevido a relatórios sensíveis da Diretoria. | Baixa | Alto | Implementar criptografia em repouso/trânsito, controle rigoroso de RBAC no backend e trilhas de auditoria para todas as consultas. |
| **RSK-04** | Resistência dos usuários na adoção do novo fluxo digital em relação ao processo atual. | Baixa | Médio | Envolver Gabinete, CGP e DG desde a fase de prototipação (UX centrada no usuário) e realizar treinamento prático antes da implantação. |
| **RSK-05** | Inconsistência nos dados legados importados da base institucional. | Média | Médio | Aplicar camada obrigatória de sanidade e validação de dados (RNF03 / RN13) antes da persistência de qualquer portaria. |

---

## 6. Plano de Qualidade e Testes

A qualidade do software será assegurada por meio de práticas contínuas durante todo o ciclo de desenvolvimento:
* **Padrões de Código e Revisão:** Uso de controle de versão via Git/GitHub com revisão de *Pull Requests* antes da integração na branch principal.
* **Conformidade Visual:** Garantia de que os documentos gerados sigam rigorosamente o padrão visual oficial dos boletins anuais do IFC (RNF04).
* **Níveis de Teste:**
  1. *Testes Unitários:* Validação isolada das regras de negócio (cálculo de carga horária, prazos e bloqueios).
  2. *Testes de Integração:* Verificação da comunicação e troca de dados com o cadastro interno do IFC e o SIPAC.
  3. *Testes de Homologação (UAT):* Execução de cenários reais junto aos servidores do Gabinete, CGP e Direção Geral antes da entrada em produção.
