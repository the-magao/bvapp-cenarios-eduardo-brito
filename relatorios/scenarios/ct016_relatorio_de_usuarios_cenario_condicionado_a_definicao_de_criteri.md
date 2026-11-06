# CT016 — Relatório de usuários — cenário condicionado à definição de critérios

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Relatorios  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #27052 Feature (sem critérios de aceitação); US #27053

## Objetivo
Registrar o cenário candidato e os pontos que impedem uma especificação testável definitiva.

## Ator
Ator não definido nos requisitos (Q04/Q31).

## Pré-condições
Stakeholders devem definir critérios de aceitação, colunas, filtros e resultados.

## [FP] Fluxo principal
1. O ator previsto pelos stakeholders acessará a funcionalidade de relatório de usuários.
2. O ator solicitará a geração do relatório.
3. O sistema deverá apresentar o relatório conforme campos, filtros e regras ainda não especificados.
4. O responsável pela documentação deverá atualizar este cenário após validação formal dos critérios.

## [FA] Fluxos alternativos e de exceção
- FA01: usuário sem permissão — comportamento não definido.
- FA02: relatório vazio, falha de geração e tipos de arquivo — comportamento não definido.

## [RN] Regras de negócio existentes
- RN01: existe a feature #27052 e a US #27053, sem critérios de aceitação correspondentes no levantamento.
- RN02: não atribuir colunas, filtros ou mensagens sem decisão dos stakeholders.

## Dados de teste e resultados esperados
- Entrada: a ser definida.
- Esperado: INDETERMINADO até aprovação de critérios de aceitação; cenário não está pronto para execução.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q04, Q20, Q22, Q31. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
