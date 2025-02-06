
# Projeto Desafio Lighthouse – Precificação de Aluguéis

## Trilha de Desenvolvimento

Neste projeto, desenvolvi uma solução completa para o desafio da Lighthouse, que consistiu em:

1. **Análise Exploratória de Dados (EDA):**  
   - Carregamento, limpeza e exploração do dataset.
   - Cálculo de novas features, como a proximidade de pontos turísticos.
   - Geração de diversos gráficos (histograma, dispersão, wordcloud, heatmap, mapa geoespacial) para identificar padrões e levantar hipóteses de negócio.

2. **Modelagem Preditiva:**  
   - Preparação dos dados e engenharia de features.
   - Criação de um pipeline que integra transformações (OneHotEncoder e StandardScaler) e o modelo XGBRegressor.
   - Ajuste de hiperparâmetros usando RandomizedSearchCV.
   - Avaliação do modelo com métricas como RMSE, MAE e R².
   - Exemplo de previsão e salvamento do modelo em formato .pkl.

3. **Geração do Relatório:**  
   - Criação de um relatório PDF com gráficos e tabelas, contendo interpretações e hipóteses levantadas durante o desenvolvimento.
   - Os gráficos são salvos como imagens para uso futuro.

Segue abaixo um exemplo de instruções detalhadas de instalação e execução, escritas de forma simples para quem não tem muita experiência:

---

# Instruções de Instalação e Execução

Estas instruções vão guiá-lo passo a passo para instalar e executar o projeto. Siga cada etapa com atenção.

## 1. Pré-requisitos

### a. Ter o Python Instalado

1. **Verifique se o Python já está instalado:**  
   Abra o **Prompt de Comando** (no Windows) ou o **Terminal** (no Mac ou Linux) e digite:
   ```bash
   python --version
   ```
   Se aparecer uma mensagem como `Python 3.7.9` ou superior, você já tem o Python instalado. Caso contrário, siga os passos abaixo.

