# CT004 — Manutenção de Fornecedores (CRUD parcialmente especificado)

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Estado:** PARCIAL — exclusão e Q13 pendentes  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Manutenção de Fornecedores (CRUD parcialmente especificado), conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #24306 (inclusão), #24308 (consulta), #24309 (atualização)
- **User Story(s):** #24345 (adicionar), #24367 (consultar), #24361 (editar)
- **Critérios de aceitação:** #24315, #24322, #24325, #24335; #24364–#24366; #24358–#24360

## Ator
Usuário autorizado a cadastrar, consultar e editar fornecedores (autorização: Q04).

## Pré-condições
O CNPJ do fornecedor de teste ainda não consta dos cadastros; há acesso aos recursos sujeitos às permissões a esclarecer.

## [FP] Fluxo principal
1. **CRIAR:** abrir o cadastro e informar CNPJ, razão social, telefone, e-mail, endereço e status (padrão ativo, #24315); opcionalmente informar site institucional.
2. Solicitar inclusão. **Esperado:** se os campos exigidos estiverem preenchidos e o CNPJ não estiver cadastrado, o fornecedor é registrado. **ATENÇÃO:** endereço está em contradição entre #24315 e #24325; este roteiro preenche endereço e não resolve o conflito.
3. **CONSULTAR:** acessar a listagem de fornecedores, localizar o registro por razão social ou CNPJ. **Esperado:** fornecedor aparece na lista (#24364–#24365).
4. **ATUALIZAR:** editar um campo cadastral permitido (por exemplo, telefone), sem esvaziar os obrigatórios nem duplicar CNPJ, e salvar. **Esperado:** alteração registrada e campos obrigatórios preservados (#24358–#24360).
5. **EXCLUIR:** **operação não especificada** para Fornecedores. **Resultado esperado indefinido** até validação; não equiparar a alterar status.

## [FA] Fluxos alternativos e exceções
- FA01 — criar com campo obrigatório vazio (ex.: razão social): cadastro impedido, erro e destaque (#24322).
- FA02 — criar com CNPJ existente: impedir duplicidade (#24335).
- FA03 — atualizar para CNPJ existente: impedir duplicidade (#24359).
- FA04 — atualizar removendo campo obrigatório: impedir atualização (#24360).
- FA05 — endereço vazio: **não concluir resultado** antes de Q13.
- FA06 — exclusão: aguardar regra de negócio e CA correspondente.

## [RN] Regras de negócio documentadas
RN01: campos de inclusão conforme #24315; status inicial ativo. RN02: cadastro e atualização não podem aceitar campos obrigatórios vazios. RN03: não aceitar CNPJ duplicado. RN04: alteração de status (#24350) é uma função própria e não prova existência de exclusão.

## Dados de teste e resultados esperados
| Etapa | Dados fictícios | Resultado esperado |
|---|---|---|
| Criar | `Fornecedor Exemplo Ltda.`, CNPJ `<cnpj_valido_novo>`, telefone `<telefone>`, e-mail `fornecedor@exemplo.test`, endereço `<endereco>` | Cadastro registrado se requisitos atendidos |
| Consultar | Buscar `Fornecedor Exemplo` ou `<cnpj_valido_novo>` | Registro localizado |
| Atualizar | Telefone `<telefone_novo>` | Dado persistido; demais obrigatórios preservados |
| Excluir | Fornecedor previamente criado | **A definir**; comportamento não especificado |
| Cadastro inválido | Razão social vazia | Operação negada, erro e destaque |

## Dúvidas para validação
Q04–Q06, Q12–Q18. **Conflito prioritário Q13:** endereço é obrigatório em #24315 e opcional em #24325. **Nova pergunta:** existe exclusão de fornecedor? Física/lógica? Efeitos sobre históricos e vínculos?

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
