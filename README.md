# Banco-De-dados
Projeto Conceitual – Oficina Mecânica

🚗 Oficina Mecânica – Esquema Conceitual

## 📖 Descrição
Este projeto apresenta o **esquema conceitual** de um sistema de controle e gerenciamento de **ordens de serviço (OS)** para uma **oficina mecânica**.  
O objetivo é estruturar as informações necessárias para controlar clientes, veículos, equipes de mecânicos, ordens de serviço, serviços prestados e peças utilizadas.

---

## 🏗️ Contexto da Narrativa
- Clientes levam veículos à oficina para conserto ou revisão.
- Cada veículo é designado a uma equipe de mecânicos.
- A equipe preenche uma **Ordem de Serviço (OS)** com data de entrega e status.
- O valor da OS é calculado a partir de:
  - Tabela de referência de mão de obra (serviços).
  - Peças utilizadas no reparo/revisão.
- O cliente deve autorizar a execução dos serviços.
- A mesma equipe avalia e executa os serviços.

---

## 📊 Entidades e Relacionamentos
- **Cliente** (id_cliente, nome, endereço, telefone)  
- **Veículo** (id_veiculo, placa, modelo, ano, marca, id_cliente)  
- **Mecânico** (id_mecanico, nome, endereço, especialidade)  
- **Equipe** (id_equipe, nome_equipe)  
- **Ordem de Serviço** (id_os, numero_os, data_emissao, valor_total, status, data_conclusao_prevista, id_veiculo, id_equipe)  
- **Serviço** (id_servico, descricao, valor_referencia)  
- **Peça** (id_peca, descricao, valor_unitario)  
- **OS_Serviço** (id_os, id_servico, quantidade, valor_total_servico)  
- **OS_Peça** (id_os, id_peca, quantidade, valor_total_peca)  

---

## 🔗 Principais Relacionamentos
- Cliente 1:N Veículo  
- Veículo 1:N Ordem de Serviço  
- Equipe 1:N Ordem de Serviço  
- Equipe N:N Mecânico  
- Ordem de Serviço N:N Serviço  
- Ordem de Serviço N:N Peça  

