# CT001 — Manutenção dos dados da Cooperativa (CRUD parcialmente especificado)

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Cooperativa  
**Estado:** PARCIAL — exclusão e decisões de negócio pendentes  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Manutenção dos dados da Cooperativa (CRUD parcialmente especificado), conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #24058 (inclusão), #24059 (consulta), #24060 (atualização)
- **User Story(s):** #24103 (inclusão), #24112 (consulta), #24129 (edição)
- **Critérios de aceitação:** #24098–#24101; #24106–#24108; #24117, #24119, #24123, #24125, #24126

## Ator
Usuário com autorização adequada (perfil específico: Q04).

## Pré-condições
Há acesso ao módulo; para criar, não há cooperativa de teste previamente cadastrada; para consultar e atualizar, há um cadastro realizado. A possibilidade de múltiplas cooperativas depende de Q02.

## [FP] Fluxo principal
1. **CRIAR:** o ator acessa o cadastro e informa razão social, CNPJ, endereço e e-mail; pode informar nome fantasia e data de fundação.
2. Solicita o cadastro. **Esperado:** quando todos os campos obrigatórios estão preenchidos, o sistema registra a Cooperativa e informa sucesso (#24098–#24100).
3. **CONSULTAR:** o ator autorizado acessa a consulta. **Esperado:** visualiza os dados cadastrados, conforme permissões do perfil (#24106–#24108).
4. **ATUALIZAR:** altera um dado cadastral permitido, preservando os campos obrigatórios, e confirma. **Esperado:** os novos dados são registrados; há mensagem de confirmação, registro da data da última atualização e do usuário responsável (#24117–#24126).
5. **EXCLUIR:** operação documentalmente **não especificada** no recorte analisado. **Resultado esperado indefinido**: não se afirma que existe botão, exclusão física/lógica, confirmação ou remoção. A etapa somente poderá ser detalhada após decisão dos stakeholders.

## [FA] Fluxos alternativos e exceções
- **FA01 — campo obrigatório vazio (criação):** tentar incluir sem razão social. **Esperado:** impedir a inclusão, exibir erro e destacar o campo ausente (#24099).
- **FA02 — campo obrigatório apagado (edição):** remover o e-mail obrigatório e tentar atualizar. **Esperado:** impedir a atualização e exibir mensagem de erro (#24119, #24123).
- **FA03 — usuário sem permissão de consulta:** tentar visualizar. **Esperado:** respeitar a restrição do perfil (#24108); forma da negativa depende de Q04.
- **FA04 — excluir:** não executável como critério de aceitação enquanto não houver requisito validado.

## [RN] Regras de negócio documentadas
- RN01: inclusão exige razão social, CNPJ, endereço e e-mail; nome fantasia e data de fundação são opcionais.
- RN02: consulta respeita o perfil do usuário.
- RN03: atualização não pode deixar campos obrigatórios vazios e deve registrar data e responsável.
- RN04: inexistem critérios explícitos de exclusão no conjunto selecionado.

## Dados de teste e resultados esperados
| Etapa | Dados fictícios ou condição | Resultado esperado |
|---|---|---|
| Criar | Razão social `Cooperativa Exemplo`, CNPJ `<cnpj_valido_novo>`, endereço `<endereco>`, e-mail `contato@exemplo.test` | Cadastro registrado; sucesso informado |
| Consultar | Registro criado e usuário com permissão | Dados cadastrados apresentados |
| Atualizar | Alterar nome fantasia para `Coop Exemplo` | Alteração registrada; data e usuário responsáveis registrados |
| Excluir | Registro existente | **A definir**: operação não especificada |
| Inválido | Razão social vazia | Cadastro impedido, erro e destaque do campo |

## Dúvidas para validação
Q01–Q11; sobretudo Q02 (quantidade de cooperativas), Q04 (permissões), Q09–Q11 (consulta, campos editáveis e auditoria). **Nova pergunta para stakeholders:** existe exclusão da Cooperativa? Se sim, regras, permissão e efeitos?

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
