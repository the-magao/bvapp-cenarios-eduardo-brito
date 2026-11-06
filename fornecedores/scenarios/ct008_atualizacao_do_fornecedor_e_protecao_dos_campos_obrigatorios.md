# CT008 — Atualização do fornecedor e proteção dos campos obrigatórios

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24358 CA01; #24359 CA02; #24360 CA03

## Objetivo
Especificar atualização de fornecedor, rejeição de CNPJ já existente e preservação de obrigatórios.

## Ator
Usuário autorizado a editar fornecedor.

## Pré-condições
Fornecedores F1 e F2 previamente cadastrados com CNPJs diferentes.

## [FP] Fluxo principal
1. O ator escolhe F1 e solicita edição.
2. Altera dado cadastral editável de F1, mantendo preenchidos os campos obrigatórios confirmados.
3. Solicita salvar a atualização.
4. O sistema atualiza os dados de F1.
5. O ator consulta F1 e verifica a alteração persistida.

## [FA] Fluxos alternativos e de exceção
- FA01: retirar telefone ou e-mail obrigatório deve impedir atualização que deixe cadastro incompleto (#24360).
- FA02: substituir CNPJ de F1 pelo CNPJ de F2 deve ser impedido (#24359).
- FA03: editabilidade do CNPJ e tratamento de fornecedor inativo dependem de Q18.

## [RN] Regras de negócio existentes
- RN01: permitir atualização cadastral (#24358).
- RN02: impedir duplicidade de CNPJ (#24359).
- RN03: manter obrigatórios preenchidos (#24360).

## Dados de teste e resultados esperados
- Entrada: alteração de telefone de F1; depois e-mail vazio; depois CNPJ de F2.
- Esperado: alteração válida persistida; tentativas inválidas não sobrescrevem dados válidos.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q12, Q13, Q15, Q18. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
