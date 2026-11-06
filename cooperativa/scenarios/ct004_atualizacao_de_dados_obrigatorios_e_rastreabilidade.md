# CT004 — Atualização de dados obrigatórios e rastreabilidade

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Cooperativa  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24117 CA01; #24119 CA02; #24123 CA03; #24125 CA04; #24126 CA05

## Objetivo
Descrever atualização válida, bloqueio de remoção de dados obrigatórios e registros de data e autor.

## Ator
Usuário autorizado a editar cooperativa (Q04).

## Pré-condições
Cooperativa registrada; usuário autenticado.

## [FP] Fluxo principal
1. O ator abre a edição de uma cooperativa existente.
2. Altera um dado cadastral cuja editabilidade esteja confirmada (Q10).
3. Mantém preenchidos razão social, CNPJ, endereço e e-mail e solicita salvar.
4. O sistema atualiza o cadastro e exibe confirmação de sucesso.
5. O sistema registra a data da última atualização e o usuário responsável.
6. O ator consulta o registro e verifica que a alteração persistiu.

## [FA] Fluxos alternativos e de exceção
- FA01: remover endereço obrigatório e salvar; sistema impede alteração e emite erro, preservando o registro anterior.
- FA02: alterar CNPJ ou e-mail exige confirmação de editabilidade e unicidade (Q03/Q10).

## [RN] Regras de negócio existentes
- RN01: campos obrigatórios permanecem preenchidos (#24119).
- RN02: remoção de obrigatório é rejeitada (#24123).
- RN03: registrar data e usuário da atualização (#24125, #24126).

## Dados de teste e resultados esperados
- Entrada: substituir razão social ilustrativa por novo valor; depois tentar endereço vazio.
- Esperado: primeira edição persistida, confirmação e rastros; segunda tentativa rejeitada sem apagar endereço.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q03, Q05, Q10, Q11. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
