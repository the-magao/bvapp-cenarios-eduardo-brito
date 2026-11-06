# CT003 — Consulta da Cooperativa com controle de acesso

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Cooperativa  
**Estado:** ESPECIFICADO COM PENDÊNCIAS PONTUAIS  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Consulta da Cooperativa com controle de acesso, conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #24059
- **User Story(s):** #24112
- **Critérios de aceitação:** #24106, #24107, #24108

## Ator
Usuário que solicita consulta aos dados da Cooperativa.

## Pré-condições
Cooperativa cadastrada; dois perfis de teste cuja autorização de consulta seja conhecida após Q04.

## [FP] Fluxo principal
1. Acessar a consulta com um usuário que possua a permissão correspondente.
2. Localizar os dados da Cooperativa.
3. **Esperado:** o sistema apresenta os dados cadastrados, respeitando a permissão do perfil.

## [FA] Fluxos alternativos e exceções
- FA01: usuário sem a permissão necessária tenta consultar. **Esperado:** o acesso não deve ser autorizado, conforme #24108. A mensagem/experiência visual depende de Q04–Q05.
- FA02: nenhum cadastro existente. **Resultado pendente** (Q08).

## [RN] Regras de negócio documentadas
RN01: a consulta apresenta dados cadastrados (#24106–#24107). RN02: o acesso respeita permissões do perfil (#24108).

## Dados de teste e resultados esperados
| Entrada | Esperado |
|---|---|
| Perfil autorizado + cadastro existente | Consulta disponível e dados apresentados |
| Perfil sem autorização | Consulta não autorizada |
| Nenhuma Cooperativa cadastrada | A definir (Q08) |

## Dúvidas para validação
Q04 (perfis), Q08 (vazio), Q09 (campos apresentados).

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
