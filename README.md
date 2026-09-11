# 📊 Simulador de Investimentos em Fundos Imobiliários (FIIs)

## 📌 Sobre o projeto

Este projeto foi desenvolvido como parte de um desafio prático de **Microsoft Excel**, com o objetivo de aplicar conceitos de Excel na criação de uma ferramenta para **simulação de investimentos em Fundos de Investimento Imobiliário (FIIs)**.

A planilha permite que o usuário configure diferentes parâmetros financeiros e simule a evolução de seus investimentos ao longo do tempo, além de estimar o patrimônio acumulado, os dividendos mensais e uma possível distribuição dos aportes entre diferentes tipos de FIIs de acordo com o perfil do investidor.

O projeto busca transformar informações financeiras em uma ferramenta simples e automatizada para análise de diferentes cenários de investimento.

---

## 🎯 Objetivo

O objetivo da ferramenta é auxiliar o usuário na simulação e no planejamento de investimentos em FIIs, respondendo perguntas como:

* Quanto investir mensalmente?
* Por quanto tempo investir?
* Qual patrimônio pode ser acumulado?
* Quanto esse patrimônio pode gerar em dividendos?
* Como o valor investido pode ser distribuído entre diferentes categorias de FIIs?
* Como diferentes horizontes de investimento impactam o patrimônio acumulado?

---

## ⚙️ Funcionalidades

### 💰 Configuração financeira

A planilha possui uma área de configurações em que o usuário pode informar seu **salário** e a **rentabilidade estimada da carteira**.

A partir do salário informado, a ferramenta calcula automaticamente uma **sugestão de investimento correspondente a 30% da renda**.

Isso permite ao usuário utilizar sua própria realidade financeira como ponto de partida para as simulações.

---

### 📈 Simulação do investimento mensal

O usuário pode definir:

* Quanto deseja investir por mês;
* Por quantos anos pretende investir;
* A taxa de rendimento mensal esperada.

A partir desses parâmetros, a planilha calcula automaticamente o **patrimônio acumulado ao final do período**.

Para realizar essa projeção, foi utilizada a função financeira `FV` do Excel, responsável pelo cálculo do valor futuro de um investimento considerando aportes periódicos e uma determinada taxa de rendimento.

---

### 💵 Estimativa de dividendos

Além do patrimônio acumulado, a ferramenta estima os **dividendos mensais** que poderiam ser gerados pelo patrimônio projetado.

O cálculo utiliza o patrimônio acumulado e a taxa de rendimento da carteira definida na área de configurações.

Dessa forma, o usuário consegue visualizar não apenas o patrimônio potencial, mas também uma estimativa da renda mensal que esse patrimônio poderia proporcionar.

---

### ⏳ Simulação por horizonte de investimento

Para facilitar a comparação entre diferentes estratégias de longo prazo, a planilha apresenta projeções automáticas para:

* **2 anos**
* **5 anos**
* **10 anos**
* **20 anos**
* **30 anos**

Para cada período são calculados:

* Patrimônio acumulado;
* Dividendos mensais estimados.

Essa comparação permite visualizar de maneira prática o impacto do tempo e dos aportes recorrentes na construção de patrimônio.

---

## 👤 Perfil do investidor

A ferramenta também possui uma funcionalidade para simular a distribuição do investimento de acordo com diferentes **perfis de investidor**.

Foram considerados três perfis:

* 🟢 Conservador
* 🟡 Moderado
* 🔴 Agressivo

Cada perfil possui uma distribuição percentual diferente entre as categorias de Fundos Imobiliários disponíveis na ferramenta.

---

## 🏢 Categorias de FIIs

A carteira simulada considera seis categorias:

| Tipo de FII         | Característica geral                                                      |
| ------------------- | ------------------------------------------------------------------------- |
| **Papel**           | Fundos com maior exposição a títulos e recebíveis imobiliários            |
| **Tijolo**          | Fundos que investem diretamente em imóveis físicos                        |
| **Híbridos**        | Fundos que combinam diferentes estratégias e tipos de ativos              |
| **FOFs**            | Fundos que investem em cotas de outros Fundos Imobiliários                |
| **Desenvolvimento** | Fundos relacionados ao desenvolvimento de projetos imobiliários           |
| **Hotelarias**      | Fundos com exposição a hotéis e empreendimentos relacionados à hospedagem |

A distribuição entre essas categorias é alterada de acordo com o perfil selecionado.

---

## 🧮 Distribuição automática da carteira

