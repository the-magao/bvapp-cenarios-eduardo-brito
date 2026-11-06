# CT002 — Bloqueio de inclusão com campos obrigatórios ausentes

**Autoria:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Cooperativa  
**Tipo:** documentação de cenário; **não automatizado e não executado**  
**Requisitos relacionados (IDs do OpenProject):** #24098 CA01; #24099 CA02

## Objetivo
Documentar rejeição da inclusão incompleta e feedback de erro.

## Ator
Usuário autorizado a cadastrar cooperativa (Q04).

## Pré-condições
Formulário de inclusão disponível.

## [FP] Fluxo principal
1. O ator abre o cadastro de cooperativa.
2. Preenche razão social, CNPJ e e-mail e mantém o endereço obrigatório não preenchido.
3. Solicita salvar o cadastro.
4. O sistema impede a inclusão, emite mensagem de erro e destaca o campo obrigatório ausente.
5. O ator informa o endereço e solicita salvar novamente.
6. Com os obrigatórios presentes, o sistema permite prosseguir, sujeito às regras pendentes.

## [FA] Fluxos alternativos e de exceção
- FA01: repetir a tentativa omitindo, individualmente, razão social, CNPJ e e-mail.
- FA02: valores inválidos, somente espaços ou indisponibilidade do serviço de CEP exigem regras adicionais (Q01/Q06).

## [RN] Regras de negócio existentes
- RN01: não incluir cooperativa com campo obrigatório ausente (#24099).
- RN02: erro com destaque do campo não preenchido (#24099).

## Dados de teste e resultados esperados
- Entrada: endereço vazio.
- Esperado: nenhum cadastro criado na tentativa inválida; erro e indicação do campo.

## Pendências do walkthrough / decisões dos stakeholders
**Questões referenciadas:** Q01, Q05, Q06. Consulte `docs/pendencias_stakeholders.md` e a planilha original. Nenhuma resposta para estas questões foi presumida.

## Observação sobre escopo
O cenário descreve o comportamento **requerido/documentado**, não afirma que ele já exista na implementação. Quaisquer detalhes de telas, endpoints ou mensagens não constantes dos requisitos permanecem a definir.
