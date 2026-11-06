# Pendências herdadas do walkthrough (Q01–Q31)

Fonte: aba `Dúvidas para stakeholders` da planilha individual de walkthrough. Esta é uma **síntese**, não uma resolução; a planilha original prevalece.

- **Q01:** Composição do endereço da cooperativa e formatos válidos de CNPJ/e-mail.
- **Q02:** Quantidade de cooperativas e regra de segundo cadastro.
- **Q03:** Unicidade de CNPJ/e-mail na cooperativa.
- **Q04:** Perfis e permissões para cadastro, consulta, alteração e relatórios.
- **Q05:** Texto e padrão visual de mensagens e destaques.
- **Q06:** Tratamento de dados inválidos, duplicados ou erro de serviço CEP.
- **Q07:** Significado e destinatários dos vínculos institucionais.
- **Q08:** Consulta sem cooperativa cadastrada.
- **Q09:** Campos e auditoria exibidos na consulta da cooperativa.
- **Q10:** Campos editáveis e destaque na edição da cooperativa.
- **Q11:** Semântica/formato/disponibilidade de datas e usuário responsável.
- **Q12:** Fornecedor pessoa física (CPF) versus razão social/CNPJ.
- **Q13:** Conflito: endereço obrigatório no CA01 e opcional no CA03; site.
- **Q14:** Status padrão ativo no cadastro de fornecedor.
- **Q15:** Duplicidade de CNPJ (máscara, excluídos, inativos, e-mail).
- **Q16:** Colunas, ordenação e paginação da lista de fornecedores.
- **Q17:** Busca e filtro de fornecedores: correspondência e combinação.
- **Q18:** Campos editáveis e regras para fornecedor inativo.
- **Q19:** Efeitos e histórico da alteração de status do fornecedor.
- **Q20:** Colunas, ordenação, inclusão de inativos e conteúdo de relatórios.
- **Q21:** Gerar versus exportar, seleção PDF/CSV e fidelidade de filtros.
- **Q22:** Relatório vazio, falha e carregamento.
- **Q23:** Significado de perfil no filtro de cooperados.
- **Q24:** CPF/CNPJ do cooperado e relatório de cargos.
- **Q25:** Tipos de correspondência e combinação dos filtros.
- **Q26:** Funcionalidades versus permissões no relatório de perfis.
- **Q27:** Escopo/permissão do filtro por cooperado no relatório UC.
- **Q28:** Incluir UCs inativas na contagem por cooperado.
- **Q29:** Significado de localização e listagem/histórico de usinas.
- **Q30:** Quais entidades externas e tipos do filtro.
- **Q31:** Critérios de aceitação ausentes do relatório de usuários.

## Conflitos prioritários

- Fornecedores: endereço obrigatório (#24315) versus opcional (#24325).
- Fornecedores: critérios falam em razão social/CNPJ, mas a análise do backend registra modelo que usa nome e CPF ou CNPJ.
- Relatório de cooperados: exportação PDF ou CSV prevista, mas backend analisado no walkthrough oferece apenas PDF.
- Relatório de usuários: feature #27052 não possui critérios de aceitação no levantamento.
- Inativação não é exclusão. Não foi localizado requisito de exclusão para cooperativa/fornecedor no recorte analisado; não foi inventado um fluxo CRUD de exclusão.
