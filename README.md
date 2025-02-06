Desafio Lighthouse – Precificação de Aluguéis
Introdução

Este projeto foi desenvolvido como parte do desafio para Cientista de Dados da Lighthouse. O objetivo do desafio é testar a capacidade de resolver problemas de negócios, realizar uma análise exploratória de dados (EDA) e aplicar modelos preditivos para determinar a precificação de aluguéis.

Durante o desenvolvimento deste projeto, aprendi e apliquei conceitos de engenharia de dados, visualização, modelagem preditiva e validação de modelos. Além disso, pude aprimorar minhas habilidades em transformar dados brutos em insights acionáveis e em documentar de forma clara o processo adotado para resolver o desafio.
Motivação e Habilidades Desenvolvidas

    Análise Exploratória de Dados (EDA):
    Realizei uma exploração detalhada do dataset, identifiquei relações entre variáveis e criei hipóteses de negócio. Essa etapa me permitiu entender melhor o comportamento dos preços dos imóveis e a importância de fatores como localização, avaliações e características dos anúncios.

    Modelagem Preditiva:
    Desenvolvi um pipeline de machine learning utilizando transformações (OneHotEncoder e StandardScaler) e o modelo XGBRegressor. Ajustei os hiperparâmetros com RandomizedSearchCV, otimizando o modelo para prever os preços de forma eficaz.

    Documentação e Comunicação de Resultados:
    A criação de um relatório em PDF com gráficos, tabelas e interpretações detalhadas foi fundamental para organizar e comunicar os insights obtidos durante o projeto.

    Integração de Ferramentas:
    Utilizei diversas bibliotecas do Python para análise de dados, visualização e modelagem, o que reforçou meu conhecimento em ferramentas amplamente utilizadas na área de Data Science.

Instalação e Execução
Pré-requisitos

    Python 3.7+
    Ambiente de execução: Google Colab (ou outro ambiente que permita a montagem do Google Drive)

Dependências

O projeto utiliza as seguintes bibliotecas:

    pandas
    numpy
    matplotlib
    seaborn
    geopandas
    contextily
    wordcloud
    scikit-learn
    xgboost
    fpdf
    tabulate
    joblib
    tqdm

Para instalar as dependências, execute:

pip install pandas numpy matplotlib seaborn geopandas contextily wordcloud scikit-learn xgboost fpdf tabulate joblib tqdm

Passos para Instalação e Execução

    Clone o Repositório

    Clone o repositório para a sua máquina:

git clone https://github.com/vitfreire/LH_CD_VitoriaFreire.git

cd LH_CD_VitoriaFreire

Monte o Google Drive (para usuários do Google Colab)

No início do notebook, insira e execute:

    from google.colab import drive
    drive.mount('/content/drive', force_remount=True)

    Configure os Caminhos dos Arquivos

    Certifique-se de que o arquivo teste_indicium_precificacao.csv e o arquivo pontos_turisticos.csv estejam no caminho correto (por exemplo, /content/drive/MyDrive/LH_CD/).

    Execute o Notebook

    Abra o notebook no Google Colab e execute todas as células na ordem. O código realizará:
        A análise exploratória dos dados, geração e salvamento de gráficos e mapas.
        A criação e treinamento do modelo preditivo.
        A geração de um relatório PDF contendo tabelas, gráficos e explicações.

    Salvamento do Modelo

    Ao final, o modelo otimizado será salvo no formato .pkl (por exemplo, em /content/drive/MyDrive/LH_CD/modelo_final.pkl).

Estrutura do Projeto

    Análise Exploratória (EDA):
    Carregamento e limpeza dos dados, cálculo de novas features (incluindo pontos turísticos) e geração de visualizações que apoiam as hipóteses de negócio.

    Modelagem Preditiva:
    Preparação dos dados, criação do pipeline com transformações e XGBRegressor, ajuste de hiperparâmetros e avaliação do modelo.

    Relatório PDF:
    Um relatório completo com tabelas, gráficos e interpretações que documenta cada etapa do projeto.

    Código e Documentação:
    Todo o código segue boas práticas de programação e está devidamente comentado para facilitar a compreensão.

Conclusão

Este projeto não só demonstra minha capacidade de aplicar técnicas avançadas de análise de dados e modelagem preditiva, como também evidencia a importância de documentar e justificar cada passo na resolução de um problema de negócios. Ao longo do desafio, foram levantadas hipóteses como:

    Distribuição dos Preços: Preços elevados podem indicar nichos premium.
    Reviews e Demanda: Um alto número de reviews pode refletir alta demanda, influenciando a precificação.
    Mínimo de Noites e Público-Alvo: Restrições de estadia podem direcionar os imóveis a segmentos específicos do mercado.
    Disponibilidade: Baixa disponibilidade pode sinalizar alta demanda e preços mais elevados.
    Proximidade de Pontos Turísticos: Imóveis próximos a atrações turísticas tendem a ser mais valorizados.
    Padrão nos Nomes: Termos que sugerem luxo e exclusividade são mais comuns em imóveis com preços elevados.
    Correlação entre Variáveis: Variáveis como disponibilidade e reviews são determinantes na formação dos preços.
    Localização: A região central de Nova York é um fator importante para a precificação dos imóveis.
