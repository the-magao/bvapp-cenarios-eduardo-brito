# BVapp — Cenários de Teste Documentados | Gestão de Pessoas

**Autor:** Eduardo Brito Oliveira  
**Disciplina:** Validação e Verificação de Testes de Software (VVTS)  
**Atividade:** Especificação de cenários de teste (Aula 06 — Introdução ao TDD)

## O que é este mini projeto

Repositório individual contendo **16 cenários de teste documentais** distribuídos nos recortes **Cooperativa, Fornecedores e Relatórios**, tomando como referência o exemplo UC001 — Manter produtos. **Não contém sistema, telas, testes executáveis nem resultados de execução**: a entrega solicitou apenas a documentação e organização dos arquivos.

**Importante:** os IDs são os IDs originais dos **critérios de aceitação no OpenProject**, e não identificadores RF inventados. Regras pendentes permanecem perguntas em `docs/pendencias_stakeholders.md`. O cenário CT016 de Relatório de Usuários está explicitamente **condicionado** à criação/aprovação dos critérios de aceitação.

## Estrutura do repositório

```text
bvapp-cenarios-eduardo-brito-revisado/
├── README.md
├── .gitignore
├── functional_tests/
│   ├── cooperativa/
│   │   ├── ct001_manutencao_cooperativa_crud.md
│   │   ├── ct002_validacao_cadastro.md
│   │   └── ct003_permissoes_consulta.md
│   ├── fornecedores/
│   │   ├── ct004_manutencao_fornecedores_crud.md
│   │   ├── ct005_cnpj_duplicado.md
│   │   ├── ct006_pesquisa_filtros.md
│   │   └── ct007_alteracao_status.md
│   └── relatorios/
│       ├── ct008_relatorio_cooperados.md
│       ├── ct009_relatorio_perfis.md
│       ├── ct010_relatorio_unidades.md
│       ├── ct011_relatorio_usinas.md
│       ├── ct012_relatorio_entidades.md
│       └── ct013_exportacao_relatorios.md
└── docs/
    ├── rastreabilidade.md
    ├── pendencias_stakeholders.md
    ├── relatorio_usuarios_pendente.md
    ├── roteiro_apresentacao.md
    └── guia_migracao.md
```

## Fontes e limites

1. Planilha de walkthrough entregue pelo autor, especialmente dúvidas Q01–Q31.
2. PDF `bvapp_All_open_2026-11-05_20-50.pdf` (OpenProject, IDs de Feature, User Story e CA).
3. ZIP do backend BVapp, exclusivamente como apoio para identificar divergências; a implementação não substitui requisitos.
4. Os dois ZIPs de colegas foram usados **somente como referências de organização e formatação**, sem copiar sua autoria.

Quando existe contradição ou ausência de regra, a especificação preserva a dúvida. Em particular, endereço de fornecedor é obrigatório em #24315 e opcional em #24325. Ativar/inativar não equivale a excluir.

## Conferência

- [x] 13 cenários documentados e identificados por Eduardo Brito Oliveira
- [x] Rastreabilidade de requisitos e pendências
- [x] Fluxos e resultados esperados, sem implementação
- [x] Arquivos de manutenção com a etapa de exclusão assinalada como não especificada
- [ ] Esclarecimentos dos stakeholders e eventual complementação dos cenários CRUD
- [ ] Publicação do repositório individual no GitHub
