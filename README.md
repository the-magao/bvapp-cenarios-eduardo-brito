# BVapp — Cenários de Teste Documentados | Gestão de Pessoas

**Autor:** Eduardo Brito Oliveira  
**Disciplina:** Validação e Verificação de Testes de Software (VVTS)  
**Atividade:** Especificação de cenários de teste (Aula 06 — Introdução ao TDD)

## O que é este mini projeto

Repositório individual contendo **16 cenários de teste documentais** distribuídos nos recortes **Cooperativa, Fornecedores e Relatórios**, tomando como referência o exemplo UC001 — Manter produtos. **Não contém sistema, telas, testes executáveis nem resultados de execução**: a entrega solicitou apenas a documentação e organização dos arquivos.

As fontes foram: (1) planilha `Eduardo_Brito_Oliveira_-_BVapp-walkthrough-requisitos-funcionais_.xlsx` (checklist, revisões e Q01–Q31); (2) PDF OpenProject `bvapp_All_open_2026-11-05_20-50.pdf`; (3) ZIP do backend BVapp para identificar divergências entre implementação e especificação; (4) ZIP do colega apenas como inspiração de estrutura, **sem reutilização de autoria ou de conteúdo**.

**Importante:** os IDs são os IDs originais dos **critérios de aceitação no OpenProject**, e não identificadores RF inventados. Regras pendentes permanecem perguntas em `docs/pendencias_stakeholders.md`. O cenário CT016 de Relatório de Usuários está explicitamente **condicionado** à criação/aprovação dos critérios de aceitação.

## Estrutura

```text
bvapp-cenarios-eduardo-brito/
├── README.md
├── .gitignore
├── pyproject.toml
├── cooperativa/scenarios/        # CT001–CT004
├── fornecedores/scenarios/       # CT005–CT009
├── relatorios/scenarios/         # CT010–CT016
└── docs/
    ├── pendencias_stakeholders.md
    ├── rastreabilidade.md
    └── roteiro_apresentacao.md
```

Não há dependências de execução. Python é uma referência organizacional; todos os cenários são arquivos Markdown independentes, facilmente transferíveis para testes Python/Django quando os requisitos forem validados.

## Índice de cenários

