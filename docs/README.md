# Introdução

**Objetivo:** Realizar a elicitação de requisitos para o desenvolvimento de um software de apoio à gestão de uma padaria, onde os dados fiquem retidos localmente em um único estabelecimento.  

---

## Mini Mundo

A padaria **[INSIRA A PADARIA AQUI]** atua na região de **[INSIRA A REGIÃO AQUI]**, fornecendo produtos industrializados (refrigerantes, sorvetes, etc.) e suas receitas (pães, bolos, salgados, etc.) em um único estabelecimento. A equipe é composta por o dono, e mais 10 funcionários, divididos em equipes para realizar tarefas.  

- **Funcionários:**  
  - Podem executar múltiplas tarefas: atuar na cozinha, manter o estoque, atender clientes e registrar movimentações financeiras.  
  - Durante a manhã e tarde, 2 funcionários atendem os clientes e registram vendas.  

- **Dono:**  
  - Dono e principal chef, responsável pela produção das receitas.  
  - Administra o estoque de matéria-prima e controla o financeiro.  
  - Calcula o preço dos produtos com base no custo de produção e percentual/valor fixo de lucro.  

Atualmente, os registros de venda são feitos manualmente em um caderno. Não há cadastro de clientes ou vendas "fiadas". Os produtos são rotulados com:

- Nome  
- Descrição (ex.: bolo de chocolate de 500g com cerejas)  
- Preço de venda  
- Custo de produção  

---

## Requisitos Funcionais

### 1. Manter Ingredientes

- **Cadastrar:**  
  - ID (gerado automaticamente)
  - Nome  
  - Valor  
  - Tipo de unidade de medida (KG, G, Unidade, L, ML)  
  - Imagem  
  - Marca (opcional)  
  - Descrição (opcional)  
  - Data de validade (opcional)  
  - Data de registro  
  - Quantidade  
  - Quantidade mínima em estoque (opcional)  

- **Editar:**  
  - Nome  
  - Valor  
  - Tipo de unidade de medida  
  - Imagem  
  - Marca (opcional)  
  - Descrição (opcional)  
  - Data de validade (opcional)  
  - Quantidade  
  - Quantidade mínima em estoque (opcional)  

- **Remover:**  

- ID: Através do ID, o item será identificado e removido.

---

### 2. Gerenciamento de Preço de Produto

- **Cálculos:**  
  - Custo de produção (ingredientes * quantidades)  
  - Lucro (percentual ou valor fixo)  
  - Valor final (custo + lucro)  

---

### 3. Manter Produtos

- **Cadastrar:**  
  - ID (gerado automaticamente)  
  - Nome  
  - Custo de fabricação (calculado)  
  - Valor de venda  
  - Unidade de medida  
  - Imagem  
  - Descrição (opcional)  
  - Quantidade mínima em estoque (opcional)  
  - Data de validade (opcional)  

- **Editar:**  
  - Nome  
  - Recalcular custo de fabricação  
  - Recalcular valor de venda  
  - Descrição  
  - Quantidade em estoque  
  - Quantidade mínima em estoque  
  - Data de validade  

- **Remover:**  
  - ID: Através do ID, o item será identificado e removido.

- **Mostrar:**  
  - Imagem  
  - Nome  
  - Descrição  
  - Preço de venda  
  - Quantidade em estoque  

---

### 4. Controle de Estoque (Lote)

- **Atualização Automática:**  
  - Atualizar estoque após vendas ou recebimento de mercadorias.  

- **Relatórios de Estoque Mínimo:**  
  - Alertar quando a quantidade em estoque estiver abaixo do mínimo.  
  - Alertar quando um produto estiver próximo da data de validade.  

- **Histórico de Movimentação:**  
  - Registrar todas as transações relacionadas ao estoque.  

---

### 5. Manter Vendas

- **Adicionar Produtos:**  
  - Listar produtos disponíveis.  
  - Selecionar N produtos para venda.  
  - Garantir que a quantidade vendida não seja negativa ou maior que o estoque.  

- **Cálculo Automático:**  
  - Calcular o valor total da venda com base na quantidade e preço dos produtos.  

- **Registro de Vendas:**  
  - Registrar detalhes da transação:  
    - Produtos  
    - Valores  
    - Data (Dia/Mês/Ano/Hora/Minuto)  
    - Atualizar estoque automaticamente.  

---

### 6. Controle Financeiro

- **Relatórios Financeiros:**  
  - Balanço diário, semanal, mensal e anual.  
  - Demonstrativos em gráficos e dashboards.  

- **Análise de Vendas:**  
  - **Vendas X Produto:** Identificar produtos mais e menos vendidos.  
  - **Fluxo de Vendas:**  
    - Por horário (manhã, tarde, noite).  
    - Por intervalo de dias, semanas, meses ou anos.  

- **Análise Financeira:**  
  - Faturamento bruto e por produto.  
  - Vendas brutas (somatório total).  
  - Faturamento por data.  

---

### 7. Análise de Estoque

- **Categorias:** Ingredientes e Produtos.  
- **Fatores:**  
  - **Vencimento:** Contar itens vencidos.  
  - **Consumo:** Taxa média de consumo diário.  
  - **Permanência:** Tempo médio de permanência em estoque.  

---

### 8. Autenticação e Autorização

- **Controle de Acesso:**  
  - Login e senha.  
  - Níveis de acesso:  
        - **Dono:** Gerenciar todos os módulos.  
        - **Atendente:** Gerenciar produtos, vendas e ingredientes.  

---

## Requisitos Não Funcionais

### Usabilidade

- Interface amigável e fácil de usar.  

### Desempenho

- Resposta rápida mesmo com grande volume de dados.  
- Consultas otimizadas ao banco de dados.  

### Segurança

- Criptografia para dados sensíveis (login e senha).  
- Backup regular para evitar perda de dados.  

### Portabilidade

- Compatibilidade com diferentes dispositivos e sistemas operacionais (prioridade para Windows).  

### Manutenção

- Facilidade de atualização e correção.  
- Registro de logs para identificação de problemas.  

---
