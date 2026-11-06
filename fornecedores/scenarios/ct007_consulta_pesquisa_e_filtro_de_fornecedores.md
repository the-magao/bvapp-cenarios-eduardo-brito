# CT007 — Consulta, pesquisa e filtro de fornecedores

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24364 CA01; #24365 CA02; #24366 CA03

## Objetivo
Especificar consulta da lista, busca por razão social/CNPJ e filtro por status.

## Ator
Usuário autorizado a consultar fornecedores (Q04).

## Pré-condições
Fornecedores com razões sociais, CNPJs e estados conhecidos; ao menos um ativo e um inativo.

## [FP] Fluxo principal
1. O ator acessa a listagem de fornecedores.
2. O sistema apresenta os fornecedores cadastrados.
3. O ator pesquisa por uma razão social conhecida e confere a presença do registro correspondente.
4. O ator pesquisa por um CNPJ conhecido e confere a presença do fornecedor correspondente.
5. O ator aplica o filtro de status ativo e observa os itens correspondentes.
6. Repete a filtragem para status inativo.

## [FA] Fluxos alternativos e de exceção
- FA01: pesquisa sem correspondência; a representação de lista vazia depende de Q17.
- FA02: combinação de busca e status, busca parcial, máscara e ordenação dependem de Q16/Q17.

## [RN] Regras de negócio existentes
- RN01: consultar lista (#24364).
- RN02: pesquisar por razão social ou CNPJ (#24365).
- RN03: filtrar por status (#24366).

## Dados de teste e resultados esperados
- Entrada: fornecedor A ativo e fornecedor B inativo; critérios de pesquisa correspondentes.
- Esperado: localização dos fornecedores pelos campos previstos e filtragem conforme status.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q04, Q12, Q16, Q17. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
