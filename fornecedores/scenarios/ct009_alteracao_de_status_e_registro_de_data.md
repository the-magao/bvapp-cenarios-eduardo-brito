# CT009 — Alteração de status e registro de data

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24350 CA01; #24351 CA02

## Objetivo
Especificar mudança de status ativo/inativo com registro da data.

## Ator
Usuário autorizado a alterar status (Q04).

## Pré-condições
Fornecedor F1 existente e ativo.

## [FP] Fluxo principal
1. O ator consulta F1.
2. Solicita alteração de status para inativo.
3. O sistema atualiza o status do fornecedor.
4. O sistema registra a data da alteração.
5. O ator consulta F1 e verifica status inativo e rastreabilidade de data.
6. O ator solicita retorno ao status ativo.
7. O sistema altera o status e registra a nova data.

## [FA] Fluxos alternativos e de exceção
- FA01: efeitos do status sobre fornecedores associados a ativos não foram definidos (Q19).
- FA02: registrar somente última data ou histórico completo depende de Q19.

## [RN] Regras de negócio existentes
- RN01: alternar status entre ativo e inativo (#24350).
- RN02: registrar a data de alteração (#24351).
- RN03: inativação não equivale a exclusão do cadastro.

## Dados de teste e resultados esperados
- Entrada: status ativo → inativo → ativo.
- Esperado: estado consultado acompanha a última alteração; registro de data correspondente.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q04, Q11, Q19. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
