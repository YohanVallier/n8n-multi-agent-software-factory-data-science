# Exemplo de Especificação Modular de Entrada

Use os exemplos abaixo no campo **"Especificação do Módulo"** do `Form Trigger (Web Download)` para testar o fluxo de forma incremental.

---

## Exemplo 1 — Módulo 01 (Planejamento e Arquitetura)

- **ID/Nome do Projeto:** `sistema_busca_freelances`
- **Nome do Módulo:** `modulo_01_arquitetura`
- **Estado de Módulos Anteriores (Opcional):** *(deixar vazio)*
- **Orçamento Máximo (USD):** `5.0`

### Especificação do Módulo

```text
MÓDULO 01 — ARQUITETURA E PLANEJAMENTO
Atue como Software Architect.
Planeje o sistema de busca de oportunidades freelancer.
Defina:
1. Arquitetura geral.
2. Estrutura de diretórios.
3. Banco de dados.
4. Comunicação entre módulos.
5. Contratos de entrada e saída.
6. Estratégia de coleta de cada plataforma.
7. Estratégia de automação com Python.
8. Estratégia de integração com n8n.
9. Processamento de dados.
10. Inteligência artificial.

Crie uma arquitetura extensível que permita adicionar novas fontes sem modificar o sistema inteiro.
Defina um modelo único de oportunidade contendo:
- opportunity_id;
- title;
- description;
- source;
- source_group;
- original_url;
- published_at;
- collected_at;
- budget;
- technologies;
- category;
- compatibility_score;
- status.

Os campos deverão aceitar valores ausentes.
Defina como cada conector entregará informações ao motor central.
Identifique quais fontes permitem automação de navegador e quais precisarão de importação manual ou notificações.

Entregáveis:
- ARCHITECTURE.md;
- Diagrama de arquitetura;
- Estrutura de diretórios;
- Modelo de dados;
- Plano de execução;
- Dependências entre módulos.

Não desenvolva funcionalidades ainda.
```

---

## Exemplo 2 — Módulo 02 (Implementação Incremental com Memória de Estado)

- **ID/Nome do Projeto:** `sistema_busca_freelances`
- **Nome do Módulo:** `modulo_02_core_dados`
- **Estado de Módulos Anteriores (Opcional):** *(colar o conteúdo completo do arquivo `PROJECT_STATE.json` gerado no Módulo 01)*
- **Orçamento Máximo (USD):** `5.0`

### Especificação do Módulo

```text
MÓDULO 02 — MODELO DE DADOS E CAMADA DE PERSISTÊNCIA SQLITE
Implemente exclusivamente:
1. Schemas Pydantic para o modelo Opportunity com suporte a campos opcionais e validação de datas/URLs.
2. Camada de banco de dados SQLite com criação idempotente de tabelas e deduplicação por hash de oportunidade.
3. Repositório CRUD com logging estruturado e tratamento de exceções.
4. Testes unitários em pytest cobrindo inserção, duplicidade e campos ausentes.

Reutilize os contratos definidos no Módulo 01 sem recriar a documentação de arquitetura já aprovada.
```
