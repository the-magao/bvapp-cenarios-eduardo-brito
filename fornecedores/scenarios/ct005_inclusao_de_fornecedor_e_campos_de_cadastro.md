# CT005 — Inclusão de fornecedor e campos de cadastro

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24315 CA01; #24322 CA02; #24325 CA03

## Objetivo
Especificar inclusão segundo os critérios, apontando o conflito sobre endereço.

## Ator
Usuário autorizado a incluir fornecedor (Q04).

## Pré-condições
Nenhum registro com CNPJ escolhido, sujeitos a critérios de duplicidade (Q15).

## [FP] Fluxo principal
1. O ator abre a inclusão de fornecedor.
2. O sistema apresenta CNPJ, razão social, telefone, e-mail, endereço e status, além do site institucional.
3. O ator informa os dados fictícios previstos e solicita a inclusão.
4. Quando os campos obrigatórios definidos estiverem preenchidos, o sistema efetua a inclusão.
5. O ator consulta a lista e verifica a existência do fornecedor.

## [FA] Fluxos alternativos e de exceção
- FA01: omitir telefone ou e-mail impede a inclusão e destaca o campo ausente (#24322).
- FA02: não decidir se endereço vazio é aceito; CA01 o torna obrigatório e CA03 opcional (Q13).
- FA03: uso do valor padrão ativo e possibilidade de alterá-lo na inclusão dependem de Q14.

## [RN] Regras de negócio existentes
- RN01: campos descritos em #24315; endereço em conflito com #24325.
- RN02: campos obrigatórios faltantes impedem a inclusão, com erro e destaque (#24322).

## Dados de teste e resultados esperados
- Entrada: Fornecedor Solar Exemplo Ltda.; CNPJ fictício; telefone e e-mail fictícios; endereço e site ilustrativos.
- Esperado: inclusão nos casos sem conflito; não concluir resultado para endereço ausente.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q04, Q05, Q12, Q13, Q14. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