| Código | Recorte | Cenário | Critérios relacionados |
|---|---|---|---|
| CT001 | Cooperativa | [Inclusão de dados obrigatórios e opcionais da cooperativa](cooperativa/scenarios/ct001_inclusao_de_dados_obrigatorios_e_opcionais_da_cooperativa.md) | #24098 CA01; #24099 CA02; #24100 CA03 |
| CT002 | Cooperativa | [Bloqueio de inclusão com campos obrigatórios ausentes](cooperativa/scenarios/ct002_bloqueio_de_inclusao_com_campos_obrigatorios_ausentes.md) | #24098 CA01; #24099 CA02 |
| CT003 | Cooperativa | [Consulta dos dados cadastrais e controle de acesso](cooperativa/scenarios/ct003_consulta_dos_dados_cadastrais_e_controle_de_acesso.md) | #24106 CA01; #24107 CA02; #24108 CA03 |
| CT004 | Cooperativa | [Atualização de dados obrigatórios e rastreabilidade](cooperativa/scenarios/ct004_atualizacao_de_dados_obrigatorios_e_rastreabilidade.md) | #24117 CA01; #24119 CA02; #24123 CA03; #24125 CA04; #24126 CA05 |
| CT005 | Fornecedores | [Inclusão de fornecedor e campos de cadastro](fornecedores/scenarios/ct005_inclusao_de_fornecedor_e_campos_de_cadastro.md) | #24315 CA01; #24322 CA02; #24325 CA03 |
| CT006 | Fornecedores | [Impedimento de CNPJ duplicado no cadastro](fornecedores/scenarios/ct006_impedimento_de_cnpj_duplicado_no_cadastro.md) | #24335 CA04; #24315 CA01 |
| CT007 | Fornecedores | [Consulta, pesquisa e filtro de fornecedores](fornecedores/scenarios/ct007_consulta_pesquisa_e_filtro_de_fornecedores.md) | #24364 CA01; #24365 CA02; #24366 CA03 |
| CT008 | Fornecedores | [Atualização do fornecedor e proteção dos campos obrigatórios](fornecedores/scenarios/ct008_atualizacao_do_fornecedor_e_protecao_dos_campos_obrigatorios.md) | #24358 CA01; #24359 CA02; #24360 CA03 |
| CT009 | Fornecedores | [Alteração de status e registro de data](fornecedores/scenarios/ct009_alteracao_de_status_e_registro_de_data.md) | #24350 CA01; #24351 CA02 |
| CT010 | Relatorios | [Relatório de cooperados com filtros e data de ingresso](relatorios/scenarios/ct010_relatorio_de_cooperados_com_filtros_e_data_de_ingresso.md) | #23808 CA01; #23810 CA02; #23822 CA03; #23823 CA04; #23824 CA05; #23826 CA07 |
| CT011 | Relatorios | [Relatório de perfis e permissões](relatorios/scenarios/ct011_relatorio_de_perfis_e_permissoes.md) | #23837 CA01; #23839 CA02; #23840 CA03; #23846 CA05 |
| CT012 | Relatorios | [Relatório de unidades consumidoras por cooperado](relatorios/scenarios/ct012_relatorio_de_unidades_consumidoras_por_cooperado.md) | #23858 CA01; #23859 CA02; #23861 CA03; #23863 CA04; #23864 CA05; #23867 CA07 |
| CT013 | Relatorios | [Relatório de usinas por status e localização](relatorios/scenarios/ct013_relatorio_de_usinas_por_status_e_localizacao.md) | #23891 CA01; #23892 CA02; #23893 CA03; #23895 CA05 |
| CT014 | Relatorios | [Relatório de entidades externas por tipo e status](relatorios/scenarios/ct014_relatorio_de_entidades_externas_por_tipo_e_status.md) | #23912 CA01; #23914 CA02; #23915 CA03; #23917 CA05 |
| CT015 | Relatorios | [Exportação de relatórios em PDF ou CSV](relatorios/scenarios/ct015_exportacao_de_relatorios_em_pdf_ou_csv.md) | #23825 CA06; #23844 CA04; #23866 CA06; #23894 CA04; #23916 CA04 |
| CT016 | Relatorios | [Relatório de usuários — cenário condicionado à definição de critérios](relatorios/scenarios/ct016_relatorio_de_usuarios_cenario_condicionado_a_definicao_de_criteri.md) | #27052 Feature (sem critérios de aceitação); US #27053 |

## Sobre CRUD e inativação

A atividade pede **criar, consultar, atualizar e excluir em um mesmo cenário quando houver um CRUD**. Porém, os requisitos selecionados descrevem inclusão, consulta, atualização e **alteração de status**, sem especificar **exclusão**. Portanto, não se nomeou nenhum fluxo de inativação como excluir nem se criou uma exclusão imaginária. Deve-se esclarecer com os stakeholders se há requisito de exclusão e como se relaciona ao status.

## Como usar no GitHub

1. Crie um repositório individual público no GitHub (por exemplo, `bvapp-cenarios-eduardo-brito`).
2. Extraia este ZIP e envie o conteúdo da pasta raiz para o repositório.
3. Confirme que o professor consegue abrir os `.md` individualmente e visualizar este README.
4. Compartilhe o endereço verdadeiro do **seu repositório** no Classroom (não foi possível publicar no GitHub automaticamente nesta entrega).

## Checklist de conformidade

- [x] Mais de dez cenários individuais de documentação
- [x] Autoria informada em todos os cenários
- [x] Objetivo, IDs originais, ator, fluxos, regras, dados e resultados
- [x] Questões e conflitos sinalizados sem inventar regras
- [x] Separação por recorte e índice de rastreabilidade
- [ ] Decisões dos stakeholders incorporadas (pendente)
- [ ] Repositório pessoal publicado e link enviado (a cargo do autor)
