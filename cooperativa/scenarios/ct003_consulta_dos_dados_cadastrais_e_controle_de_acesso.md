# CT003 — Consulta dos dados cadastrais e controle de acesso

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Cooperativa  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24106 CA01; #24107 CA02; #24108 CA03

## Objetivo
Especificar visualização dos dados cadastrados e respeito às permissões.

## Ator
Usuário com permissão de consulta a confirmar (Q04).

## Pré-condições
Há cooperativa previamente cadastrada.

## [FP] Fluxo principal
1. O ator autenticado solicita consultar a cooperativa.
2. O sistema verifica a autorização do perfil do usuário.
3. Quando autorizado, apresenta os dados cadastrados.
4. O ator compara razão social, CNPJ, endereço, e-mail, nome fantasia e data de fundação com os dados de origem.

## [FA] Fluxos alternativos e de exceção
- FA01: tentativa sem permissão deve ser negada; forma de negativa depende de Q04.
- FA02: ausência de cooperativa cadastrada, resposta visual pendente de Q08.

## [RN] Regras de negócio existentes
- RN01: acesso à consulta respeita as permissões do perfil (#24108).
- RN02: a consulta deve apresentar as informações cadastradas (#24107).

## Dados de teste e resultados esperados
- Entrada: cooperativa com dados conhecidos; perfil autorizado e não autorizado.
- Esperado: informações cadastrais correspondentes quando autorizado; não acesso quando não autorizado.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q04, Q08, Q09. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
