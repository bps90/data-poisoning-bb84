# QUANTUM LAYER SIMULATIONS FOR DEFENSE AGAINST DATA POISONING

Este repositório contém o código de simulação para detecção de ataques de envenenamento de dados em camadas quânticas.

## 1. Descrição do Projeto
O projeto utiliza o simulador NetSquid para analisar o comportamento da Taxa de Erro de Bits Quânticos (QBER) no protocolo BB84. O objetivo é diferenciar estatisticamente um canal benigno (com ruído natural) de um canal sob ataque Man-in-the-Middle (MITM) do tipo Intercept-Resend.



## 2. Tecnologias e Dependências
* Simulador: NetSquid (Requer registro acadêmico em https://netsquid.org/).
* Linguagem: Python 3.11+.
* Bibliotecas: numpy, matplotlib, scipy, pandas.

## 3. Configurações da Simulação
Os parâmetros técnicos definidos para os experimentos são:
* Tamanho da Chave: 2000 qubits por bloco.
* Fidelidade do Canal: 0.83 (Atenuação de Beer-Lambert).
* Threshold de Segurança: 11.0% de QBER.
* Amostragem Estatística: 100 experimentos independentes.

## 4. Resultados Obtidos (Tabela I)
Abaixo estão as métricas reais geradas pela simulação no NetSquid (com 95% de confiança):

| Métrica | Valor Obtido | Intervalo de Confiança (95%) |
| :--- | :--- | :--- |
| True Positive Rate | 100.0% | 96.3% - 100.0% |
| False Positive Rate | 0.0% | 0.6% - 7.0% |
| Average QBER (Benign) | 8.6% | 8.4% - 8.9% |
| Average QBER (MitM) | 29.2% | 28.9% - 29.6% |



## 5. Como Executar
1. Instale as dependências listadas no arquivo requirements.txt:
   pip install -r requirements.txt
2. Execute o notebook Jupyter:
   jupyter notebook "QUANTUM LAYER SIMULATIONS FOR DEFENSE AGAINST DATA POISONING.ipynb"
