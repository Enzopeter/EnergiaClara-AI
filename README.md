# EnergiaClara AI 🌱

**Global Solution — Citizen Assist AI | Soluções em Energias Renováveis e Sustentáveis**

O **EnergiaClara AI** é um simulador didático independente, desenvolvido em **Python e Google Colab**, que compara duas alternativas para uma residência brasileira: **substituição de lâmpadas por LED** e **geração solar fotovoltaica**. O sistema oferece gráficos, cálculos de consumo, análises de custo e recomendações automáticas explicadas em linguagem acessível.

> **Aviso:** os resultados são estimativas, não uma previsão de fatura, orçamento de instalação nem promessa de economia. O assistente interpreta perguntas por regras e palavras-chave; não utiliza um modelo generativo de IA.

## Público e problema

O público-alvo são consumidores residenciais brasileiros, inclusive pessoas sem formação técnica em energia elétrica. O problema estudado é a dificuldade de avaliar quanto se pode economizar com eficiência energética e geração renovável, considerando custos, condições e limitações.

## Funcionalidades

- Formulário editável com consumo em kWh, tarifa, características das lâmpadas e parâmetros solares.
- Estimativa de consumo, custo e economia com LED.
- Estimativa de geração fotovoltaica, considerando potência, irradiação e desempenho do sistema.
- Consulta opcional à **NASA POWER** para climatologia histórica de irradiação de São Paulo, com alternativa manual identificada.
- Comparação de cenários, gráficos de energia/custos e análise de sensibilidade com 27 combinações.
- Assistente de perguntas frequentes que usa os resultados calculados.
- Testes automáticos, rastreabilidade das entradas e exportação de evidências.

## Como executar no Google Colab

1. Acesse https://colab.research.google.com/.
2. Escolha **Arquivo → Fazer upload de notebook** e envie `EnergiaClara_AI.ipynb`.
3. Selecione **Ambiente de execução → Executar tudo**.
4. Na **seção 3**, altere os parâmetros e execute as células seguintes para recalcular os resultados.
5. Consulte gráficos e tabelas, escreva perguntas na **seção 8** e verifique os testes nas seções 15 e 19.
6. Na **seção 22**, gere o pacote ZIP de evidências atualizado para os parâmetros escolhidos.

**Dependências utilizadas:** Python, pandas, matplotlib, requests e recursos do IPython/Colab. A consulta à NASA requer internet; o notebook dispõe de parâmetro manual quando a API não estiver acessível.

## Exemplo didático documentado

| Parâmetro ou resultado | Exemplo |
|---|---:|
| Consumo residencial | 250 kWh em 30 dias |
| Tarifa informada | R$ 0,90/kWh (hipótese) |
| Economia física com LED | 76,50 kWh em 30 dias |
| Geração fotovoltaica estimada | 108,69 kWh em 30 dias |
| Irradiação (HSP) | 4,53 h/dia — NASA POWER, climatologia histórica, São Paulo |
| Fator de aproveitamento financeiro solar | 75% (hipótese didática) |

**Não confundir:** geração solar, redução física de consumo e economia financeira são grandezas diferentes. A estimativa financeira simplifica a compensação de energia; não simula as regras completas de faturamento.

## Dados, metodologia e limitações

A pasta [`evidencias/`](evidencias/) contém o resultado numérico do cenário, parâmetros e sua origem, os cinco cenários sintéticos, análise de sensibilidade, referências, testes do assistente, regressão numérica e registros de usabilidade. Leia `resumo_da_analise.md`, `rastreabilidade_parametros.csv` e `referencias_metodologicas.csv` para entender as premissas.

Os custos e a tarifa iniciais são **hipóteses declaradas**. A irradiação da NASA é **histórica**, não geração medida. O modelo não reproduz tributos e regras específicas de créditos, custo mínimo, sombreamento, degradação, sazonalidade, financiamentos e outros fatores que afetam o resultado real.

## Testes e avaliação com usuário

O notebook registra **7 testes textuais**, **12 testes de regressão** e **3 testes de formatação**, além de um teste real de usabilidade identificado como **P1**. P1 conseguiu utilizar o simulador, compreendeu os gráficos e considerou o uso fácil. Sugeriu organizar melhor as respostas; a seção 8 foi reorganizada com tópicos e ressalvas. **O reteste dessa alteração por P1 não foi realizado**. Detalhes em [`evidencias/registros_testes_reais.csv`](evidencias/registros_testes_reais.csv).

## Estrutura do repositório

```text
EnergiaClara_AI/
├── README.md
├── EnergiaClara_AI.ipynb
└── evidencias/
    ├── resumo_da_analise.md
    ├── resultado_energetico.csv
    ├── rastreabilidade_parametros.csv
    ├── registros_testes_reais.csv
    └── ... demais evidências e testes
```

## Referências

As fontes metodológicas e suas utilizações estão listadas em [`evidencias/referencias_metodologicas.csv`](evidencias/referencias_metodologicas.csv). Dentre elas: [ANEEL](https://www.gov.br/aneel/pt-br), [NASA POWER](https://power.larc.nasa.gov/) e [Inmetro](https://www.gov.br/inmetro/pt-br).

## Equipe

**Preencher antes da entrega:** nomes completos e RMs de todos os integrantes.

## Entrega da disciplina

A entrega final solicitada pelo professor é **um arquivo `.txt`** contendo os nomes e RMs dos integrantes, o link do GitHub e o link do vídeo técnico **não listado no YouTube**, com duração máxima de **3 minutos**. O vídeo é a etapa posterior à publicação do repositório.
