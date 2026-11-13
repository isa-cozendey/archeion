# Termo de Abertura do Projeto (TAP)

**Título do Projeto:** Archeion
**Instituição:** Instituto Federal Catarinense (IFC) – Campus Videira  

---

## 1. Necessidade de Negócio / Objetivos do Projeto

Desenvolver um sistema para digitalizar, centralizar e controlar o ciclo de vida das portarias institucionais, desde a solicitação até a assinatura, publicação, vigência, acompanhamento, vencimento, retificação, revogação e arquivamento.

### Objetivos Específicos
* Centralizar as informações das portarias;
* Reduzir erros de elaboração e cadastro;
* Automatizar validações;
* Controlar vigências;
* Garantir rastreabilidade;
* Emitir alertas;
* Integrar dados com os sistemas institucionais;
* Facilitar consultas e relatórios;
* Reduzir riscos de vencimento ou ausência de atos administrativos vigentes.

---

## 2. Requisitos do Projeto (Visão de Alto Nível)

* Permitir que servidores cadastrados no sistema interno do IFC solicitem a criação de portarias.
* Permitir diferentes níveis de acesso, conforme o perfil do usuário:
  * **DG (Diretor Geral):** nível máximo, incluindo assinatura das portarias;
  * **Emissor (Gabinete / CGP):** cadastro, edição, análise e gerenciamento das portarias;
  * **Requerente:** solicitação e consulta das portarias relacionadas às suas demandas;
  * **Consultor:** consulta das informações autorizadas.
* Integrar-se ao sistema interno de cadastro do IFC para obtenção e validação de dados dos servidores.
* Integrar-se ao SIPAC para armazenamento, protocolo e publicação dos documentos oficiais.
* Validar nome, SIAPE, setor, carga horária e demais dados dos servidores antes da inclusão em uma portaria.
* Permitir associação de uma portaria a um ou mais memorandos e processos.
* Permitir cadastro de identificador único, cabeçalho, corpo, objetivo, justificativa, status, datas de emissão, publicação e validade.
* Permitir cadastro e gerenciamento de categorias de portarias, contemplando inicialmente:
  * Fiscalização de Contrato;
  * Localização/Lotação;
  * Ato de Normalização;
  * Pessoal;
  * Comissões e Grupos de Trabalho;
  * Retificação.
* Permitir criação de novas categorias pelo setor responsável.
* Implementar fluxo de solicitação, análise, aprovação/reprovação, emissão, assinatura e publicação.
* Permitir assinatura por usuários com papel DG, incluindo substitutos autorizados.
* Controlar os estados: **Ativa**, **Vigente**, **Retificada** e **Revogada**.
* Controlar vigência e ciclo de vida das portarias.
* Implementar regras de duração para mandatos, comissões, núcleos, GTs e bancas.
* Controlar portarias com efeito retroativo, exigindo justificativa.
* Validar composição das comissões e grupos de trabalho.
* Implementar regras de segregação de funções.
* Validar cotas e representações obrigatórias, quando aplicáveis.
* Validar existência de Presidente/Coordenador e Presidente Suplente nas comissões que exigirem esses papéis.
* Controlar carga horária atribuída aos servidores conforme as regras institucionais.
* Exigir número da portaria anterior em processos de substituição ou revogação.
* Registrar motivos e referências em processos de desentranhamento.
* Permitir vinculação ao processo individual e ao Edital nº 68/2024 nos casos relacionados ao PGD.
* Gerar alertas de vencimento, irregularidade de representação, necessidade de substituição e encerramento de atividades.
* Gerar relatórios gerenciais e individuais conforme o nível de autorização.
* Garantir controle de acesso e proteção das informações administrativas e funcionais sensíveis.

---

## 3. Descrição do Produto / Entregas

