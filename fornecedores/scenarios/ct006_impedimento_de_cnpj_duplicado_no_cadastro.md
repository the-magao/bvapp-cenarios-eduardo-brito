# CT006 — Impedimento de CNPJ duplicado no cadastro

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24335 CA04; #24315 CA01

## Objetivo
Verificar que não se podem cadastrar dois fornecedores com o mesmo CNPJ.

## Ator
Usuário autorizado a incluir fornecedor.

## Pré-condições
Fornecedor F1 já cadastrado com CNPJ X.

## [FP] Fluxo principal
1. O ator abre inclusão de um segundo fornecedor.
2. Preenche todos os demais dados previstos e informa o mesmo CNPJ X do fornecedor F1.
3. Solicita concluir a inclusão.
4. O sistema identifica a duplicidade de CNPJ.
5. O sistema impede a criação do segundo fornecedor.
6. O ator consulta os registros para verificar que não houve segundo cadastro com CNPJ X.

## [FA] Fluxos alternativos e de exceção
- FA01: comparação de CNPJ com e sem máscara depende de Q15.
- FA02: duplicidade envolvendo fornecedor inativo ou excluído depende de Q15.

## [RN] Regras de negócio existentes
- RN01: impedir duplicidade de CNPJ entre fornecedores (#24335).

## Dados de teste e resultados esperados
- Entrada: F1: CNPJ X; F2: CNPJ X.
- Esperado: apenas F1 permanece cadastrado; mensagem específica de erro não foi definida.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q05, Q12, Q15. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
