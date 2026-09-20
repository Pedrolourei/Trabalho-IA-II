# Student Performance - Machine Learning

Projeto desenvolvido para a disciplina de Inteligência Artificial II
do curso de Sistemas de Informação da Faculdade Antonio Meneghetti (AMF).

## Objetivo

Desenvolver um modelo de Machine Learning capaz de classificar estudantes
como Aprovado ou Reprovado a partir do Student Performance Dataset.

O projeto também compara o desempenho dos modelos com e sem as notas
anteriores G1 e G2.

## Dataset

Foi utilizado o Student Performance Dataset, disponibilizado pelo
UCI Machine Learning Repository.

O arquivo utilizado foi `student-mat.csv`, referente à disciplina
de Matemática, contendo 395 estudantes.

A variável alvo `resultado` foi criada a partir da nota final G3:

- G3 >= 10: Aprovado
- G3 < 10: Reprovado

G3 não foi utilizada como atributo de entrada dos modelos.

## Tecnologias

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Google Colab

## Modelos utilizados

Foram avaliados:

- Regressão Logística
- Random Forest
- Random Forest com `class_weight="balanced"`
- Random Forest com G1 e G2

## Principais resultados

### Random Forest sem G1/G2

- Acurácia: 70,89%
- Recall Reprovado: 31%

### Random Forest com G1/G2

- Acurácia: 91,14%
- Precision Reprovado: 88%
- Recall Reprovado: 85%
- F1 Reprovado: 86%
- ROC-AUC: 0,975

Na validação cruzada estratificada com 5 folds:

- Accuracy média: 90,9% ± 3,3%
- Precision macro: 89,6% ± 3,7%
- Recall macro: 90,1% ± 4,3%
- F1 macro: 89,7% ± 3,9%
- Recall médio de Reprovado: 87,7% ± 7,8%

## Estrutura

## 📁 Estrutura do projeto

```text
student-performance-ml/
│
├── student_performance.ipynb
│
├── data/
│   └── student-mat.csv
│
├── models/
│   └── modelo_student_performance.pkl
│
├── reports/
│   └── Relatorio_Student_Performance_IA_II.pdf
│
├── images/
│
├── requirements.txt
├── .gitignore
└── README.md
```

## 🚀 Como executar

### 1. Clone o repositório

```bash
git clone URL_DO_REPOSITORIO
```

### 2. Entre na pasta do projeto

```bash
cd student-performance-ml
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Execute o notebook

Abra o arquivo:

`student_performance.ipynb`

O notebook também pode ser executado utilizando o Google Colab.

## 📊 Principais resultados

O modelo Random Forest com as notas G1 e G2 apresentou:

- Acurácia no conjunto de teste: **91,14%**
- Precision para Reprovado: **88%**
- Recall para Reprovado: **85%**
- F1-score para Reprovado: **86%**
- ROC-AUC: **0,975**

Na validação cruzada estratificada com 5 folds:

- Acurácia média: **90,9% ± 3,3%**
- F1 macro médio: **89,7% ± 3,9%**
- Recall médio para Reprovado: **87,7% ± 7,8%**

## 👨‍💻 Autor

**Pedro Henrique Loureiro de Avila**

Sistemas de Informação — AMF  
Inteligência Artificial II — 2026/02