* **Sistema Archeion:** destinado ao gerenciamento do ciclo de vida das portarias do IFC – Campus Videira.
* **Módulo de autenticação e usuários:** integração com o cadastro institucional do IFC e gerenciamento de perfis e permissões.
* **Módulo de solicitação:** permite aos servidores solicitar a elaboração de uma nova portaria e informar justificativa, objetivo, participantes, informações específicas e processos relacionados.
* **Módulo de emissão:** permite ao Gabinete e ao CGP analisar solicitações aprovadas, cadastrar e editar portarias.
* **Módulo de composição:** permite selecionar servidores a partir dos dados institucionais e validar sua participação, função, setor e carga horária.
* **Módulo de validação:** aplica regras de vigência, composição, carga horária, segregação de funções, representação e demais regras administrativas.
* **Módulo de assinatura:** encaminha a portaria para usuários autorizados da DG realizarem a assinatura.
* **Integração com SIPAC:** permite encaminhamento e relacionamento dos documentos oficiais com o sistema institucional.
* **Controle de vigência:** acompanha datas de início e término e regras específicas de cada categoria de portaria.
* **Controle de ciclo de vida:** acompanha portarias ativas, vigentes, retificadas e revogadas, mantendo histórico e rastreabilidade.
* **Módulo de retificação e revogação:** registra portarias anteriores, documentos auxiliares e histórico das alterações.
* **Módulo de alertas:** emite notificações relacionadas a vencimentos, substituições, encerramento de GTs, mandatos e demais eventos relevantes.
* **Módulo de relatórios:** disponibiliza relatório gerencial da Diretoria, relatório de contexto do servidor e relatórios específicos por categoria de portaria, respeitando as permissões de acesso.
* **Auditoria e rastreabilidade:** registra ações, alterações, aprovações, reprovações, assinaturas, relacionamentos e demais eventos relevantes.
* **Documentação:** documentação técnica e funcional do sistema, incluindo regras de negócio e procedimentos de utilização.
* **Testes e implantação:** realização de testes funcionais e de integração, homologação pelos usuários responsáveis e implantação da solução.

---

## 4. Exclusões de Escopo (O Projeto Não Inclui)

* Substituição integral do SIPAC ou do sistema institucional de cadastro de servidores.
* Alteração da estrutura ou das regras internas dos sistemas institucionais integrados.
* Gestão de documentos institucionais que não estejam relacionados ao ciclo de vida das portarias.
* Criação ou alteração de regras administrativas oficiais sem validação e autorização institucional.
* Disponibilização pública irrestrita de dados funcionais ou administrativos protegidos.
* Alteração dos procedimentos formais de assinatura e publicação definidos pela instituição.
* Gestão de contratos como finalidade principal; os contratos serão utilizados como referência quando necessários às portarias de fiscalização.
* Gestão acadêmica, financeira, patrimonial ou de recursos humanos além das informações necessárias ao gerenciamento das portarias.

---

## 5. Recursos Alocados

* Equipe de desenvolvimento de software.
* Responsáveis do Gabinete Institucional.
* Direção Geral.
* CGP.
* Representantes da DAP e DEPE, quando necessário.
* Servidores responsáveis pela homologação e validação das regras de negócio.
* Infraestrutura computacional e banco de dados institucional.
* Ambiente de desenvolvimento, testes e produção.
* Acesso às APIs, serviços ou mecanismos de integração disponibilizados pelo sistema interno do IFC e pelo SIPAC.
* Documentação institucional, boletins e modelos de portarias utilizados como referência.
* Dados necessários para testes e validação, respeitando as políticas institucionais de segurança e privacidade.

---

## 6. Lista de Partes Interessadas

| Nome | Título | Função |
| :--- | :--- | :--- |
| **Hygor Marques** | — | Desenvolvedor |
| **Isadora Cozendey** | — | UI/UX |

---

## 7. Cronograma de Marcos do Projeto

| Marco | Período Previsto | Descrição / Entregas |
| :--- | :--- | :--- |
| **Marco 1:** Levantamento e validação de requisitos | Março/2026 a Julho/2026 | Levantamento detalhado dos processos atuais, regras de negócio, categorias, perfis, integrações e requisitos funcionais e não funcionais. |
| **Marco 2:** Modelagem e prototipação | Agosto/2026 a Novembro/2026 | Definição da arquitetura, banco de dados, fluxos, interfaces, permissões e protótipos do sistema. |
| **Marco 3:** Desenvolvimento do sistema | A definir | Implementação dos módulos de usuários, solicitações, emissão, validações, vigência, assinatura, alertas e relatórios. |
| **Marco 4:** Integração e homologação | A definir | Integração com o sistema interno do IFC e SIPAC, realização de testes e homologação junto aos usuários-chave. |
| **Marco 5:** Implantação e encerramento | A definir | Publicação do sistema em ambiente de produção, treinamento dos usuários, entrega da documentação e encerramento do projeto. |

---

## 8. Considerações do Projeto (Observações)

### Estabilidade e Testes
* O sistema deverá permitir o fluxo completo de solicitação, análise, aprovação, emissão, assinatura e encaminhamento para publicação.
* Os dados dos servidores deverão ser obtidos e validados por fonte institucional.
* As regras de vigência, composição, carga horária e impedimentos deverão ser aplicadas conforme os requisitos definidos pelo IFC.
* As permissões deverão impedir o acesso não autorizado a informações sensíveis.
* As alterações e ações relevantes deverão possuir rastreabilidade.
* Os relatórios deverão apresentar informações compatíveis com o perfil do usuário.
* As integrações previstas deverão ser testadas e homologadas.
