# Máquina de Lavar em Verilog 🚿🔧

Este projeto simula o funcionamento de uma máquina de lavar roupa utilizando **Verilog**, com simulação feita no **ISE Xilinx**.

## 🎯 Objetivo
Modelar uma **máquina de lavar controlada por uma FSM (Máquina de Estados Finita)** que executa um ciclo completo de lavagem, incluindo:

- Entrada de água
- Aquecimento
- Inserção de detergente
- Lavagem
- Enxaguamento
- Centrifugação
- Abertura da porta

## ⚙️ Funcionalidades

- **FSM com ciclos bem definidos**, controlada por sinais `start`, `pause` e `reset`.
- **Modo de proteção contra falha de energia**, permitindo retomar do último estado.
- **Atraso no início da lavagem**, útil para agendamento em horários específicos.

## 🛠️ Estrutura do Sistema

- **FSM** com transições baseadas em `clk`, `reset`, `start`, `pause`
- **Bloco combinatório** para definição das saídas em cada estado
- **Simulação no ISE Xilinx** para validar todas as transições

## 🧪 Casos de Teste

- Iniciar o ciclo e observar transições corretas
- Pausar e retomar o ciclo
- Verificar sequência entre lavagem → enxágue → centrifugação

## 🚀 Possíveis Expansões

- Temporização realista para cada fase
- Módulo de aquecimento com controle de temperatura
- Interface com display ou LEDs

## 📚 Conclusão

Projeto ideal para aprender lógica digital e FSMs, com aplicação prática e possibilidade de expansão futura.

