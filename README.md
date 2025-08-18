# Análise Exploratória de Dados - Falhas Industriais

## Descrição do Projeto

Este projeto implementa uma **Análise Exploratória de Dados (EDA)** abrangente utilizando R Markdown para análise de dados de falhas industriais. O objetivo é realizar uma investigação detalhada dos padrões, tendências e características dos dados do parceiro através de técnicas estatísticas e visualizações interativas.

## Estrutura do Projeto

```
ponderada-s1-m11/
├── README.md                    # Documentação do projeto
├── Untitled.Rmd               # Notebook principal de análise
├── Untitled.html              # Relatório gerado em HTML
└── ponderada-s1-m11.Rproj     # Projeto RStudio
```

## Objetivo da Atividade

Desenvolver um documento R Markdown que gere saídas em PDF ou HTML contendo uma análise exploratória completa dos dados de falhas industriais, seguindo as melhores práticas de análise de dados e visualização.

## Dataset Analisado

O projeto analisa o dataset **InteliFalhas.csv**, que contém informações sobre falhas detectadas em sistemas industriais, incluindo:

### Variáveis do Dataset:

- **ID**: Identificação única de cada ocorrência
- **DATA_DETECCAO**: Data e hora da detecção da falha
- **PONTO**: Localização geral da falha
- **LOC_ID**: Código identificador do local
- **LOC**: Descrição do local específico
- **POS_ID**: Código de posição
- **POS**: Posição detalhada
- **TYPE_ID**: Código do tipo de falha
- **TYPE_TEXT**: Descrição do tipo de falha
- **VIEW_ID**: Código de visualização
- **COLUNA**: Coluna da falha
- **LINHA**: Linha da falha

## Metodologia de Análise

### 1. Preparação dos Dados

- **Carregamento**: Importação e estruturação do dataset
- **Limpeza**: Tratamento de valores ausentes e inconsistências
- **Transformação**: Conversão de tipos de dados apropriados
- **Validação**: Verificação da integridade dos dados

### 2. Análise Exploratória Implementada

#### **Análise Univariada**

- Distribuição dos tipos de falha mais frequentes
- Identificação de outliers através de boxplots
- Estatísticas descritivas das variáveis numéricas

#### **Análise Bivariada**

- Relação entre pontos de falha e tipos de erro
- Matriz de correlação entre variáveis numéricas
- Análise de associações entre variáveis categóricas

#### **Análise Multivariada**

- **PCA (Principal Component Analysis)**: Redução de dimensionalidade
- **Scree Plot**: Análise da variância explicada por componente
- Identificação de padrões complexos nos dados

## Tecnologias Utilizadas

### Linguagem e Ambiente

- **R**: Linguagem principal para análise de dados
- **R Markdown**: Framework para documentação reproduzível
- **RStudio**: Ambiente de desenvolvimento integrado

### Principais Bibliotecas

```r
library(tidyverse)    # Manipulação e visualização de dados
library(ggplot2)      # Visualizações avançadas
library(dplyr)        # Manipulação eficiente de dados
library(FactoMineR)   # Análise fatorial e PCA
library(corrplot)     # Visualização de matrizes de correlação
```

## Principais Descobertas

### Padrões Identificados

- **Falhas Recorrentes**: Identificação de tipos de falha que ocorrem com maior frequência
- **Correlações Espaciais**: Associações significativas entre `LOC_ID`, `POS_ID`, `TYPE_ID` e `VIEW_ID`
- **Outliers Críticos**: Posições específicas com concentração anômala de falhas
- **Redundância de Variáveis**: Componentes principais explicam a maior parte da variância

### Insights Estratégicos

- Alguns tipos de falha são persistentes, indicando necessidade de intervenção preventiva
- Existem padrões geográficos nas falhas que podem orientar manutenção direcionada
- A análise de componentes principais sugere oportunidades de simplificação do monitoramento

## Como Executar

### Pré-requisitos

1. **R** (versão 4.0 ou superior)
2. **RStudio** (recomendado)
3. Pacotes R necessários (instalação automática no primeiro chunk)

### Execução

1. Clone o repositório ou baixe os arquivos
2. Abra o arquivo `ponderada-s1-m11.Rproj` no RStudio
3. Execute o arquivo `Untitled.Rmd`:
   - Para HTML: `Ctrl+Shift+K` ou botão "Knit"
   - Para PDF: Altere `output: html_document` para `output: pdf_document` no cabeçalho YAML

### Configuração do Dataset

⚠️ **Importante**: Atualize o caminho do arquivo CSV na linha 21 do `Untitled.Rmd`:

```r
data <- read.csv("CAMINHO/PARA/SEU/InteliFalhas.csv")
```

## Resultados e Outputs

### Relatório HTML

- Documento interativo com visualizações dinâmicas
- Navegação facilitada entre seções
- Gráficos de alta qualidade para apresentação

### Análises Estatísticas

- Estatísticas descritivas completas
- Visualizações exploratórias profissionais
- Insights documentados e interpretados

## Próximos Passos

### Melhorias Sugeridas

1. **Modelagem Preditiva**: Implementação de algoritmos de machine learning
2. **Análise Temporal**: Exploração de padrões temporais nas falhas
3. **Dashboard Interativo**: Desenvolvimento de interface para monitoramento em tempo real
4. **Análise de Severidade**: Classificação e priorização de tipos de falha

### Oportunidades de Expansão

- Integração com sistemas de monitoramento em tempo real
- Desenvolvimento de alertas automatizados
- Análise comparativa com dados históricos
- Implementação de técnicas de deep learning para detecção de anomalias

## Estrutura Técnica

### Formato de Saída

- **HTML**: Relatório interativo para visualização web
- **PDF**: Documento formal para documentação técnica

### Reprodutibilidade

- Código completamente documentado
- Seed fixada para resultados consistentes
- Versionamento de pacotes explícito

---

## Autor

**Antonio Nassar**  
Data: 12 de Fevereiro de 2025

## Licença

Este projeto é desenvolvido para fins educacionais como parte do Módulo 11 - Inteli.
