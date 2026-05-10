# Desafio DIO - AWS Step Functions

## Descrição

Este repositório foi desenvolvido como parte do laboratório da DIO com foco em AWS Step Functions.

O objetivo do desafio foi compreender como funcionam workflows automatizados utilizando máquinas de estado na AWS, além de documentar o aprendizado adquirido durante as aulas práticas.

---

# Objetivos do Laboratório

- Entender o funcionamento do AWS Step Functions
- Criar workflows automatizados
- Compreender máquinas de estado
- Executar fluxos de processamento
- Registrar execuções e monitoramento
- Documentar todo o processo utilizando GitHub

---

# O que são AWS Step Functions?

AWS Step Functions é um serviço da AWS utilizado para orquestrar processos distribuídos utilizando máquinas de estado.

Com ele é possível:

- Automatizar fluxos de trabalho
- Integrar múltiplos serviços AWS
- Controlar execuções passo a passo
- Implementar tratamento de erros
- Criar workflows serverless

---

# Conceitos Aprendidos

## State Machine

A máquina de estados define o fluxo de execução da aplicação.

Cada etapa do processo é chamada de "State".

---

## Tipos de States

### Task
Executa uma ação específica.

### Choice
Cria decisões condicionais.

### Wait
Adiciona tempo de espera entre etapas.

### Parallel
Executa fluxos em paralelo.

### Succeed
Finaliza o fluxo com sucesso.

### Fail
Finaliza o fluxo com erro.

---

# Exemplo de Workflow

Exemplo simples de fluxo:

1. Início da execução
2. Validação de dados
3. Processamento
4. Tratamento de erros
5. Finalização

---

# Exemplo de definição JSON

```json
{
  "Comment": "Exemplo simples de State Machine",
  "StartAt": "Validacao",
  "States": {
    "Validacao": {
      "Type": "Pass",
      "Next": "Processamento"
    },
    "Processamento": {
      "Type": "Pass",
      "End": true
    }
  }
}
