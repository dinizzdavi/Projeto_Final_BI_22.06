# Celnet Analytics: Otimização de Performance Comercial

**Autor:** Davi Veras Diniz  
**Disciplina:** Business Intelligence II  
**Professor:** MsC Pedro H. Mello  
**Empresa Estudada:** Grupo Celnet (Agente Autorizado Claro - Planaltina/DF)

---

## 🚀 Sobre o Projeto
Este repositório contém a solução de Business Intelligence desenvolvida para o Grupo Celnet. O objetivo principal é transformar os dados manuais de ativações celulares em um ecossistema analítico automatizado (*Data-Driven*), focando no controle de descontos, monitoramento de margem de lucro e eficiência no processo de auditoria de vendas.

## 🗂️ Modelagem dos Dados
O projeto foi estruturado seguindo o modelo **Star Schema (Esquema Estrela)** puro, garantindo integridade e performance ao motor do Power BI:
* **Tabela Fato:** `Fato_Vendas` (Granularidade por transação de venda, incluindo métricas de margem, custo e o status da auditoria).
* **Tabelas Dimensão:** `Dim_Lojas`, `Dim_Vendedores`, `Dim_Produtos`, `Dim_Clientes` e `Dim_Calendario` (criada via DAX).

## 🔐 Governança e Segurança (RLS)
Foram implementados dois papéis de Segurança em Nível de Linha:
1. **Gerente Aguas Claras:** Filtra a tabela `Dim_Lojas` para exibir apenas dados locais da filial.
2. **Direcao:** Acesso global e irrestrito a todas as margens e canais da empresa.
