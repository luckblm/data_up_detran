# README

## Processamento e Análise da Frota de Veículos no Estado do Pará

Este repositório contém um script em R que realiza a limpeza, padronização e sumarização de dados sobre a frota de veículos no estado do Pará.

## Etapas do Processamento

### 1. Carregamento de Pacotes e Dados  
- Importa bibliotecas necessárias (`tidyverse`, `janitor`, `sf`, entre outras).  
- Lê arquivos CSV e RDS contendo informações sobre a frota de veículos e as regiões integradas.  
- Converte dados espaciais para o sistema de coordenadas adequado.  

### 2. Limpeza e Padronização de Dados  
- Ajusta os nomes das variáveis para um formato padronizado.  
- Corrige a capitalização de textos e preposições em nomes de municípios.  
- Normaliza categorias de veículos, cores, combustíveis e nacionalidade.  
- Agrupa algumas categorias em "Outros" para facilitar análises.  

### 3. Filtragem e Seleção de Colunas  
- Mantém apenas as colunas relevantes para análise.  
- Renomeia a coluna `ano_licenciado` para `ano` e filtra apenas veículos licenciados a partir do ano 2000.  

### 4. Agrupamento e Sumarização dos Dados  
- Calcula o total de veículos licenciados por município e por Região de Integração.  
- Agrega os dados por categoria, tipo de veículo, cor, combustível, espécie do veículo e nacionalidade.  
- Preenche valores ausentes com zero para evitar inconsistências.  

### 5. Criação de Tabelas Agregadas  
- Gera tabelas de estatísticas agrupadas, como:
  - Total de veículos licenciados por ano e localidade.  
  - Distribuição dos veículos por categoria, tipo, cor, combustível, espécie e nacionalidade.  
- Consolida os dados sumarizados em um único dataset (`frota`).  

### 6. Tratamento de Valores Ausentes  
- Substitui valores `NA` na contagem de veículos por zero para evitar inconsistências.  

## Utilização dos Dados

O código é essencial para preparar os dados antes de serem utilizados em visualizações e análises no **dashboard sobre veículos no Pará**.

Para executar o script, certifique-se de ter os pacotes necessários instalados e os arquivos de dados no diretório correto.

