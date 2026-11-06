# CT013 — Exportação de Relatórios em PDF ou CSV

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Relatórios  
**Estado:** ESPECIFICADO COM PENDÊNCIAS PONTUAIS  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Exportação de Relatórios em PDF ou CSV, conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #23808, #23837, #23858, #23891, #23912
- **User Story(s):** Histórias de geração de relatórios nas Features correspondentes
- **Critérios de aceitação:** #23825, #23844, #23866, #23894, #23916

## Ator
Usuário autorizado a gerar e exportar relatórios (Q04).

## Pré-condições
Existe ao menos um relatório contemplado pelos requisitos que possa ser solicitado.

## [FP] Fluxo principal
1. Selecionar um dos relatórios previstos: Cooperados, Perfis e Permissões, Unidades Consumidoras, Usinas ou Entidades Externas.
2. Aplicar um filtro documentado para o relatório escolhido, quando aplicável.
3. Solicitar a geração.
4. Selecionar a exportação em **PDF**. **Esperado:** existe opção de exportar nesse formato, conforme critério correspondente.
5. Repetir com formato **CSV**. **Esperado:** existe opção de exportar nesse formato, conforme critério correspondente.
6. Verificar correspondência dos dados exportados com os parâmetros do relatório **apenas quando a regra de fidelidade dos filtros for validada** (Q21).

## [FA] Fluxos alternativos e exceções
- FA01: sem registros correspondentes: conteúdo de arquivo, mensagem e possibilidade de exportar permanecem indefinidos (Q22).
- FA02: erro de geração/exportação: forma de comunicação e retentativa não definidas (Q21–Q22).
- FA03: implementação expõe só PDF: divergência implementação/requisito, não motivo para reescrever CA como PDF apenas.

## [RN] Regras de negócio documentadas
RN01: os cinco critérios de exportação estabelecem PDF ou CSV. RN02: não supor que gerar e exportar são a mesma operação.

## Dados de teste e resultados esperados
| Relatório | CA | Formatos previstos |
|---|---|---|
| Cooperados | #23825 | PDF ou CSV |
| Perfis/Permissões | #23844 | PDF ou CSV |
| Unidades Consumidoras | #23866 | PDF ou CSV |
| Usinas | #23894 | PDF ou CSV |
| Entidades Externas | #23916 | PDF ou CSV |

## Dúvidas para validação
Q20–Q22 (formato, ordem, fidelidade dos filtros, resultados vazios e falhas). O walkthrough observou possível divergência do backend, mas o cenário descreve o requisito e não declara execução.

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
