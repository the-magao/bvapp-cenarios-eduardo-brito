# Matriz de rastreabilidade — projeto revisado

Todos os cenários são documentais. Os IDs a seguir identificam **critérios/Features no OpenProject**, não códigos de testes executados.

| Cenário | Área | Feature(s) | CAs principais | Fonte anterior |
|---|---|---|---|---|
| CT001 | Cooperativa | #24058, #24059, #24060 | #24098–#24101, #24106–#24108, #24117–#24126 | CT001, CT003, CT004 |
| CT002 | Cooperativa | #24058 | #24098–#24099 | CT002 |
| CT003 | Cooperativa | #24059 | #24106–#24108 | CT003 |
| CT004 | Fornecedores | #24306, #24308, #24309 | #24315–#24335, #24364–#24366, #24358–#24360 | CT005, CT007, CT008 |
| CT005 | Fornecedores | #24306 | #24335 | CT006 |
| CT006 | Fornecedores | #24308 | #24364–#24366 | CT007 |
| CT007 | Fornecedores | #24310 | #24350–#24351 | CT009 |
| CT008 | Relatórios | Conforme PDF/planilha | #23808–#23826 | CT010 |
| CT009 | Relatórios | Conforme PDF/planilha | #23837–#23846 | CT011 |
| CT010 | Relatórios | Conforme PDF/planilha | #23858–#23867 | CT012 |
| CT011 | Relatórios | Conforme PDF/planilha | #23891–#23895 | CT013 |
| CT012 | Relatórios | Conforme PDF/planilha | #23912–#23917 | CT014 |
| CT013 | Relatórios | Conforme PDF/planilha | #23825, #23844, #23866, #23894, #23916 | CT015 |

**Não contado entre os 13 cenários:** antigo CT016, Relatório de Usuários (Feature #27052, US #27053): não possui CAs suficientes. Mantido em `docs/relatorio_usuarios_pendente.md`.

**Exclusão:** CT001 e CT004 reúnem as quatro posições do fluxo CRUD para atender à estrutura da aula, mas o passo de excluir está **pendente de requisitos**, não descrito como funcionalidade efetiva. Não afirmar CRUD integralmente testável antes da decisão.
