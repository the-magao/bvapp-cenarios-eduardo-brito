# CT015 — Exportação de relatórios em PDF ou CSV

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Relatorios  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #23825 CA06; #23844 CA04; #23866 CA06; #23894 CA04; #23916 CA04

## Objetivo
Especificar exportação nos formatos expressamente citados, distinguindo requisitos de implementação atual.

## Ator
Usuário autorizado a exportar o relatório escolhido (Q04).

## Pré-condições
Relatório selecionado foi gerado com registros e filtros conhecidos.

## [FP] Fluxo principal
1. O ator abre um relatório dentre cooperados, perfis, UCs, usinas ou entidades externas.
2. Solicita a opção de exportação em PDF.
3. O sistema disponibiliza a exportação em PDF prevista no requisito.
4. O ator solicita a opção de exportação em CSV.
5. O sistema disponibiliza a exportação em CSV prevista no requisito.
6. O ator verifica o tipo do arquivo obtido para cada escolha.

## [FA] Fluxos alternativos e de exceção
- FA01: a redação “PDF ou CSV” pode representar escolha do usuário ou opções alternativas; confirmar Q21.
- FA02: backend de cooperados observado no walkthrough exporta apenas PDF; divergência com o requisito deve ser validada.
- FA03: equivalência entre filtros exibidos e exportados requer resposta de Q21.

## [RN] Regras de negócio existentes
- RN01: requisitos de exportação especificam PDF ou CSV nos cinco relatórios citados.
- RN02: não assumir que ambos os formatos já estejam implementados.

## Dados de teste e resultados esperados
- Entrada: relatório de cooperados com filtro de status e outras amostras fictícias.
- Esperado: arquivos dos formatos declarados no requisito; detalhe de seleção/conteúdo aguarda Q21.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q04, Q20, Q21, Q22. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
