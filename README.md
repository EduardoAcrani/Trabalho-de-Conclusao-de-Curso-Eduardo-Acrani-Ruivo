# Trabalho de Conclusão de Curso - Ciência de Dados Aplicada para Manutenção Preditiva

Projeto apresentado no Trabalho de Conclusão de Curso (TCC) de Eduardo Acrani Ruivo no curso de Engenharia de Controle e Automação da Universidade Feredal de Uberlândia (UFU), sob orientação do professor Dr. Josué Silva de Morais.

Link para o LinkdIn do Aluno: https://www.linkedin.com/in/eduardo-acrani-ruivo-0219041b7/
Link para os dados: https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification/data

## Introdução 

Neste projeto foi analisado dados sintéticos de máquinas para manutenção preditiva, uma vez que coletar dados reais é algo muito difícil e é ainda mais difícil encontrar uma empresa que divulgue tais dados. Com isso, foram utilizados os dados presentes no conjunto de dados nomeado de "Machine Predictive Maintenance Classification" que, refletem dados reais encontrados nas indústrias para manutenção preditiva.

Os dados foram analisados com os seguintes intuitos:
- Identificar a separabilidade nos dados dos equipamentos que sofreram falha dos que não sofreram;
- Identificar se alguma variável tem uma correlação direta com algum dos tipos de falha;
- Criar modelos para tentar prever quando o equipamento falhará e identificar qual tipo de falha, na expectativa de ajudar os setores de manutenção com seus planejamentos e prevenir quaisquer falhas indesejadas;

Após os dados serem analisados e passarem pelas devidas modificações, foram utilizados para treinar modelos de regressão logística, classificação e Ensemble da biblioteca [Scikit-Learn](https://scikit-learn.org/stable/).

Nota: Como os dataset tem um desbalanço de 96,52%-3,48% no Target, as expectativas devem ser reduzidas para o resultado obtido.

## Dataset

O dataset possui 10000 registros e 10 colunas, sendo:

* **UDI**: Identificador único na faixa de 1 até 10000

* **Product ID** - Consistindo em uma letra, sendo L para baixa (60% de todos os produtos), M para média (30%) e H para alta (10%) como variantes de qualidade do produto e um número de série específico da variante.

* **Type** - Consistindo em uma letra, sendo L para baixa (60% de todos os produtos), M para média (30%) e H para alta (10%) como variantes de qualidade do produto.

* **Air temperature [K]** - Temperatudra do Ar. Gerado usando um processo de passo aleatório e posteriormente normalizado para um desvio padrão de 2K em torno de 300K

* **Process temperature [K]** - Temperatudra do Processo. Gerado usando um processo de passo aleatório e posteriormente normalizado para um desvio padrão de 1K, adicionado à temperatura do ar mais 10K.

* **Rotational speed [rpm]** - Velocidade Rotacional. Calculado a partir de uma potência de 2860 W, sobreposta a um ruído normalmente distribuído.

* **Torque [Nm]** - Os valores de torque são normalmente distribuídos em torno de 40 Nm com Ïƒ = 10 Nm e sem valores negativos.

* **Tool wear [min]** - Desgaste do Equipamento. As variantes de qualidade H/M/L adicionam 5/3/2 minutos de desgaste da ferramenta usada no processo.

* **Target** - Valor alvo. Indica se o equipamento falou ou não alguma vez.

* **Failure Type** - Tipo de falha. Indica qual tipo de falha o equipamento teve, caso teve. São eles Heat Dissipation Failure (falha na dissipação de calor), Power Failure (falha na energia), Overstrain Failure (falha por sobretensão), Tool Wear Failure (falha por desgate do equipamento) e Random Failures (falha aleatória).

As informações acima foram retiradas da descrição dada pelo usuário que forneceu o conjunto de dados e foi traduzida e ajustada para melhor entendimento na língua portuguesa.