# Roteiro de apresentação — cerca de 5 minutos

**Autor: Eduardo Brito Oliveira.**

**0:00–0:40 | Contexto.** BVapp, módulo Gestão de Pessoas, recortes Cooperativa, Fornecedores e Relatórios. A tarefa é **documentar**, não implementar nem executar testes.

**0:40–1:25 | Estrutura.** Mostrar `README.md`, `functional_tests/` (13 arquivos, separados por área), `docs/rastreabilidade.md` e `docs/pendencias_stakeholders.md`.

**1:25–3:10 | Cenário demonstrado.** Abrir `functional_tests/fornecedores/ct004_manutencao_fornecedores_crud.md`. Explicar criar, consultar, atualizar e **exclusão pendente**. Mostrar um fluxo alternativo: CNPJ duplicado e a contradição do endereço obrigatório/opcional.

**3:10–4:15 | Exemplo verificável.** Abrir `ct005_cnpj_duplicado.md` e mostrar entrada de CNPJ repetido, resultado esperado (impedir cadastro) e dúvida sobre normalização/inativos.

**4:15–5:00 | Rastreabilidade e conclusão.** Mostrar os IDs do OpenProject e justificar por que `relatorio_usuarios_pendente.md` não foi contado como cenário testável. Explicar que a documentação será refinada após validação dos stakeholders.
