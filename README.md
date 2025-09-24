# Tarefa Go-NoGo - Teste de Controle Inibitório

## Sobre
Implementação web da tarefa Go-NoGo para avaliação de controle inibitório e atenção sustentada.

## Características
- Teste reduzido (36 tentativas) ou completo (72 tentativas)
- Feedback visual e sonoro em tempo real
- Exportação de dados (CSV e JSON)
- Análise estatística automática (d', beta, TR)
- Totalmente responsivo e funciona offline

## Como Usar
1. Acesse: [seu-usuario.github.io/gonogo-task]
2. Escolha o tipo de teste
3. Siga as instruções na tela
4. Exporte os resultados ao final

## Análise de Dados
No console do navegador:
- `GoNoGo.analisarDados()` - Ver estatísticas agregadas
- `GoNoGo.exportarTodosDados()` - Exportar todos os dados salvos
- `GoNoGo.limparDados()` - Limpar dados locais


# 🧠 Tarefa Go-NoGo - Sistema de Avaliação de Controle Inibitório

[![Version](https://img.shields.io/badge/version-2.0-blue.svg)](https://github.com/seu-usuario/gonogo-task)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-Ready-orange.svg)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://www.ecma-international.org/ecma-262/)
[![Responsive](https://img.shields.io/badge/Responsive-Mobile%20Ready-purple.svg)](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)

## 📋 Índice

- [Visão Geral](#-visão-geral)
- [Características](#-características)
- [Demonstração](#-demonstração)
- [Instalação e Uso](#-instalação-e-uso)
- [Como Funciona](#-como-funciona)
- [Métricas e Análises](#-métricas-e-análises)
- [Exportação de Dados](#-exportação-de-dados)
- [API JavaScript](#-api-javascript)
- [Configurações](#-configurações)
- [Estrutura dos Dados](#-estrutura-dos-dados)
- [Análise Estatística](#-análise-estatística)
- [Requisitos Técnicos](#-requisitos-técnicos)
- [Troubleshooting](#-troubleshooting)
- [Contribuindo](#-contribuindo)
- [Citação](#-citação)
- [Licença](#-licença)
- [Contato](#-contato)

## 🎯 Visão Geral

A **Tarefa Go-NoGo** é uma implementação web moderna e cientificamente validada do paradigma clássico de avaliação neuropsicológica usado para medir controle inibitório, atenção sustentada e impulsividade. Esta ferramenta é amplamente utilizada em pesquisas sobre TDAH, funções executivas, neurociência cognitiva e psicologia experimental.

### O que é a Tarefa Go-NoGo?

É um teste cognitivo onde os participantes devem:
- **Responder rapidamente** (GO) a estímulos-alvo (círculos coloridos)
- **Inibir a resposta** (NO-GO) a estímulos distratores (círculo preto)

## ✨ Características

### 🎮 Interface e Experiência
- **Design Responsivo**: Funciona perfeitamente em desktop, tablet e mobile
- **Modo Tela Cheia**: Minimiza distrações durante o teste
- **Feedback em Tempo Real**: Visual (✓/✗) e sonoro para cada resposta
- **Barra de Progresso**: Acompanhamento visual do andamento do teste
- **Interface Intuitiva**: Instruções claras e design amigável

### 📊 Coleta de Dados
- **Precisão Temporal**: Uso de `performance.now()` para medições em milissegundos
- **Metadados Completos**: Navegador, resolução de tela, timestamps
- **Ordem Aleatória**: Algoritmo Fisher-Yates para randomização
- **Identificação Única**: Sistema de IDs para cada tentativa e participante

### 💾 Exportação e Armazenamento
- **CSV Detalhado**: Dados brutos trial-by-trial
- **CSV Resumido**: Estatísticas agregadas
- **JSON Completo**: Estrutura completa de dados
- **LocalStorage**: Armazenamento local automático
- **Análise Agregada**: Ferramentas para análise multi-participante

### 📈 Análises Estatísticas
- **Teoria de Detecção de Sinal**: d' (d-prime) e β (beta)
- **Métricas de Desempenho**: Acurácia, tempos de reação, variabilidade
- **Tipos de Erro**: Omissão e comissão
- **Estatísticas Descritivas**: Médias, desvios-padrão, percentuais

## 🚀 Demonstração

[🔗 Teste ao vivo](https://seu-usuario.github.io/gonogo-task)

### Screenshots

```
┌─────────────────────────────────┐
│      TAREFA GO-NOGO            │
│                                 │
│   ┌─────────────────────┐      │
│   │    Instruções       │      │
│   │  • Colorido = CLIQUE│      │
│   │  • Preto = NÃO      │      │
│   └─────────────────────┘      │
│                                 │
│   [Teste Reduzido] [Completo]  │
│                                 │
│         ⭕ (estímulo)           │
│                                 │
│    [████████░░░░] 60%          │
└─────────────────────────────────┘
```

## 🛠 Instalação e Uso

### Opção 1: GitHub Pages (Recomendado)

1. **Fork este repositório**
   ```bash
   git clone https://github.com/seu-usuario/gonogo-task.git
   cd gonogo-task
   ```

2. **Configure GitHub Pages**
   - Vá em Settings → Pages
   - Source: Deploy from a branch
   - Branch: main / root
   - Salve e aguarde o deploy

3. **Acesse sua aplicação**
   ```
   https://seu-usuario.github.io/gonogo-task
   ```

### Opção 2: Servidor Local

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server

# Acesse: http://localhost:8000
```

### Opção 3: Deploy Direto

Simplesmente abra o arquivo `index.html` em qualquer navegador moderno.

## 🎮 Como Funciona

### Para Participantes

1. **Início do Teste**
   - Escolha entre teste reduzido (36 tentativas, ~3 min) ou completo (72 tentativas, ~5 min)
   - Leia as instruções cuidadosamente
   - Opcionalmente, ative o modo tela cheia

2. **Durante o Teste**
   - **Círculo Colorido** (vermelho/verde/azul) → CLIQUE rapidamente
   - **Círculo Preto** → NÃO clique
   - Receba feedback imediato (som e símbolo)
   - Acompanhe seu progresso na barra superior

3. **Após o Teste**
   - Visualize suas estatísticas imediatamente
   - Insira seu identificador único
   - Baixe seus resultados em CSV ou JSON

### Para Pesquisadores

1. **Configuração**
   ```javascript
   // Personalize no código:
   const CONFIG = {
       DURACAO_ESTIMULO: 1000,        // ms
       INTERVALO_INTER_ESTIMULO: 700, // ms
       CORES_GO: ['#FF6B6B', '#4ECDC4', '#45B7D1'],
       COR_NOGO: '#2C3E50'
   };
   ```

2. **Coleta de Dados**
   - Distribua o link para participantes
   - Oriente sobre o identificador único
   - Colete arquivos CSV/JSON ao final

3. **Análise**
   - Use scripts R/Python para análise agregada
   - Importe CSVs diretamente no SPSS/JASP
   - Use a API JavaScript para análises no navegador

## 📊 Métricas e Análises

### Métricas Primárias

| Métrica | Descrição | Fórmula | Interpretação |
|---------|-----------|---------|---------------|
| **Taxa de Acertos GO** | % de respostas corretas em tentativas GO | (Acertos GO / Total GO) × 100 | > 80% = bom desempenho |
| **Tempo de Reação (TR)** | Velocidade média de resposta | Σ(TR
