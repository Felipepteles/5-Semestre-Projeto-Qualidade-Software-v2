# Aula 15 – Modelos de Maturidade no Processo de Desenvolvimento

## 👥 Integrantes

- Felipe Teles

---

## 1. Diagnóstico de Maturidade

Abaixo está a avaliação do processo atual da equipe no desenvolvimento do sistema LocalEats, considerando as práticas de planejamento, execução e monitoramento.

| Critério | Sim | Parcial | Não |
| :--- | :---: | :---: | :---: |
| Os requisitos são documentados? | | X | |
| Existe controle de mudanças? | | X | |
| Há atividades de teste definidas? | X | | |
| Os defeitos são registrados? | | X | |
| O processo de desenvolvimento é conhecido por toda a equipe? | X | | |
| As tarefas são planejadas e acompanhadas regularmente? | X | | |
| Existe padronização para implementação de funcionalidades? | X | | |
| Os testes são executados antes da entrega das funcionalidades? | X | | |
| Há revisão de código ou validação por outro integrante da equipe? | X | | |
| A equipe utiliza ferramentas para gerenciamento das atividades? | X | | |
| Os artefatos do projeto (requisitos, testes, código) são organizados e versionados? | X | | |
| Existe rastreabilidade entre requisitos e funcionalidades implementadas? | | X | |
| A equipe realiza reuniões ou momentos de retrospectiva para identificar melhorias? | | X | |
| Existem indicadores ou métricas para acompanhar a qualidade do projeto? | | | X |

### Nível de maturidade estimado

**Classificação: CMMI - Nível 2 (Gerenciado)**

### Justificativa

Os projetos são devidamente planejados, medidos e controlados em sua essência. Utilizo ferramentas (Trello e GitHub) para organizar tarefas e versionar artefatos. No entanto, o processo ainda não alcança o Nível 3 (Definido), visto que falta uma padronização formal em toda a organização do projeto, não possuí rastreabilidade rigorosa entre as mudanças de requisitos e o código, e há total ausência de métricas quantitativas de qualidade para embasar decisões de melhoria.

---

## 2. Lacunas Identificadas

Com base no diagnóstico, identificamos três pontos críticos que dificultam a evolução do processo atual:

| Lacuna | Impacto no Processo e Produto |
| :--- | :--- |
| **1. Falta de integração contínua (CI)** | A execução de testes e linting depende de ação manual do desenvolvedor. Isso aumenta o risco de falhas humanas e permite que código defeituoso chegue à branch principal. |
| **2. Ausência de métricas de qualidade** | Sem ferramentas que meçam a cobertura de testes ou densidade de bugs, a equipe não consegue afirmar quantitativamente se a estabilidade do LocalEats está melhorando ou piorando. |
| **3. Rastreabilidade parcial entre tarefas e código** | Alterações no código nem sempre são vinculadas aos cards originais do Trello. Isso dificulta o controle de mudanças e o entendimento do motivo de certas implementações no longo prazo. |

---

## 3. Propostas de Melhoria

Para que o processo da equipe evolua para o Nível 3 (Definido), propomos as seguintes ações práticas:

| Melhoria Proposta | Benefício Esperado |
| :--- | :--- |
| **1. Configurar GitHub Actions (CI/CD)** | Automatizar a execução dos testes e validações a cada Pull Request criado. O benefício é barrar falhas antes da revisão de código, aumentando a confiabilidade da entrega. |
| **2. Adotar ferramentas de análise estática** | Implementar relatórios de cobertura do framework de testes (ex: Jest). Isso fornecerá os indicadores numéricos necessários para monitorar a saúde e a qualidade do projeto. |
| **3. Padronizar commits e Pull Requests** | Exigir o uso de *templates* no GitHub e a marcação do ID da tarefa do Trello em todo commit. Isso garantirá rastreabilidade total entre o que foi pedido no requisito e o que foi implementado no sistema. |

---

## Conclusão

Embora o processo atual garanta entregas funcionais e organizadas (Nível 2), a adoção das melhorias propostas focadas em automação e métricas será fundamental para mitigar falhas. Compreender a nossa própria maturidade nos permite enxergar que a qualidade do LocalEats depende diretamente de evoluirmos de um modelo apenas "gerenciado" para um processo formalmente "definido" e medido.