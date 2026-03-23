# Atividade Avaliativa 1 — Python

**Curso:** Administração  
**Aluna:** Letícia Santana  
**Professor:** Sérgio Monteiro  

---

## Como Executar no Google Colab

1. Acesse [https://colab.research.google.com](https://colab.research.google.com)
2. Clique em **"Arquivo" → "Fazer upload de notebook"**
3. Selecione o arquivo `.ipynb` deste projeto
4. Com o notebook aberto, clique em **"Ambiente de execução" → "Executar tudo"** (ou `Ctrl + F9`)
5. Os resultados aparecerão abaixo de cada célula de código

> Nenhuma instalação adicional é necessária — o Colab já possui Python e todas as funcionalidades usadas neste projeto.

---

## Questões

---

### Questão 1 — Classificação de Temperaturas

**Descrição:**  
Dada uma lista de temperaturas em graus Celsius, o programa classifica cada valor em uma categoria e conta quantas temperaturas pertencem a cada uma.

**Categorias:**
- `< 20°C` → Frio
- `20°C a 30°C` → Agradável
- `> 30°C` → Quente

**Lógica:**  
O código percorre cada temperatura da lista com um `for`. Para cada valor, uma estrutura `if / elif / else` determina a categoria. A classificação é adicionada a uma lista de resultados, e um dicionário `contagem_categorias` é incrementado a cada iteração para registrar o total por categoria.

**Saída esperada:**
```
Classificações das temperaturas: ['Frio', 'Agradável', 'Agradável', 'Quente', 'Agradável', 'Frio', 'Quente']
Contagem por categoria: {'Frio': 2, 'Agradável': 3, 'Quente': 2}
```

---

### Questão 2 — Sistema de Avaliação de Alunos

**Descrição:**  
Dada uma lista de notas, o programa classifica cada aluno e calcula o percentual de reprovados em relação ao total da turma.

**Categorias:**
- `< 5.0` → Reprovado
- `5.0 a 6.9` → Recuperação
- `≥ 7.0` → Aprovado

**Lógica:**  
O código usa um `for` para percorrer as notas. A cada iteração, o `if / elif / else` define a situação do aluno, que é armazenada em uma lista. Contadores separados acumulam aprovados, reprovados e em recuperação. Ao final, o percentual de reprovados é calculado dividindo a quantidade de reprovados pelo total de alunos e multiplicando por 100.

**Saída esperada:**
```
Classificações das notas: ['Reprovado', 'Recuperação', 'Aprovado', 'Aprovado', 'Recuperação', 'Aprovado']
Quantidade de alunos aprovados: 3
Percentual de alunos reprovados: 16.67%
```

---

### Questão 3 — Monitoramento de Consumo de Energia

**Descrição:**  
Dada uma lista com o consumo diário de energia em kWh durante uma semana, o programa identifica os dias de consumo elevado, calcula o total e a média, e emite um alerta se necessário.

**Critério de consumo alto:** acima de 180 kWh por dia.  
**Alerta:** disparado se mais de 2 dias ultrapassarem o limite.

**Lógica:**  
O `for` percorre a lista usando `enumerate()`, que fornece tanto o índice (número do dia) quanto o valor do consumo. A cada iteração, o consumo é somado a um acumulador. Se o valor ultrapassar 180 kWh, o dia e o consumo são salvos em uma lista de alertas. Após o loop, a média é calculada e, se houver mais de 2 dias com consumo alto, uma mensagem de alerta é exibida.

**Saída esperada:**
```
Dias com consumo alto (Dia, Consumo kWh):
  Dia 3: 200 kWh
  Dia 6: 220 kWh

Total de consumo da semana: 1050 kWh
Média semanal de consumo: 150.00 kWh

Consumo alto dentro dos limites aceitáveis (máximo 2 dias).
```

---

### Questão 4 — Simulação de Carrinho de Compras

**Descrição:**  
Dada uma lista de preços, o programa aplica descontos progressivos a cada item conforme seu valor, e calcula o total original, o total com desconto e a economia obtida.

**Tabela de descontos:**
| Preço do item | Desconto |
|---|---|
| Abaixo de R$ 50 | 5% |
| Entre R$ 50 e R$ 150 | 10% |
| Acima de R$ 150 | 15% |

**Lógica:**  
O `for` percorre cada preço da lista. Para cada item, o `if / elif / else` determina o percentual de desconto aplicável. O preço final é calculado multiplicando o preço original por `(1 - desconto)`, e os totais original e com desconto são acumulados separadamente. Ao final, a economia é obtida pela diferença entre os dois totais.

**Saída esperada:**
```
Preços originais: [50, 120, 30, 200, 80, 15]
Preços finais com desconto: ['45.00', '108.00', '28.50', '170.00', '72.00', '14.25']
Total da compra original: 495.00
Total da compra com desconto: 437.75
Economia total obtida: 57.25
```

---

## Conceitos de Python Utilizados

| Conceito | Aplicação |
|---|---|
| `for` | Percorrer listas em todas as questões |
| `if / elif / else` | Classificação por faixas de valor |
| Listas | Armazenar resultados e entradas |
| Dicionários | Contagem de categorias (Q1) |
| `enumerate()` | Obter índice e valor simultaneamente (Q3) |
| Acumuladores | Somar totais ao longo do loop |
| f-strings | Formatar saídas com casas decimais |
