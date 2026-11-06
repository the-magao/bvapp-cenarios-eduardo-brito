# CT006 — Consulta, pesquisa e filtro de Fornecedores

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Estado:** ESPECIFICADO COM PENDÊNCIAS PONTUAIS  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Consulta, pesquisa e filtro de Fornecedores, conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #24308
- **User Story(s):** #24367, #24369
- **Critérios de aceitação:** #24364, #24365, #24366

## Ator
Usuário que consulta fornecedores, sujeito à autorização (Q04).

## Pré-condições
Há fornecedores registrados com razões sociais, CNPJs e status distintos.

## [FP] Fluxo principal
1. Abrir a lista de fornecedores.
2. **Esperado:** o sistema exibe fornecedores cadastrados (#24364).
3. Pesquisar por razão social de um fornecedor conhecido. **Esperado:** a pesquisa permite localizar fornecedores por razão social (#24365).
4. Pesquisar por CNPJ de fornecedor conhecido. **Esperado:** a pesquisa permite localizar fornecedores por CNPJ (#24365).
5. Filtrar por status `ativo` e depois por `inativo`. **Esperado:** a lista é filtrada pelo status escolhido (#24366).

## [FA] Fluxos alternativos e exceções
- FA01: termo sem correspondência; formato da lista vazia/mensagem a definir (Q17).
- FA02: combinação de busca e filtro; resultado a definir (Q17).

## [RN] Regras de negócio documentadas
RN01: é possível listar fornecedores, pesquisar por razão social ou CNPJ e filtrar por status.

## Dados de teste e resultados esperados
| Entrada | Esperado |
|---|---|
| Razão social do Fornecedor A | A pode ser localizado |
| CNPJ do Fornecedor B | B pode ser localizado |
| Status ativo | Filtragem de fornecedores ativos |
| Status inativo | Filtragem de fornecedores inativos |

## Dúvidas para validação
Q16 (colunas, ordenação, paginação), Q17 (correspondência parcial/exata, combinação e vazio).

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
