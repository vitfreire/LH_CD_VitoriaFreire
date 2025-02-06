
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

## Instalação e Execução do Código

### Pré-requisitos

- **Python 3.7 ou superior**
- **Google Colab** (ou outro ambiente que permita a montagem do Google Drive)

### Passo a Passo

1. **Clone o Repositório**  
   Se o código estiver hospedado no GitHub, execute:
   ```bash
   git clone https://github.com/vitfreire/LH_CD_VitoriaFreire.git
   cd LH_CD_VitoriaFreire
   ```

2. **Instale as Dependências**  
   Execute o seguinte comando para instalar as bibliotecas necessárias:
   ```bash
   pip install pandas numpy matplotlib seaborn geopandas contextily wordcloud scikit-learn xgboost fpdf tabulate joblib tqdm
   ```

3. **Monte o Google Drive (para Google Colab)**  
   No início do notebook, execute:
   ```python
   from google.colab import drive
   drive.mount('/content/drive', force_remount=True)
   ```

4. **Configure os Caminhos dos Arquivos**  
   Verifique se os arquivos estão no local correto:  
   - Dataset: `/content/drive/MyDrive/LH_CD/teste_indicium_precificacao.csv`
   - Pontos turísticos: `/content/drive/MyDrive/LH_CD/pontos_turisticos.csv`  
   - Diretório para gráficos: `/content/drive/MyDrive/LH_CD/graficos`

5. **Execute o Notebook**  
   Abra e execute todas as células do notebook no Google Colab. O código fará:
   - A análise exploratória dos dados e salvará os gráficos.
   - O treinamento do modelo preditivo e sua avaliação.
   - A geração do relatório PDF com todas as análises.

6. **Verifique as Entregas**  
   Após a execução, confirme se foram gerados:  
   - O relatório PDF (ex.: `/content/drive/MyDrive/LH_CD/Relatorio_vit.pdf`)
   - Os gráficos salvos na pasta especificada.
   - O modelo salvo em formato .pkl (ex.: `/content/drive/MyDrive/LH_CD/modelo_final.pkl`)

---

Este README explica de forma concisa a trilha do desenvolvimento e fornece um passo a passo detalhado para instalar e executar o código.
