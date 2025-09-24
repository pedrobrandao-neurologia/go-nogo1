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
