# 📌 Requisitos Funcionais e Não-Funcionais – Archeion

**Projeto:** Archeion (`portarias.gestao`)  
**Instituição:** Instituto Federal Catarinense (IFC) – Campus Videira  
**Versão:** 1.0  

---

## 1. Requisitos Funcionais (RF)

### 1.1 Gestão de Acessos e Perfis

* **RF01 - Autenticação de Usuários:** Permitir o login de todos os usuários (servidores docentes, técnicos e alunos) baseando-se no sistema interno do IFC.
* **RF02 - Controle de Permissões por Papel (RBAC):**
  * **Diretor Geral (DG):** Nível máximo. Assina portarias e acessa relatórios sensíveis.
  * **Emissor (Gabinete e CGP):** Permissão para cadastrar, editar, validar e tramitar as portarias.
  * **Requerente (Servidores/Geral):** Pode solicitar portarias e consultar documentos associados ao seu perfil.
  * **Consultor:** Consulta das informações autorizadas.

### 1.2 Ciclo de Vida da Portaria (O Fluxo Principal)

* **RF03 - Solicitação de Portaria:** O Requerente solicita a criação inserindo justificativa, objetivo, informações voláteis e processos associados.
* **RF04 - Triagem e Emissão:** O Emissor (Gabinete ou CGP) revisa a solicitação, podendo **aprovar** ou **reprovar**.
* **RF05 - Assinatura Eletrônica:** Uma vez aprovada, a portaria é enviada para a fila do Diretor Geral (DG) ou substituto legal para assinatura.
* **RF06 - Integração de Publicação:** Após a assinatura do DG, o sistema deve disparar automaticamente o documento para publicação no **SIPAC**.

### 1.3 Cadastro e Validações no Formulário

* **RF07 - Preenchimento Automatizado de Dados:** Na criação de uma portaria, os dados do servidor (Nome, SIAPE, Setor, CH) devem ser puxados dinamicamente do sistema interno do IFC para evitar erros humanos.
* **RF08 - Tratamento de Retificações e Revogações:**
  * Se for uma **Retificação**, o sistema deve exigir um documento auxiliar e manter o histórico de alterações.
  * Se for uma **Revogação/Substituição**, o formulário deve exigir obrigatoriamente o número da portaria anterior para dar baixa automática na antiga.
* **RF09 - Gestão Dinâmica de Categorias:** Permitir que o Gabinete/CGP cadastre novas categorias de portaria caso a demanda não se enquadre nas padrões (*Fiscalização*, *Lotação*, *Normalização*, *Pessoal*, *Comissões/GT*, *Retificação*).

### 1.4 Automação de Alertas

* **RF10 - Alertas de Vencimento de Mandato:** Emitir alertas prioritários antes do vencimento de mandatos coletivos ($2$ e $3$ anos) e comissões sazonais.
* **RF11 - Alerta de Entrega de Relatórios:** Cobrar automaticamente o envio do relatório final para GTs e bancas (prazos de $30$ a $60$ dias).
* **RF12 - Alerta de Irregularidade por Vencimento:** Caso uma portaria vença sem substituto, gerar alerta imediato de "irregularidade de representação" e "pendência de substituição".

### 1.5 Relatórios e Visões

* **RF13 - Relatório da Diretoria (Acesso Restrito ao DG):** Consolidação de dados sensíveis sobre servidores, contratos, carga horária acumulada e vigências gerais.
* **RF14 - Relatório de Contexto do Servidor:** Permite ao servidor logado extrair um panorama geral de suas próprias portarias, detalhando sua carga horária empenhada, setores e categorias.
* **RF15 - Relatório por Categorias:** Agrupamento e compilação de todas as portarias pertencentes a uma categoria específica.

---

## 2. Requisitos Não-Funcionais (RNF)

* **RNF01 - Integrações de Sistemas (API/Middleware):**
  * O sistema **deve** se integrar ao **SIPAC** para armazenamento, protocolo e publicação de documentos oficiais.
  * O sistema **deve** se integrar ao **Sistema Interno de Cadastro do IFC** para sincronização centralizada de servidores, discentes e estruturas organizacionais.
* **RNF02 - Segurança e Privacidade de Dados:** O relatório da diretoria contém dados sensíveis e deve possuir controle estrito de criptografia e restrição de acesso em nível de banco de dados (apenas para o papel DG).
* **RNF03 - Validação Antecipada (Sanidade dos Dados):** Todos os dados vindos de bases externas (Nome, setor, carga horária) precisam passar por uma camada de validação e consistência antes de persistidos em uma nova portaria.
* **RNF04 - Padronização Visual (Boletins Oficiais):** A geração e exibição das portarias deve seguir rigorosamente o padrão visual público estabelecido nos boletins anuais da instituição.

---

## 3. Estados da Portaria no Sistema

| Estado | Descrição |
| :--- | :--- |
| `Ativa` | Cadastrada / Em fluxo de assinatura. |
| `Vigente` | Assinada, publicada e dentro do prazo de validade. |
| `Retificada` | Alterada por documento auxiliar com histórico preservado. |
| `Revogada` | Substituída ou encerrada por ato posterior. |