Após selecionar o perfil do investidor, a planilha consulta uma tabela auxiliar contendo os percentuais definidos para cada combinação entre **perfil e tipo de FII**.

A função `VLOOKUP` é utilizada para buscar automaticamente o percentual correspondente.

Com isso, a ferramenta calcula quanto do aporte mensal deveria ser destinado a cada categoria.

Por exemplo, no perfil **Moderado**, utilizado como exemplo na planilha, o aporte é distribuído entre Papel, Tijolo, Híbridos, FOFs, Desenvolvimento e Hotelarias conforme os percentuais cadastrados na base auxiliar.

---

## 🛠️ Recursos do Excel utilizados

Durante o desenvolvimento da ferramenta foram aplicados diferentes conceitos e funcionalidades do Excel, incluindo:

* Fórmulas matemáticas;
* Fórmulas financeiras;
* Função `FV` para cálculo de valor futuro;
* Função `VLOOKUP` para busca de informações;
* Referências relativas e absolutas;
* Cálculos percentuais;
* Tabela auxiliar de dados;
* Automatização de cálculos;
* Simulação de cenários;
* Organização e formatação de informações financeiras.

---

## 📂 Estrutura da planilha

O arquivo possui duas abas principais:

### `Página1`

Contém a interface principal da ferramenta, incluindo:

* Configurações financeiras;
* Sugestão de investimento;
* Simulação dos aportes mensais;
* Projeção do patrimônio;
* Estimativa dos dividendos;
* Comparação entre diferentes períodos;
* Seleção do perfil;
* Distribuição sugerida entre categorias de FIIs.

### `Página2`

Funciona como uma **base auxiliar** para a ferramenta.

Nela estão armazenadas as combinações entre:

* Perfil do investidor;
* Tipo de FII;
* Percentual de alocação.

Essas informações são consultadas automaticamente pela planilha principal por meio da função `VLOOKUP`.

---

## 📁 Estrutura do repositório

```text
simulador-investimentos-fii-excel/
│
├── README.md
└── simulador_fii.xlsx
```

---

## 🚀 Como utilizar

1. Faça o download do arquivo `simulador_fii.xlsx`.
2. Abra a planilha no Microsoft Excel.
3. Na área **Configurações**, informe seu salário e a taxa de rendimento da carteira.
4. Defina quanto deseja investir mensalmente.
5. Informe o período do investimento.
6. Defina a taxa de rendimento mensal esperada.
7. Analise o patrimônio acumulado e os dividendos mensais projetados.
8. Compare os resultados para 2, 5, 10, 20 e 30 anos.
9. Selecione o perfil de investidor desejado.
10. Analise a distribuição sugerida do aporte entre as diferentes categorias de FIIs.

---

## 📊 Exemplo de funcionamento

A lógica da ferramenta pode ser resumida da seguinte forma:

```text
Salário
   ↓
Sugestão de investimento
   ↓
Aporte mensal + Prazo + Rentabilidade
   ↓
Projeção do patrimônio
   ↓
Estimativa de dividendos
   ↓
Perfil do investidor
   ↓
Distribuição entre categorias de FIIs
```

Dessa forma, a planilha reúne em uma única ferramenta conceitos de **planejamento financeiro, juros compostos, projeção patrimonial e alocação de investimentos**.

---

## 📚 Aprendizados desenvolvidos

O desenvolvimento deste projeto permitiu aplicar na prática conhecimentos relacionados a:

* Construção e estruturação de planilhas;
* Automatização de cálculos no Excel;
* Utilização de funções financeiras;
* Funções de busca e referência;
* Organização de bases auxiliares;
* Simulação de cenários;
* Matemática financeira;
* Planejamento de investimentos;
* Organização e visualização de informações.

Além dos conhecimentos técnicos de Excel, o projeto também permitiu desenvolver uma visão mais prática sobre como ferramentas de análise podem ser utilizadas para transformar dados e parâmetros financeiros em informações úteis para tomada de decisão.

---

## ⚠️ Aviso

Este projeto foi desenvolvido exclusivamente para **fins educacionais**.

Os percentuais, rentabilidades e resultados apresentados são utilizados para fins de simulação e não representam garantia de retorno ou recomendação de investimento.

Antes de realizar qualquer investimento, é importante analisar os riscos envolvidos e, quando necessário, buscar orientação de um profissional qualificado.

---

## 👨‍💻 Autor

**Gustavo Campanholi de Castro**

Projeto desenvolvido como parte de um desafio prático de Excel para criação de uma ferramenta de simulação de investimentos em Fundos Imobiliários.
