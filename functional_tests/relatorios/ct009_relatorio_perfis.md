# CT009 — Relatório de perfis e permissões

**Autoria:** Eduardo Brito Oliveira  
**Estado:** documentado com pendências dos stakeholders  
**Módulo:** Gestão de Pessoas / Relatorios  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #23837 CA01; #23839 CA02; #23840 CA03; #23846 CA05

## Objetivo
Especificar relatório de perfis com permissões e datas de criação/atualização.

## Ator
Usuário autorizado a gerar relatório de perfis.

## Pré-condições
Existem perfis cadastrados com permissões e dados históricos disponíveis.

## [FP] Fluxo principal
1. O ator solicita geração de relatório de perfis e permissões.
2. O sistema reúne os perfis cadastrados.
3. Para cada perfil, apresenta as funcionalidades/permissões atribuídas conforme definição pendente.
4. Inclui data de criação e data da última atualização do perfil.
5. Quando gerado com sucesso, exibe “Relatório gerado com sucesso.” e apresenta o relatório.

## [FA] Fluxos alternativos e de exceção
- FA01: perfil sem permissões exige regra de apresentação (Q26).
- FA02: ausência de data de última atualização na fonte exige definição do registro (Q11).

## [RN] Regras de negócio existentes
- RN01: listar perfis (#23837).
- RN02: exibir funcionalidades e permissões por perfil (#23839).
- RN03: data de criação e última atualização (#23840).

## Dados de teste e resultados esperados
- Entrada: perfil Administrativo com permissões conhecidas e datas ilustrativas.
- Esperado: perfil e informações previstas exibidos, sem definir representação de data ausente.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q11, Q20, Q22, Q26. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.


## Rastreabilidade complementar e verificação de dados
- Critérios do OpenProject: #23837, #23839, #23840, #23846.
- Critério de exportação relacionado: #23844 (exportar PDF/CSV — ver CT013).
- A **geração** e a **exportação** são verificações distintas. O formato exato de mensagens, listas vazias, filtros combinados e falhas depende de Q20–Q30 conforme o relatório.

| Condição / dado de teste | Resultado esperado verificável |
|---|---|
| Dados cadastrados que correspondem aos filtros definidos no critério | Relatório gerado com as informações previstas no CA, sujeito às definições pendentes |
| Aplicar filtro explicitamente previsto no CA | Conteúdo limitado pelo critério do filtro; detalhes de combinação a validar |
| Solicitar exportação do relatório | Disponibilidade de PDF ou CSV prevista em #23844; confirmação de formato/efeitos aguardando Q21 |

**Sem execução:** esta documentação não relata testes realizados nem afirma que o backend implemente todas as opções do requisito.
