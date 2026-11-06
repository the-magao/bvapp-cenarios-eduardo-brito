# CT012 — Relatório de entidades externas por tipo e status

**Autoria:** Eduardo Brito Oliveira  
**Estado:** documentado com pendências dos stakeholders  
**Módulo:** Gestão de Pessoas / Relatorios  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #23912 CA01; #23914 CA02; #23915 CA03; #23917 CA05

## Objetivo
Especificar relatório de entidades externas e os filtros previstos.

## Ator
Usuário autorizado a gerar relatório de entidades externas.

## Pré-condições
Existem registros das entidades que vierem a ser classificadas como externas pelos stakeholders.

## [FP] Fluxo principal
1. O ator acessa a geração do relatório de entidades externas.
2. Solicita apresentar as entidades externas cadastradas.
3. O sistema exibe o conjunto de entidades definido para este relatório.
4. O ator seleciona um tipo de entidade admitido e observa o resultado.
5. Aplica filtro de status ativo e posteriormente inativo.
6. No sucesso, o sistema apresenta “Relatório gerado com sucesso.” e o relatório.

## [FA] Fluxos alternativos e de exceção
- FA01: não fixar valores de tipo até definição de Q30.
- FA02: se não houver resultados, mensagem e tela aguardam Q22.

## [RN] Regras de negócio existentes
- RN01: gerar relatório de entidades externas (#23912).
- RN02: filtrar por tipo (#23914).
- RN03: filtrar por status ativo/inativo (#23915 e revisão da planilha).

## Dados de teste e resultados esperados
- Entrada: fornecedores/operadoras/prestadores apenas como candidatos a confirmar, não como conjunto definitivo.
- Esperado: filtros de tipo/status conforme categorias posteriormente validadas.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q20, Q22, Q30. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.


## Rastreabilidade complementar e verificação de dados
- Critérios do OpenProject: #23912, #23914, #23915, #23917.
- Critério de exportação relacionado: #23916 (exportar PDF/CSV — ver CT013).
- A **geração** e a **exportação** são verificações distintas. O formato exato de mensagens, listas vazias, filtros combinados e falhas depende de Q20–Q30 conforme o relatório.

| Condição / dado de teste | Resultado esperado verificável |
|---|---|
| Dados cadastrados que correspondem aos filtros definidos no critério | Relatório gerado com as informações previstas no CA, sujeito às definições pendentes |
| Aplicar filtro explicitamente previsto no CA | Conteúdo limitado pelo critério do filtro; detalhes de combinação a validar |
| Solicitar exportação do relatório | Disponibilidade de PDF ou CSV prevista em #23916; confirmação de formato/efeitos aguardando Q21 |

**Sem execução:** esta documentação não relata testes realizados nem afirma que o backend implemente todas as opções do requisito.
