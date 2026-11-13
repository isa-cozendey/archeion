[regras_de_neg_cio.md](https://github.com/user-attachments/files/34829781/regras_de_neg_cio.md)
# Regras de Negócio (RN) – Archeion

**Projeto:** Archeion (`portarias.gestao`)  
**Instituição:** Instituto Federal Catarinense (IFC) – Campus Videira  
**Versão:** 1.0  

---

## 1. Controle de Prazos e Vigências

* **RN01 - Mandato de Núcleos (CLA, CPPD, NEABI, NEGES, NGA):** O sistema não deve permitir datas de vigência que ultrapassem o limite máximo de $2$ anos.
* **RN02 - Mandato da CIS Local:** O sistema deve bloquear prazos de vigência que excedam o limite máximo de $3$ anos.
* **RN03 - Sazonalidade de Matrícula e Ingresso:** Portarias destinadas a comissões de ingresso, matrícula e validação PPI possuem data limite de vigência fixada obrigatoriamente em **julho de 2026**.
* **RN04 - Prazos de GTs e Bancas:** Grupos de trabalho e bancas avaliadoras devem possuir uma data de término obrigatória configurada para $30$, $45$ ou $60$ dias para a entrega do relatório final.
* **RN05 - Vinculação de Fiscalização de Contrato:** A vigência da portaria de fiscalização de contrato fica estritamente limitada e atrelada ao período de validade do instrumento jurídico principal localizado no SIPAC.
* **RN06 - Justificativa de Efeito Retroativo:** É obrigatório o preenchimento do campo de justificativa textual para qualquer portaria que retroaja seus efeitos (ex: localização ou interrupção de férias).

---

## 2. Restrições de Membros e Composição

* **RN07 - Impedimento de Acúmulo em Licitações (Segregação de Funções):** O sistema deve impedir que um mesmo número de SIAPE seja cadastrado simultaneamente como Agente de Contratação e Pregoeiro dentro do mesmo processo.
* **RN08 - Estrutura Mínima de Comissão:** O cadastro de qualquer comissão especial exige a definição obrigatória de ao menos um Presidente/Coordenador e um Presidente Suplente.
* **RN09 - Obrigatoriedade de Quota Discente:** Colegiados e núcleos específicos exigem a validação e preenchimento obrigatório de campos destinados a representantes discentes (alunos).

---

## 3. Contabilidade de Carga Horária (Nota Técnica 001/2023)

* **RN10 - Limite para Colegiados:** O somatório de horas semanais do servidor em portarias de Colegiados não pode ultrapassar o teto de $0,5\text{h}$ ($30$ minutos).
* **RN11 - Limite para NDEs e CPPD:** O somatório de horas semanais do servidor nestas categorias não pode ultrapassar o teto de $1\text{ hora}$.
* **RN12 - Limite para Núcleos e GTs:** O acúmulo de horas semanais deve ser travado entre $4\text{h}$ e $8\text{h}$, dependendo da função exercida (membro ou coordenação).

---

## 4. Integridade dos Dados e Modificações

* **RN13 - Bloqueio de Dados Inválidos na Origem:** Se o sistema identificar inconsistências em dados de servidores (Nome, setor, CH) antes do salvamento, o processo de criação da portaria deve ser sumariamente barrado.
* **RN14 - Imutabilidade da Portaria Original (Retificação):** Erros identificados após a publicação não alteram o documento original; o sistema deve gerar uma Retificação anexando um documento auxiliar e abrindo um histórico de modificações.
* **RN15 - Baixa Automática por Substituição:** Formulários que visam substituir servidores devem exigir o número da portaria anterior para revogá-la automaticamente no sistema, evitando duplicidade de vigência.
