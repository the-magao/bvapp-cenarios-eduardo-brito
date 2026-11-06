# BVapp — Cenários de Teste | Gestão de Pessoas

**Autor:** Eduardo Brito Oliveira  
**Disciplina:** Validação e Verificação de Testes de Software (VVTS)  
**Atividade:** Especificação de Cenários de Teste — Aula 06 (Introdução ao TDD)  
**Projeto:** BVapp — Sistema de Gerenciamento de Cooperativa de Energia Solar

## 1. Sobre o projeto

Este repositório contém a documentação de **13 cenários de teste funcionais** relacionados ao módulo de Gestão de Pessoas do BVapp, com foco nas funcionalidades de **Cooperativa, Fornecedores e Relatórios**.

A atividade tem como objetivo especificar cenários de teste a partir dos requisitos funcionais analisados na atividade anterior de verificação estática de requisitos (walkthrough).

Os cenários seguem como referência o exemplo **UC001 — Manter produtos**, apresentado na Aula 06, contemplando:

- Identificador e título;
- Objetivo;
- Requisitos relacionados;
- Ator;
- Pré-condições;
- Fluxo principal;
- Fluxos alternativos;
- Regras de negócio;
- Dados de teste e resultados esperados;
- Identificação da autoria.

**Observação:** O projeto é exclusivamente documental. Não foram implementados ou executados testes automatizados, interfaces ou funcionalidades do sistema.

## 2. Cenários de teste

Foram documentados 13 cenários, distribuídos entre três áreas do BVapp.

### Cooperativa

| ID | Cenário |
|---|---|
| CT001 | Manutenção da Cooperativa (CRUD com exclusão pendente) |
| CT002 | Validação dos campos obrigatórios no cadastro |
| CT003 | Controle de permissões na consulta |

### Fornecedores

| ID | Cenário |
|---|---|
| CT004 | Manutenção de Fornecedores (CRUD com exclusão pendente) |
| CT005 | Impedimento de CNPJ duplicado |
| CT006 | Consulta, pesquisa e filtros de fornecedores |
| CT007 | Alteração de status de fornecedor |

### Relatórios

| ID | Cenário |
|---|---|
| CT008 | Relatório de Cooperados |
| CT009 | Relatório de Perfis e Permissões |
| CT010 | Relatório de Unidades Consumidoras |
| CT011 | Relatório de Usinas |
| CT012 | Relatório de Entidades Externas |
| CT013 | Exportação de relatórios em PDF ou CSV |

**Total: 13 cenários documentados.**

## 3. Estrutura do repositório

```text
bvapp-cenarios-eduardo-brito/
│
├── README.md
├── .gitignore
├── pyproject.toml
│
├── functional_tests/
│   ├── cooperativa/
│   │   ├── ct001_manutencao_cooperativa_crud.md
│   │   ├── ct002_validacao_cadastro.md
│   │   └── ct003_permissoes_consulta.md
│   │
│   ├── fornecedores/
│   │   ├── ct004_manutencao_fornecedores_crud.md
│   │   ├── ct005_cnpj_duplicado.md
│   │   ├── ct006_pesquisa_filtros.md
│   │   └── ct007_alteracao_status.md
│   │
│   └── relatorios/
│       ├── ct008_relatorio_cooperados.md
│       ├── ct009_relatorio_perfis.md
│       ├── ct010_relatorio_unidades.md
│       ├── ct011_relatorio_usinas.md
│       ├── ct012_relatorio_entidades.md
│       └── ct013_exportacao_relatorios.md
│
└── docs/
    ├── rastreabilidade.md
    ├── pendencias_stakeholders.md
    ├── relatorio_usuarios_pendente.md
    └── roteiro_apresentacao.md
```

## 4. Metodologia

Os cenários foram elaborados com base nos requisitos funcionais e critérios de aceitação registrados no OpenProject, considerando as revisões propostas na atividade de walkthrough.

A especificação contempla fluxos principais, alternativos e condições de validação.

Nos cenários de manutenção de Cooperativa e Fornecedores, foram agrupadas as operações de criação, consulta e atualização.

A operação de **exclusão permanece pendente de especificação**, pois os requisitos analisados não definem seu comportamento.

A alteração de status para inativo não foi considerada equivalente à exclusão de um registro.

## 5. Rastreabilidade dos requisitos

Cada cenário identifica os requisitos relacionados por meio dos IDs registrados no OpenProject, permitindo relacionar:

**Requisito funcional → Critério de aceitação → Cenário de teste**

A documentação de rastreabilidade está disponível em:

`docs/rastreabilidade.md`

## 6. Pendências de validação

Durante a análise dos requisitos, foram identificadas regras incompletas, ambiguidades e contradições que dependem de esclarecimento dos stakeholders.

Entre elas:

- Divergência sobre a obrigatoriedade do endereço do fornecedor;
- Ausência de regras de