# CT007 — Alteração de status do Fornecedor e registro da data

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Estado:** ESPECIFICADO COM PENDÊNCIAS PONTUAIS  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Alteração de status do Fornecedor e registro da data, conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #24310
- **User Story(s):** #24354
- **Critérios de aceitação:** #24350, #24351

## Ator
Usuário autorizado a alterar status do Fornecedor.

## Pré-condições
Fornecedor existente com status ativo e registro identificado.

## [FP] Fluxo principal
1. Consultar fornecedor existente.
2. Solicitar mudança de status de `ativo` para `inativo`.
3. **Esperado:** o status passa a inativo e a data da alteração é registrada (#24350–#24351).
4. Solicitar mudança de `inativo` para `ativo`.
5. **Esperado:** o status passa a ativo e a data da nova alteração é registrada.

## [FA] Fluxos alternativos e exceções
- FA01: solicitação por usuário sem autorização — a regra de permissão específica não consta desses CAs; verificar Q04, sem supor mensagem.
- FA02: tentar associar fornecedor inativo a outras entidades — efeitos ainda não definidos (Q19).

## [RN] Regras de negócio documentadas
RN01: status alterna entre ativo e inativo. RN02: a data da alteração é registrada. RN03: inativar não equivale a excluir.

## Dados de teste e resultados esperados
| Entrada | Esperado |
|---|---|
| Ativo → Inativo | Status inativo + data registrada |
| Inativo → Ativo | Status ativo + data registrada |
| Solicitação de excluir | Fora deste cenário; operação não definida |

## Dúvidas para validação
Q11 (precisão/forma da data); Q19 (efeitos sobre vínculos, histórico e permissões).

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
