# 🗄️ Estudos de SQL para Suporte Técnico

Este repositório contém anotações práticas de estudos sobre a **linguagem SQL**, com foco no uso em **Suporte Técnico / Help Desk / Suporte a Sistemas**.

O objetivo é compreender consultas, análise de dados e apoio ao diagnóstico de problemas em sistemas que utilizam banco de dados.

---

## 📚 Conceitos Básicos de Banco de Dados

- Banco de dados armazena informações de forma organizada  
- SQL (Structured Query Language) é a linguagem utilizada para acessar os dados  
- Muito presente em sistemas corporativos, ERPs e aplicações internas  

---

## 🧩 Estrutura Básica de um Banco de Dados

Principais conceitos:

- **Banco de dados**  
- **Tabelas**  
- **Colunas (campos)**  
- **Linhas (registros)**  

---

## 🔍 Consultas Básicas (SELECT)

Consulta de dados em tabelas:

sql
SELECT * FROM clientes;

Selecionando colunas específicas:

SELECT nome, email FROM clientes;

## 🎯 Filtros com WHERE

Retorno de registros específicos:

SELECT *
FROM pedidos
WHERE status = 'aberto';

Uso no suporte:

Análise de registros
Validação de dados
Apoio a investigações de erro

## 📊 Ordenação de Dados (ORDER BY)

SELECT *
FROM chamados
ORDER BY data_abertura DESC;

## 🔢 Limitação de Resultados (LIMIT)

SELECT *
FROM logs
LIMIT 10;

## 🔗 Relacionamento entre Tabelas (JOIN)

Noções práticas de relacionamento:

SELECT clientes.nome, pedidos.id
FROM clientes
JOIN pedidos 
ON clientes.id = pedidos.cliente_id;

## 🧠 Funções Agregadas

Funções utilizadas para análise:

COUNT()
SUM()
AVG()
Exemplo:

SELECT COUNT(*) 
FROM chamados;

## 🔍 Subconsultas

Uso de subconsultas para análise de dados:

SELECT nome
FROM clientes
WHERE id IN (
    SELECT cliente_id
    FROM pedidos
    WHERE status = 'aberto'
);

Aplicação no suporte:

Cruzamento de informações
Investigação de problemas em sistemas
Análises mais detalhadas

## 🧱 CTE – Common Table Expressions (Conhecimento Prático Atual)

Utilização de CTE para organizar consultas complexas:

WITH pedidos_abertos AS (
    SELECT cliente_id
    FROM pedidos
    WHERE status = 'aberto'
)
SELECT *
FROM clientes
WHERE id IN (
    SELECT cliente_id 
    FROM pedidos_abertos
);

Benefícios das CTEs:

Melhor legibilidade
Organização das consultas
Facilita manutenção

## 👁️ Views (Conhecimento Básico)

Views são consultas armazenadas no banco
Facilitam reutilização de dados
Padronizam relatórios e consultas

## 📊 Consultas para Análise de Dados (Conhecimento Atual)

Uso combinado de:

JOIN
WHERE
CTE
Funções agregadas

Para:

Identificar padrões
Analisar volume de chamados
Verificar erros recorrentes
Apoiar decisões técnicas

## 🛠️ Aplicação do SQL no Suporte Técnico

Uso prático para:

Consulta de dados em sistemas
Validação de informações
Apoio ao atendimento ao cliente
Análise de erros e registros
Diagnóstico de falhas

## 🔒 Boas Práticas

Utilizar apenas comandos de consulta quando não autorizado
Conferir filtros antes de executar consultas
Evitar alterações diretas em produção
Proteger dados sensíveis

## 📌 Próximos Conteúdos a Evoluir

Otimização de consultas
Índices
Controle de permissões
Performance em grandes volumes de dados

## 🧠 Observações Pessoais

SQL é essencial para suporte a sistemas modernos
Facilita diagnósticos rápidos
Ajuda a entender o funcionamento das aplicações
Este conteúdo evolui conforme meus estudos

📅 Última atualização: Fevereiro / 2026
📈 Nível atual: Básico–intermediário prático em SQL para suporte técnico
