# CT011 — Relatório de usinas por status e localização

**Autoria:** Eduardo Brito Oliveira  
**Estado:** documentado com pendências dos stakeholders  
**Módulo:** Gestão de Pessoas / Relatorios  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #23891 CA01; #23892 CA02; #23893 CA03; #23895 CA05

## Objetivo
Especificar relatório de usinas com localização, status e filtragem.

## Ator
Usuário autorizado a relatórios de usinas.

## Pré-condições
Há usinas ativas e inativas cadastradas com dados de endereço.

## [FP] Fluxo principal
1. O ator solicita relatório de usinas.
2. O sistema apresenta as usinas cadastradas.
3. O ator verifica a presença das informações de localização e status exigidas.
4. Aplica filtro de status ativo e depois inativo.
5. Confere que cada resultado corresponde ao filtro utilizado.
6. Após sucesso, o sistema exibe a mensagem definida e apresenta o relatório.

## [FA] Fluxos alternativos e de exceção
- FA01: a granularidade de localização (endereço, município/estado ou coordenadas) depende de Q29.
- FA02: ausência de usinas e falha na geração dependem de Q22.

## [RN] Regras de negócio existentes
- RN01: gerar relatório de usinas (#23891).
- RN02: informar localização e status (#23892).
- RN03: filtrar por status (#23893).

## Dados de teste e resultados esperados
- Entrada: Usina A ativa e Usina B inativa.
- Esperado: listagem compatível com o status; formato da localização não antecipado.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q20, Q22, Q29. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.


## Rastreabilidade complementar e verificação de dados
- Critérios do OpenProject: #23891, #23892, #23893, #23895.
- Critério de exportação relacionado: #23894 (exportar PDF/CSV — ver CT013).
- A **geração** e a **exportação** são verificações distintas. O formato exato de mensagens, listas vazias, filtros combinados e falhas depende de Q20–Q30 conforme o relatório.

| Condição / dado de teste | Resultado esperado verificável |
|---|---|
| Dados cadastrados que correspondem aos filtros definidos no critério | Relatório gerado com as informações previstas no CA, sujeito às definições pendentes |
| Aplicar filtro explicitamente previsto no CA | Conteúdo limitado pelo critério do filtro; detalhes de combinação a validar |
| Solicitar exportação do relatório | Disponibilidade de PDF ou CSV prevista em #23894; confirmação de formato/efeitos aguardando Q21 |

**Sem execução:** esta documentação não relata testes realizados nem afirma que o backend implemente todas as opções do requisito.
