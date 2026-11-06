# CT002 — Bloqueio de cadastro de Cooperativa com campos obrigatórios ausentes

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Cooperativa  
**Estado:** ESPECIFICADO COM PENDÊNCIAS PONTUAIS  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Bloqueio de cadastro de Cooperativa com campos obrigatórios ausentes, conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #24058
- **User Story(s):** #24103
- **Critérios de aceitação:** #24098, #24099

## Ator
Usuário autorizado a cadastrar Cooperativa.

## Pré-condições
Uma tentativa de cadastro de Cooperativa é possível segundo o escopo de Q02.

## [FP] Fluxo principal
1. Abrir o cadastro de Cooperativa.
2. Informar razão social, CNPJ e endereço e deixar o e-mail vazio.
3. Solicitar o cadastro.
4. **Esperado:** a inclusão é impedida, é apresentada mensagem de erro e o campo obrigatório não preenchido é destacado.

## [FA] Fluxos alternativos e exceções
- FA01: deixar a razão social vazia: mesmo bloqueio e destaque.
- FA02: preencher todos os campos obrigatórios, sem os opcionais: a inclusão é permitida se os valores estiverem válidos (demais validações, Q01 e Q06).

## [RN] Regras de negócio documentadas
RN01: razão social, CNPJ, endereço e e-mail são obrigatórios (#24098). RN02: ausências impedem a inclusão (#24099).

## Dados de teste e resultados esperados
| Entrada | Esperado |
|---|---|
| E-mail vazio | Sem novo cadastro; erro e campo destacado |
| Razão social vazia | Sem novo cadastro; erro e campo destacado |
| Nome fantasia não informado | A ausência deste campo, por si só, não impede cadastro (#24100) |

## Dúvidas para validação
Q01 (formatos e endereço), Q05 (texto/forma do erro), Q06 (validações e falhas externas).

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
