# LH_CD_VitoriaFreire
# Projeto de Análise Exploratória e Modelagem de Precificação

Este projeto realiza uma análise exploratória dos dados de acomodações, incluindo o cálculo de novas features (como a proximidade a pontos turísticos) e a criação de um modelo preditivo para a precificação dos imóveis utilizando o XGBRegressor. O projeto inclui a geração de diversos gráficos, a criação de um relatório em PDF e o treinamento do modelo com ajuste de hiperparâmetros.

## Sumário

- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Execução do Projeto](#execução-do-projeto)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Arquivo de Requisitos](#arquivo-de-requisitos)
- [Referências](#referências)

## Pré-requisitos

- **Python 3.7+**  
- **Google Colab** (ou ambiente local com suporte ao Jupyter Notebook)  
- Acesso ao **Google Drive** (caso utilize o Colab) para armazenamento e leitura dos arquivos de dados e saída do relatório/modelo.

## Instalação

1. **Clone o repositório** (ou baixe os arquivos do projeto):

   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd <NOME_DO_DIRETORIO>

    Crie um ambiente virtual (opcional, mas recomendado):

python -m venv venv
source venv/bin/activate   # Linux/MacOS
venv\Scripts\activate      # Windows

Instale os pacotes necessários usando o arquivo de requisitos:

    pip install -r requirements.txt

Execução do Projeto
Utilizando o Google Colab

    Faça o upload do notebook (por exemplo, projeto_precificacao.ipynb) para o seu Google Drive ou abra diretamente no Colab.

    No notebook, monte o Google Drive (o código já contém a chamada para drive.mount):

    from google.colab import drive
    drive.mount('/content/drive', force_remount=True)

    Ajuste os caminhos dos arquivos de entrada e saída conforme a estrutura do seu Google Drive (os caminhos estão definidos nas variáveis file_path, output_pdf, etc.).

    Execute as células do notebook passo a passo para realizar a análise exploratória, gerar os gráficos, criar o relatório em PDF e treinar o modelo preditivo.

Utilizando Ambiente Local

    Abra o notebook em seu ambiente local (Jupyter Notebook, VSCode, etc.).

    Caso não utilize o Google Colab, remova ou ajuste as chamadas referentes ao drive.mount e defina os caminhos dos arquivos conforme sua estrutura local.

    Execute as células do notebook conforme a ordem apresentada para obter os resultados.

Estrutura do Projeto

├── notebooks
│   └── projeto_precificacao.ipynb   # Notebook principal com todo o código
├── data
│   ├── teste_indicium_precificacao.csv   # Arquivo de dados de acomodações
│   └── pontos_turisticos.csv             # Arquivo de dados de pontos turísticos
├── output
│   ├── graficos                         # Pasta para os gráficos gerados
│   ├── Relatorio_vit.pdf                # Relatório em PDF gerado
│   └── modelo_final.pkl                 # Modelo treinado salvo
├── requirements.txt                     # Lista de pacotes e versões necessárias
└── README.md                            # Este arquivo

Arquivo de Requisitos

Segue um exemplo do arquivo requirements.txt com os pacotes utilizados:

# Manipulação de Dados e Cálculos
numpy==1.21.6
pandas==1.3.5

# Visualização de Dados
matplotlib==3.5.1
seaborn==0.11.2
geopandas==0.10.2
contextily==1.2.0
wordcloud==1.8.1

# Processamento de Texto e PDFs
fpdf==1.7.2
tabulate==0.8.9

# Machine Learning e Modelagem
scikit-learn==1.0.2
xgboost==1.6.2

# Outras Dependências
tqdm==4.64.0
joblib==1.1.0

# (Caso utilize o Google Colab, este já possui as bibliotecas instaladas, exceto as especificadas acima)

    Observação: As versões indicadas são sugestivas. Verifique a compatibilidade com seu ambiente e atualize as versões se necessário.

Referências

    Scikit-learn: https://scikit-learn.org/stable/
    XGBoost: https://xgboost.readthedocs.io/en/latest/
    FPDF: https://pyfpdf.readthedocs.io/en/latest/
    Tabulate: https://pypi.org/project/tabulate/
