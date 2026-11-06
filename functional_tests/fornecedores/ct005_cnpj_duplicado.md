# CT005 — Impedimento de CNPJ duplicado no cadastro de Fornecedor

**Autor:** Eduardo Brito Oliveira  
**Módulo:** Gestão de Pessoas / Fornecedores  
**Estado:** ESPECIFICADO COM PENDÊNCIAS PONTUAIS  
**Natureza:** especificação documental — não implementado, não automatizado, não executado.

## Objetivo
Impedimento de CNPJ duplicado no cadastro de Fornecedor, conforme os requisitos publicados, sem presumir regras adicionais.

## Rastreabilidade
- **Feature(s):** #24306
- **User Story(s):** #24345
- **Critérios de aceitação:** #24335

## Ator
Usuário autorizado a cadastrar Fornecedores.

## Pré-condições
Já existe Fornecedor A com CNPJ `<cnpj_existente>`; a existência de cadastro com dados obrigatórios completos é garantida.

## [FP] Fluxo principal
1. Acessar inclusão de fornecedor.
2. Informar os dados do Fornecedor B, utilizando o mesmo CNPJ de A e preenchendo os outros campos exigidos.
3. Solicitar o cadastro.
4. **Esperado:** a inclusão de novo fornecedor com CNPJ duplicado é impedida.

## [FA] Fluxos alternativos e exceções
- FA01: informar CNPJ diferente e válido: a regra de duplicidade, isoladamente, não impede a inclusão, se os demais critérios forem satisfeitos.
- FA02: fornecedor existente inativo/excluído: efeito da duplicidade **a definir** (Q15).

## [RN] Regras de negócio documentadas
RN01: não é permitido cadastrar Fornecedor com CNPJ duplicado (#24335).

## Dados de teste e resultados esperados
| Entrada | Esperado |
|---|---|
| CNPJ de B igual ao de A | B não cadastrado |
| CNPJ novo | Sem bloqueio por duplicidade, sujeitos aos demais critérios |
| CNPJ com máscara diferente | Regra de normalização ainda não especificada |

## Dúvidas para validação
Q15 (normalização, inativos/excluídos e mensagens); não fixar texto de erro nem algoritmo de comparação.

**Nota de rastreabilidade:** os IDs são os identificadores do OpenProject; mudanças propostas no walkthrough ainda não equivalem a decisões aprovadas. Não se infere formato de tela, endpoint, resposta HTTP nem mensagem literal quando o critério não a define.
