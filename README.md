# RoleSemTreta

# Projetinho: Rolê sem Treta (Divisão Justa de Conta)

> **Disciplina:** Algoritmos e Programação - 1º Período  
> **Linguagem:** 

---

## O Problema Real

Final de semana, a turma da faculdade se reúne para fazer um churrasco ou sair para comer. No fim da noite, chega a conta. 

Na hora de pagar, surge o clássico impasse:
* Quem **não bebe refrigerante/cerveja** não acha justo pagar pela bebida dos outros.
* Quem é **vegetariano** não quer dividir a conta da picanha.
* Alguns chegaram mais tarde e só consumiram acompanhamentos.
* A taxa de serviço (10%) ou taxa do garçom é cobrada sobre o valor total, mas deve ser distribuída proporcionalmente ao gasto de cada um.

Tentar calcular isso de cabeça na calculadora do celular no meio do bar sempre gera confusão, erros no troco e alguém saindo no prejuízo.

---

## Objetivo do Algoritmo

Desenvolver um programa interativo via terminal para **calcular a divisão justa de despesas de um evento**, respeitando as restrições e restrições de consumo de cada participante.

---

## Decomposição 

**1. Cadastro dos participantes**

Quantas pessoas vão participar da divisão?
Nome (ou identificador) de cada participante.

**2. Cadastro dos itens consumidos**

Quais itens compõem a conta total (refrigerante, cerveja, acompanhamentos, etc.)?
Valor de cada item. Quem consumiu o quê?. Cada item precisa estar associado a um subconjunto de participantes (não a todos automaticamente).

**3. Cálculo do subtotal individual**

Para cada participante, somar apenas os itens que ele efetivamente consumiu.
Isso já resolve o caso do vegetariano e de quem não bebe (não entra na bebida).

**4. Tratamento de casos especiais**

Participantes que chegaram depois e só consumiram parte da conta.
Itens compartilhados por alguns, mas não todos (ex: uma entrada dividida por 3 de 6 pessoas), como ratear entre só quem consumiu.

**5. Cálculo da taxa de serviço (10%)**

Calcular o valor total da conta (soma de tudo).
Calcular a taxa de serviço total (10% do total).
Distribuir essa taxa proporcionalmente: cada pessoa paga 10% sobre o que ela mesma consumiu.

**6. Soma final por pessoa**

subtotal_pessoa + (subtotal_pessoa × 0.10) = valor final a pagar

**7. Conferência/validação**

Verificar se a soma de tudo que cada pessoa deve pagar bate com o valor total da conta (evitar erro de arredondamento, "sumiço" de centavos).
Tratar arredondamento (quem fica com o centavo a mais?).

**8. Interface com o usuário (entrada/saída via terminal)**

Como o programa vai perguntar essas informações (menu, loop de cadastro)?
Como vai exibir o resultado final de forma clara (ex: tabela com nome e valor a pagar)?

---
