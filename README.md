# Predição de Falhas em Compressor Industrial com Redes Neurais

Este projeto foi desenvolvido como meu **Trabalho de Conclusão de Curso (TCC)** entre agosto e dezembro de 2025 e representa meu primeiro projeto aplicado de Machine Learning.

O objetivo foi criar um modelo de rede neural capaz de classificar diferentes condições operacionais de um compressor industrial com base em dados de sensores.

---

## Sobre o Projeto

Este foi meu primeiro contato prático com:

- construção de modelos de Machine Learning
- redes neurais com TensorFlow/Keras
- pré-processamento de dados
- aplicação em um problema de engenharia

O projeto utiliza dados simulados de operação de um compressor industrial para prever sua condição de funcionamento.

---

## Dataset

O dataset utilizado foi gerado artificialmente com auxílio de Inteligência Artificial, com o objetivo de simular o comportamento de um compressor industrial em diferentes cenários.

Ele foi criado para:

- representar variáveis típicas de sensores industriais
- simular diferentes tipos de falhas
- permitir o desenvolvimento e teste do modelo

❗ Trata-se de um dataset sintético, utilizado exclusivamente para fins acadêmicos e criado artificialmente devido a dificuldade de acesso a dados de compressores reais.

---

## Dados Utilizados

- 20.000 registros  
- 10 variáveis de entrada  
- 1 variável alvo (`condicao`)  
- 10 classes de operação/falha  

### Variáveis de Entrada

- pressao_entrada_bar  
- pressao_saida_bar  
- temp_ar_saida_c  
- corrente_motor_a  
- vazao_m3h  
- vibracao_rms_mms  
- delta_p  
- temp_motor_c  
- horas_operacao  
- nivel_oleo_perc  

### Condições

- normal  
- superaquecimento  
- desgaste_rolamento  
- sobrecarga_eletrica  
- filtro_obstruido  
- vazamento  
- baixa_eficiencia  
- lubrificacao_insuficiente  
- partida_anomala  
- oscilacao_carga  

---

## Abordagem Utilizada

O fluxo implementado no notebook inclui:

1. Leitura do dataset em Excel  
2. Separação das variáveis de entrada e saída  
3. Codificação da variável alvo (LabelEncoder)  
4. Normalização dos dados (StandardScaler)  
5. Divisão em treino e validação  
6. Treinamento de uma rede neural multiclasses  
7. Uso de EarlyStopping para evitar overfitting  
8. Avaliação com métricas de treino (accuracy e loss)  
9. Salvamento do modelo e artefatos  
10. Criação de uma interface gráfica com Tkinter para predição manual  

---

## Modelo

Rede neural do tipo feedforward com:

- Camada densa (64 neurônios, ReLU)  
- Dropout (0.2)  
- Camada densa (32 neurônios, ReLU)  
- Dropout (0.2)  
- Camada de saída com Softmax  

### Configuração

- Otimizador: Adam  
- Função de perda: Sparse Categorical Crossentropy  
- Métrica: Accuracy  
- Treinamento com validação e EarlyStopping  

---

## Resultados

O notebook gera gráficos de:

- evolução da **accuracy**
- evolução da **loss**

Esses gráficos demonstram o comportamento do modelo durante o treinamento.

---

## Interface

O projeto inclui uma interface gráfica simples desenvolvida com Tkinter, permitindo:

- inserção manual dos dados de entrada  
- execução da predição  
- visualização da condição prevista pelo modelo  

<img width="323" height="485" alt="image" src="https://github.com/user-attachments/assets/20e81b89-425a-43f9-8182-8aa279f69604" />


---

## Exemplo de Previsão

O modelo recebe dados de sensores e retorna:

- classe prevista (condição do compressor)  
- distribuição de probabilidades  

<img width="398" height="377" alt="image" src="https://github.com/user-attachments/assets/73598dfa-51c1-4ab6-a75f-6cde24d82c8a" />


---

## Estrutura do Projeto

```
├── CriacaoRedeNeural.ipynb
├── dataset_compressor_balanceado.xlsx
├── modelo_compressor_excel.h5
├── scaler.pkl
├── label_encoder.pkl
├── training_history.csv
└── README.md
```

---

## Tecnologias Utilizadas

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- Tkinter  

---

## Como Executar

### 1. Clonar o repositório

```
git clone https://github.com/PetersonVital/industrial-compressor-failure-prediction-v1.git
cd industrial-compressor-failure-prediction-v1
```

### 2. Criar ambiente virtual (Python 3.10 recomendado)

```
py -3.12 -m venv .venv
.venv\Scripts\activate
```

### 3. Executar

Abra e rode o notebook:

```
CriacaoRedeNeural.ipynb
```
### 4. Preencher a interface que vai abrir

Adicionar os dados do compressor na interface que vai abrir e clicar em "prever" para obter as possibilidades de falha e os motivos.

---

## Aprendizados

Por ser meu primeiro projeto, este trabalho foi fundamental para desenvolver habilidades como:

- entendimento do fluxo completo de Machine Learning  
- pré-processamento de dados  
- treinamento de redes neurais  
- interpretação de métricas  
- integração de modelo com interface gráfica  

---

## Possíveis Melhorias

Caso eu vá evoluir o projeto, tenho possíveis ideias de imprlementação:

- métricas mais completas (Precision, Recall, F1-score)  
- matriz de confusão  
- comparação com outros modelos de ML  
- validação cruzada  
- uso de dados reais industriais  
- deploy como aplicação web (ex: Streamlit)  
- técnicas de explicabilidade (SHAP, LIME)  

---

Peterson Vital  
Engenheiro Mecânico | Data Analytics | Machine Learning  

LinkedIn: [https://www.linkedin.com/in/petersonvital](https://www.linkedin.com/in/petersonvital/)
