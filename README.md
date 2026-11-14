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
2. Escolha **Arquivo → Fazer upload de notebook** e envie `EnergiaClara.ipynb`.
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

O [pacote de evidências](EnergiaClara_AI_Evidencias_CandidatoFinal.zip) contém os resultados numéricos, parâmetros, cenários sintéticos, análise de sensibilidade, referências, testes automatizados e registros de usabilidade.
  
Os custos e a tarifa iniciais são **hipóteses declaradas**. A irradiação da NASA é **histórica**, não geração medida. O modelo não reproduz tributos e regras específicas de créditos, custo mínimo, sombreamento, degradação, sazonalidade, financiamentos e outros fatores que afetam o resultado real.

## Testes e avaliação com usuário

O notebook registra **7 testes textuais**, **12 testes de regressão** e **3 testes de formatação**, além de um teste real de usabilidade identificado como **P1**. P1 conseguiu utilizar o simulador, compreendeu os gráficos e considerou o uso fácil. Sugeriu organizar melhor as respostas; a seção 8 foi reorganizada com tópicos e ressalvas. **O reateste dessa alteração por P1 não foi realizado**.  Os detalhes do teste com P1 estão disponíveis no arquivo `registros_testes_reais.csv`, incluído no [pacote de evidências](EnergiaClara_AI_Evidencias_CandidatoFinal.zip).

## Estrutura do repositório

```text
EnergiaClara-AI/
├── README.md
├── EnergiaClara.ipynb
└── EnergiaClara_AI_Evidencias_CandidatoFinal.zip
```

## Referências


As fontes metodológicas estão documentadas no arquivo `referencias_metodologicas.csv`, incluído no [pacote de evidências](EnergiaClara_AI_Evidencias_CandidatoFinal.zip). Entre elas estão ANEEL, NASA POWER e Inmetro.


## Equipe

- **Caio Henrique Ferraz da Silva** — RM 568992
- **Enzo Caruso Peter** — RM 570908

**Instituição:** FIAP  
**Curso:** Ciência da Computação  
**Turma:** 1CCPG

## Entrega da disciplina

Projeto desenvolvido para a Global Solution — Citizen Assist AI, na disciplina de Soluções em Energias Renováveis e Sustentáveis.

O repositório reúne o notebook executável, a fundamentação matemática, os resultados energéticos, as referências e as evidências dos testes.

**Vídeo de apresentação:** a adicionar após a gravação.

**Execução:** abrir o arquivo `EnergiaClara.ipynb` no Google Colab e executar todas as células.
