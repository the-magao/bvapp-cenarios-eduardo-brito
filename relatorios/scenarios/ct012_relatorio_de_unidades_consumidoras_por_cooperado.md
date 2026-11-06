# CT012 — Relatório de unidades consumidoras por cooperado

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Relatorios  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #23858 CA01; #23859 CA02; #23861 CA03; #23863 CA04; #23864 CA05; #23867 CA07

## Objetivo
Especificar relatório de UCs, responsável, filtro por cooperado e contagem.

## Ator
Usuário autorizado a relatórios de UC (escopo de acesso pendente: Q27).

## Pré-condições
Cooperados C1 e C2 com UCs associadas e datas conhecidas.

## [FP] Fluxo principal
1. O ator solicita geração do relatório de unidades consumidoras.
2. O sistema apresenta as UCs cadastradas e o cooperado responsável por cada uma.
3. O ator filtra as UCs vinculadas ao cooperado C1.
4. O relatório apresenta a quantidade de UCs por cooperado, conforme regra a confirmar para status inativo.
5. O sistema exibe datas de criação e última atualização por UC.
6. Após geração bem-sucedida, apresenta a mensagem de sucesso e o relatório.

## [FA] Fluxos alternativos e de exceção
- FA01: UC inativa na contagem depende de Q28.
- FA02: escopo administrativo ou somente UCs do usuário logado depende de Q27.
- FA03: data da última edição ausente exige decisão (Q11).

## [RN] Regras de negócio existentes
- RN01: UCs e cooperados responsáveis (#23858, #23859).
- RN02: filtrar por cooperado (#23861).
- RN03: quantidade e datas (#23863, #23864).

## Dados de teste e resultados esperados
- Entrada: C1 com 2 UCs ativas e 1 inativa; C2 com 1 ativa (dados ilustrativos).
- Esperado: filtro de C1 apresenta UCs vinculadas; contagem de inativos é uma pendência, não um número presumido.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q11, Q20, Q27, Q28. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
