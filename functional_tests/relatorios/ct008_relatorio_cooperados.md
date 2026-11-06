# CT008 — Relatório de cooperados com filtros e data de ingresso

**Autoria:** Eduardo Brito Oliveira  
**Estado:** documentado com pendências dos stakeholders  
**Módulo:** Gestão de Pessoas / Relatorios  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #23808 CA01; #23810 CA02; #23822 CA03; #23823 CA04; #23824 CA05; #23826 CA07

## Objetivo
Especificar relatório de cooperados com campos e critérios de filtragem previstos.

## Ator
Usuário autorizado a gerar relatórios (Q04).

## Pré-condições
Existem cooperados com nomes, CPF, status e datas de ingresso conhecidos.

## [FP] Fluxo principal
1. O ator acessa o relatório de cooperados.
2. Solicita gerar a lista de cooperados cadastrados.
3. O sistema apresenta o relatório e a data de ingresso de cada cooperado.
4. O ator aplica filtro de status e verifica os cooperados correspondentes.
5. O ator aplica pesquisa por nome ou CPF/CNPJ conforme especificação, avaliando as dúvidas do campo.
6. Após geração bem-sucedida, o sistema apresenta a mensagem “Relatório gerado com sucesso.” e mostra o relatório.

## [FA] Fluxos alternativos e de exceção
- FA01: filtro por perfil requer definição se é perfil de acesso ou cargo (Q23).
- FA02: uso de CNPJ em cooperado conflita com cadastro que prevê CPF (Q24).
- FA03: resultado sem registros/falha requer orientação (Q22).

## [RN] Regras de negócio existentes
- RN01: relatório de cooperados cadastrados (#23808).
- RN02: filtros previstos em #23810, #23822 e #23823, sujeitos a esclarecimento.
- RN03: apresentar data de ingresso (#23824).

## Dados de teste e resultados esperados
- Entrada: cooperados fictícios com status e data de ingresso distintos.
- Esperado: relatório com registros correspondentes, data de ingresso e mensagem definida; filtros ambíguos aguardam decisão.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q04, Q20, Q22, Q23, Q24, Q25. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.


## Rastreabilidade complementar e verificação de dados
- Critérios do OpenProject: #23808, #23810, #23822, #23823, #23824, #23826.
- Critério de exportação relacionado: #23825 (exportar PDF/CSV — ver CT013).
- A **geração** e a **exportação** são verificações distintas. O formato exato de mensagens, listas vazias, filtros combinados e falhas depende de Q20–Q30 conforme o relatório.

| Condição / dado de teste | Resultado esperado verificável |
|---|---|
| Dados cadastrados que correspondem aos filtros definidos no critério | Relatório gerado com as informações previstas no CA, sujeito às definições pendentes |
| Aplicar filtro explicitamente previsto no CA | Conteúdo limitado pelo critério do filtro; detalhes de combinação a validar |
| Solicitar exportação do relatório | Disponibilidade de PDF ou CSV prevista em #23825; confirmação de formato/efeitos aguardando Q21 |

**Sem execução:** esta documentação não relata testes realizados nem afirma que o backend implemente todas as opções do requisito.
