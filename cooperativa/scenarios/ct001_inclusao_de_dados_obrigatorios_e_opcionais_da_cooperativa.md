# CT001 — Inclusão de dados obrigatórios e opcionais da cooperativa

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Cooperativa  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24098 CA01; #24099 CA02; #24100 CA03

## Objetivo
Especificar o cadastro da cooperativa com os campos previstos nos critérios, sem presumir validações não definidas.

## Ator
Usuário com autorização de cadastro (perfil a confirmar: Q04).

## Pré-condições
Existe ambiente de especificação e dados fictícios; política para segunda cooperativa não definida (Q02).

## [FP] Fluxo principal
1. O ator acessa a funcionalidade de inclusão de cooperativa.
2. O sistema disponibiliza razão social, CNPJ, endereço e e-mail como obrigatórios e nome fantasia e data de fundação como opcionais.
3. O ator informa valores de exemplo para os campos obrigatórios e, nesta execução, também para os opcionais.
4. O ator solicita a inclusão.
5. Estando preenchidos os obrigatórios e não ocorrendo outra restrição a esclarecer, o sistema cadastra e apresenta mensagem de sucesso.
6. O ator consulta o cadastro e confere os valores informados.

## [FA] Fluxos alternativos e de exceção
- FA01: sem nome fantasia e data de fundação, os campos opcionais não impedem o cadastro.
- FA02: se a cooperativa já existir, não definir antecipadamente aceitação/rejeição: Q02.

## [RN] Regras de negócio existentes
- RN01: razão social, CNPJ, endereço e e-mail são obrigatórios (#24098).
- RN02: nome fantasia e data de fundação são opcionais (#24100).

## Dados de teste e resultados esperados
- Entrada: Cooperativa Solar Exemplo; CNPJ fictício apenas para ilustração; endereço preenchido; contato@exemplo.test; nome fantasia opcional.
- Esperado: registro consultável e mensagem de sucesso; texto exato e validações de formato pendentes.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q01, Q02, Q04, Q05, Q03. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