2. **Instalar o Python:**  
   - Acesse o site oficial: [python.org](https://www.python.org/downloads/)  
   - Baixe a versão recomendada (certifique-se de escolher Python 3.7 ou superior).  
   - Execute o instalador e **marque a opção "Add Python to PATH"** (ou similar) para facilitar o uso no prompt/terminal.

### b. Ter um Ambiente para Executar o Código

Recomenda-se usar o [Google Colab](https://colab.research.google.com/) se você não tiver um ambiente Python configurado localmente, pois o Colab já vem com muitas bibliotecas instaladas e permite montar o Google Drive facilmente.

## 2. Instalação das Dependências

As dependências são bibliotecas que o projeto usa para funcionar. Você precisará instalá-las.

### Passo a Passo:

1. **Abra o Prompt de Comando ou Terminal:**  
   - No Windows, pressione `Win + R`, digite `cmd` e pressione Enter.  
   - No Mac ou Linux, abra o Terminal.

2. **Instale as bibliotecas necessárias:**  
   Copie e cole o seguinte comando e pressione Enter:
   ```bash
   pip install pandas numpy matplotlib seaborn geopandas contextily wordcloud scikit-learn xgboost fpdf tabulate joblib tqdm
   ```
   Isso instalará todas as bibliotecas necessárias para o projeto.

*Caso esteja usando o Google Colab, você pode criar uma célula no notebook e executar esse comando com `!` no início, assim:*

```python
!pip install pandas numpy matplotlib seaborn geopandas contextily wordcloud scikit-learn xgboost fpdf tabulate joblib tqdm
```

## 3. Obter o Código do Projeto

### Opção A: Clonar o Repositório (para quem tem Git instalado)

1. **Abra o Prompt de Comando ou Terminal.**  
2. **Digite o seguinte comando:**
   ```bash
   git clone https://github.com/vitfreire/LH_CD_VitoriaFreire.git
   ```
   Isso criará uma pasta com os arquivos do projeto no seu computador.

3. **Entre na pasta do projeto:**
   ```bash
   cd LH_CD_VitoriaFreire
   ```

### Opção B: Baixar o ZIP do Repositório (para quem não sabe usar Git)

1. Acesse a página do repositório no GitHub.
2. Clique no botão **Code** e selecione **Download ZIP**.
3. Extraia os arquivos do ZIP para uma pasta no seu computador.

## 4. Montando o Google Drive (se estiver usando Google Colab)

Se você estiver usando o Google Colab para executar o projeto, será necessário montar o Google Drive para acessar os arquivos. Siga estes passos:

1. Abra o seu notebook no Google Colab.
2. Na primeira célula, insira o seguinte código e execute:
   ```python
   from google.colab import drive
   drive.mount('/content/drive', force_remount=True)
   ```
3. Será exibido um link; clique nele, faça login com sua conta Google, copie o código de autorização e cole na caixa de entrada do Colab.

## 5. Configurando os Caminhos dos Arquivos

No código, alguns caminhos são definidos para indicar onde estão os arquivos. Verifique os seguintes pontos:

- **Dataset Principal:**  
  O arquivo `teste_indicium_precificacao.csv` deve estar localizado em:  
  `/content/drive/MyDrive/LH_CD/teste_indicium_precificacao.csv`

- **Arquivo de Pontos Turísticos:**  
  O arquivo `pontos_turisticos.csv` deve estar em:  
  `/content/drive/MyDrive/LH_CD/pontos_turisticos.csv`

- **Diretório para Salvar Gráficos:**  
  O código cria uma pasta para os gráficos em:  
  `/content/drive/MyDrive/LH_CD/graficos`

- **Relatório PDF e Modelo:**  
  O relatório será salvo em:  
  `/content/drive/MyDrive/LH_CD/Relatorio_vit.pdf`  
  e o modelo no formato `.pkl` em:  
  `/content/drive/MyDrive/LH_CD/modelo_final.pkl`

Caso os arquivos estejam em outro local, altere as variáveis correspondentes no código.

## 6. Execução do Projeto

### Para usuários do Google Colab:

1. **Abra o Notebook:**  
   Carregue o arquivo do notebook (ex.: `Projeto_Lighthouse.ipynb`) no Google Colab.

2. **Execute as Células:**  
   Execute as células na ordem apresentada. O fluxo de execução será:
   - Carregamento e limpeza dos dados.
   - Cálculo de novas features e geração de gráficos.
   - Treinamento do modelo preditivo e avaliação.
   - Geração do relatório PDF com tabelas, gráficos e interpretações.
   - Exemplo de previsão e salvamento do modelo.

### Para usuários locais:

1. **Abra o seu editor de código (ex.: VSCode, PyCharm) ou use o Jupyter Notebook.**
2. **Abra o arquivo do notebook** e execute as células na ordem indicada.

## 7. Verificação dos Resultados

Após a execução, confira se os seguintes itens foram gerados:

- **Relatório PDF:**  
  Verifique se o arquivo `/content/drive/MyDrive/LH_CD/Relatorio_vit.pdf` foi criado com sucesso.

- **Gráficos (imagens):**  
  A pasta `/content/drive/MyDrive/LH_CD/graficos` deve conter os gráficos gerados.

- **Modelo Salvo (.pkl):**  
  O arquivo `/content/drive/MyDrive/LH_CD/modelo_final.pkl` deve estar disponível.

## Conclusão

Esta etapa finaliza o processo. Se tudo foi executado corretamente, você terá:
- Um conjunto de gráficos e tabelas que apoiam a análise exploratória.
- Um modelo preditivo otimizado para a precificação de aluguéis.
- Um relatório PDF detalhado contendo todas as análises e hipóteses levantadas.

Caso haja qualquer dúvida ou problema durante a instalação ou execução, consulte os passos novamente ou entre em contato.

---

