# Socioeconomic-Clustering-Analysis
## Descrição
Este projeto foi desenvolvido como parte do meu processo de aprendizado em Ciência de Dados, com foco em técnicas de aprendizado de máquina não supervisionado. Utilizando Python e bibliotecas como Scikit-learn, Pandas e Matplotlib, realizei uma análise de clustering com o algoritmo KMeans, buscando segmentar indivíduos com base em variáveis socioeconômicas e demográficas. O objetivo é extrair padrões úteis que possam ser aplicados em políticas públicas e estratégias de mercado.
## Objetivo
O objetivo deste projeto é aplicar técnicas de aprendizado não supervisionado, utilizando o algoritmo KMeans, para identificar grupos homogêneos de indivíduos com base em características socioeconômicas e demográficas. A intenção é revelar padrões relacionados à renda, ocupação, educação, idade, estado civil e localização geográfica, contribuindo para uma melhor compreensão da estrutura social e para subsidiar tomadas de decisão em áreas como políticas públicas e segmentação de mercado.
# Planejamento da Solução
## Produto final
O produto final deste projeto é uma análise detalhada baseada em aprendizado não supervisionado, que segmenta indivíduos em grupos socioeconomicamente semelhantes. Utilizando o algoritmo KMeans, o projeto identifica padrões relevantes entre variáveis como idade, renda, escolaridade, ocupação, estado civil e localização. A segmentação permite entender melhor o perfil dos indivíduos em diferentes contextos sociais, sendo útil para direcionamento de políticas públicas, ações de marketing e estudos demográficos.
# Ferramentas
Python 3.12.9: Linguagem de programação principal, amplamente utilizada em ciência de dados por sua versatilidade e vasta gama de bibliotecas.
Pandas: Para manipulação e análise eficiente dos dados tabulares.
NumPy: Para operações numéricas e suporte a arrays.
Matplotlib & Seaborn: Para visualização gráfica dos dados e dos clusters.
Scikit-learn: Biblioteca fundamental para aplicação de algoritmos de machine learning, incluindo o KMeans e métricas de avaliação como Silhouette Score.
StandardScaler & OrdinalEncoder (Scikit-learn): Utilizados na preparação dos dados, normalizando variáveis numéricas e transformando variáveis categóricas.
# Desenvolvimento
## Estratégia da Solução
Para desenvolver esta análise de clustering socioeconômico, utilizei a linguagem Python em conjunto com bibliotecas especializadas em ciência de dados e machine learning. A estratégia adotada envolveu a limpeza e preparação dos dados, com codificação de variáveis categóricas e padronização de variáveis numéricas. Em seguida, apliquei o algoritmo KMeans para segmentar os indivíduos em grupos com características semelhantes.
A definição do número ideal de clusters foi feita por meio do método do cotovelo, utilizando a biblioteca kneed. O modelo foi avaliado por métricas como Silhouette Score e Davies-Bouldin Score, permitindo medir a separação e compactação dos grupos. Ao final, analisei o perfil de cada cluster para identificar padrões e gerar insights relevantes. Visualizações como gráficos de dispersão e boxplots ajudaram a validar a coerência dos agrupamentos.
## O passo a passo
Passo 1: Definição do objetivo e escopo da análise, focando na segmentação de indivíduos com base em variáveis socioeconômicas e demográficas.

Passo 2: Configuração do ambiente Python e instalação das bibliotecas necessárias, como Pandas, NumPy, Scikit-learn, Matplotlib e Seaborn.

Passo 3: Carregamento e exploração inicial do conjunto de dados, verificando a estrutura, tipos de variáveis e presença de valores ausentes.

Passo 4: Tratamento de dados faltantes por meio de imputação (mediana para variáveis numéricas e moda para categóricas).

Passo 5: Codificação das variáveis categóricas com OrdinalEncoder, preparando os dados para o algoritmo de clustering.

Passo 6: Padronização das variáveis numéricas com StandardScaler para garantir que todas tenham a mesma influência no modelo.

Passo 7: Aplicação do método do cotovelo com kneed para definir o número ideal de clusters para o KMeans.

Passo 8: Treinamento do modelo KMeans com o número ideal de clusters, seguido da avaliação com métricas como Silhouette Score e Davies-Bouldin Score.

Passo 9: Análise dos perfis dos clusters formados, identificando padrões entre idade, renda, escolaridade, ocupação e localização.

Passo 10: Visualização dos resultados com gráficos de dispersão e boxplots, além da documentação completa da solução com insights e sugestões de melhorias.

