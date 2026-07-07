# Aula 16 - Qualidade em Metodologias Ágeis

## Integrante

- Felipe Teles

---

# 1. Análise de Práticas Ágeis no Processo

| Prática | Existe no processo? | Como é aplicada atualmente? | Pode ser melhorada? |
| :--- | :--- | :--- | :--- |
| Planejamento iterativo | Parcial | A gente faz por ciclos mais informais, pegando o que ta mais urgente na lista. | Criar Sprints com tempo fixo pra ajudar a prever as entregas. |
| Priorizacao de funcionalidades | Sim | As tarefas ficam em ordem no Trello, de cima pra baixo. | Organizar pensando no que da mais valor pro usuario final e nao so urgencia. |
| Entregas incrementais | Sim | A gente sobe as coisas novas direto na branch principal e ja vai pro Vercel. | Quebrar as tarefas grandes em pedacos menores pra subir mais rapido. |
| Feedback frequente | Nao | Como eu to fazendo mais sozinho, acabo nao validando toda hora. | Testar e validar logo depois de fazer um pedaco pequeno de codigo. |
| Trabalho colaborativo | Parcial | Uso o GitHub pra controlar as versoes e salvar o codigo. | Fazer Pull Requests direitinho no GitHub pra ficar o historico salvo. |
| Controle visual das atividades | Sim | Uso um quadro estilo Kanban no Trello, passando os cards pro Done. | Colocar um limite de coisas fazendo ao mesmo tempo pra nao acumular tarefa pela metade. |
| Melhoria contínua | Parcial | A gente so muda algo quando da um erro muito grande ou tem que refazer muita coisa. | Parar pra analisar o que melhorar sempre que terminar uma entrega. |

### Conclusão

O processo atual ate que tem uma base agil legal, principalmente na parte de ver as tarefas no Kanban e subir as coisas picadas na web. Mas falta medir as coisas e ter uns limites melhores. O ideal é parar de so reagir aos problemas e focar em melhorar sempre, limitando o tanto de coisa que a gente faz ao mesmo tempo pra nao perder o controle da qualidade.

---

# 2. Propostas de Melhoria Ágil

| Melhoria Proposta | Metodologia Relacionada | Benefício Esperado |
| :--- | :--- | :--- |
| Colocar limite de tarefas em andamento (WIP) | Kanba | Evitar gargalo e nao ficar com um monte de coisa comecada e nada terminado. |
| Fazer testes automaticos antes de subir o codigo | XP | Dar mais seguranca nas entregas rodando teste sempre que mandar codigo novo. |
| Fazer mini retrospectivas | Scru | Separar um tempinho depois de entregar algo pra ver o que deu certo e o que melhorar pro proximo. |
| Cortar os desperdicios de tempo | Lea | Nao ficar fazendo codigo ou funcao que ninguem pediu agora, focando so no que importa. |

---

# 3. Definition of Ready (DoR)

Uma funcionalidade estara pronta para desenvolvimento quando:

1. O requisito tem os criterios de aceitacao bem definidos na tarefa.
2. A regra principal ta clara e nao tem duvida sobre o que e pra fazer.
3. Ja vi se vai precisar alterar banco de dados ou criar rota nova.
4. O desenho ou tela de como vai ficar ja ta anexado no card.
5. A tarefa não é muito gigante, da pra terminar num ciclo de trabalho so.

---

# 4. Definition of Done (DoD)

Uma funcionalidade sera considerada concluida quando:

1. Os criterios de aceitacao que a gente definiu foram todos compridos.
2. O codigo ta pronto e rodando liso sem erro de sintaxe.
3. Os testes foram feitos e nao deu nenhum bug aparente.
4. O codigo ja foi pro GitHub bonitinho.
5. A funcionalidade ja ta na branch main e subiu na Vercel funcionando perfeitamente.