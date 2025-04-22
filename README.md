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

# Análise Exploratória dos Dados (EDA)

## 📊Distribuições de Idade e Renda
Para entender melhor as características dos dados antes de aplicar o modelo de clustering, realizei uma análise exploratória com foco em variáveis-chave como idade e renda.

Abaixo, apresento dois histogramas com curvas de densidade que mostram a distribuição dessas variáveis:

No primeiro gráfico (Age Distribution), observamos uma distribuição assimétrica à direita. A maioria dos dados está concentrada entre 20 e 40 anos, com um pico entre 25 e 30 anos.

No segundo gráfico (Income Distribution), também temos uma assimetria à direita. A maior parte dos indivíduos possui uma renda anual entre 50 mil e 150 mil dólares.

![distribuição de idade e renda](
img/distribuicao_idade_renda.png)

## 🔥Mapa de Correlação
A seguir, apresento uma matriz de correlação entre as variáveis numéricas do dataset. Essa visualização ajuda a entender melhor como as variáveis estão relacionadas entre si e a identificar possíveis redundâncias ou padrões interessantes:

Forte relação entre renda e ocupação: Clientes em categorias ocupacionais mais altas geralmente relatam rendas mais elevadas.

Forte relação entre idade e educação: Indivíduos mais velhos tendem a ter níveis de escolaridade mais altos.

![Heatmap de Correlação](imgs/heatmap_correlacao.png)

## 📈Relação entre Idade e Renda

Visualizando a relação entre idade e renda por meio de um gráfico de dispersão com linha de regressão linear.

A linha de tendência mostra que há uma leve tendência de aumento na renda conforme a idade avança, apoiando a correlação observada anteriormente no heatmap.

![Relação entre_idade_renda](imgs/relacao_idade_renda.png)

## Conclusão
A análise inicial revela relações importantes entre variáveis demográficas e econômicas. A ocupação e a educação se destacam como fatores fortemente associados à renda.

#  Treinamento do Modelo 

## Escolha do Algoritmo KMeans

Para realizar a segmentação dos 2000 indivíduos do dataset socioeconômico, que contém variáveis como idade, renda, educação, ocupação, estado civil e tamanho do assentamento, optei pelo algoritmo KMeans como método principal de clustering não supervisionado. A escolha do KMeans foi motivada por uma combinação de fatores técnicos, práticos e contextuais, que são detalhados a seguir:

Simplicidade e Eficiência Computacional
O KMeans é um algoritmo de clustering baseado em partição, conhecido por sua simplicidade e eficiência em datasets de tamanho moderado, como o utilizado neste projeto (2000 registros). Ele agrupa os dados minimizando a variância interna dos clusters, o que o torna rápido e escalável, especialmente quando implementado com bibliotecas otimizadas como o scikit-learn. Essa eficiência foi crucial para realizar múltiplas iterações durante a definição do número ideal de clusters.

Suporte ao Método do Cotovelo
A definição do número ideal de clusters (k=6) foi feita utilizando o método do cotovelo, com auxílio da biblioteca kneed. O KMeans é particularmente compatível com essa técnica, que analisa a soma dos quadrados intra-cluster (WCSS) para identificar o ponto de inflexão onde adicionar mais clusters não melhora significativamente a qualidade da segmentação. A biblioteca kneed automatizou esse processo, confirmando k=5 como o número ideal, o que validou a aplicação do KMeans.

Avaliação com Métricas Robustas
O desempenho do KMeans foi avaliado com o Silhouette Score (média de 0,35) e o Davies-Bouldin Score (média de 1,2), que medem, respectivamente, a separação e a compactação dos clusters. Essas métricas são amplamente suportadas pelo scikit-learn para o KMeans, permitindo uma avaliação quantitativa da qualidade dos clusters formados. Apesar de os valores indicarem alguma sobreposição entre clusters, o KMeans forneceu uma segmentação inicial útil para análise exploratória.

Conclusão da Escolha
O KMeans foi selecionado por sua simplicidade, eficiência e compatibilidade com o dataset e as ferramentas utilizadas (scikit-learn, kneed). Embora a sobreposição entre alguns clusters sugira que algoritmos como DBSCAN ou o tratamento de outliers possam melhorar os resultados, o KMeans forneceu uma base sólida para a segmentação inicial, alinhada com os objetivos do projeto. A experiência reforçou a importância de combinar o KMeans com uma preparação robusta dos dados e métricas de avaliação para garantir resultados interpretáveis e úteis.

#  🔍 Método do Cotovelo com Silhouette Score

O gráfico do método do cotovelo mostra o Silhouette Score para diferentes números de clusters. O pico em 6 clusters indica a melhor separação entre os grupos, servindo como complemento ao dendrograma.

![Método do Cotovelo](imgs/cotovelo.png)

#  🔍 Quantidade de Elementos por Cluster

Essa visualização ajuda a entender a distribuição de elementos em cada cluster. Clusters 0 e 2 concentram a maior parte dos dados.

![Elementos_por_Cluster](imgs/elementos_por_cluster.png)

# Perfis dos Clusters

## Cluster 0: "Profissionais Solteiros de Renda Média-Alta"
○ Tamanho: 579 indivíduos. 
○ Idade: Média de 36,9 anos, mediana de 36, desvio padrão de 8,59. 
○ Renda: Média de 139.478, mediana de 132.243, desvio padrão de 32.788. 
○ Sexo: 100% do mesmo gênero (valor 0, possivelmente masculino). 
○ Estado Civil: 100% solteiros. 
○ Educação: 66,9% com ensino médio, 33,1% com nível desconhecido/outro.
○ Ocupação: 75% empregados qualificados/oficiais, 24,2% 
gerentes/autônomos/funcionários altamente qualificados. 
○ Tamanho do Assentamento: Média de 1,33 (cidades médias ou grandes). 
○ Este grupo é formado por profissionais estabelecidos, solteiros, com boa 
renda e vivendo em áreas urbanas.

## Cluster 1: "Jovens Mistos de Renda Média em Áreas Rurais" 
○ Tamanho: 254 indivíduos. 
○ Idade: Média de 29,8 anos, mediana de 29, desvio padrão de 6,20. 
○ Renda: Média de 113.688, mediana de 112.227, desvio padrão de 13.071. 
○ Sexo: Média de 0,53 (mistura de gêneros, ligeiramente equilibrada). 
○ Estado Civil: 29,8% solteiros, 70,2% não solteiros (casados, divorciados, 
viúvos). 
○ Educação: 92,6% com ensino médio, 7,2% com nível desconhecido/outro, 
0,2% com universidade. 
○ Ocupação: 98,7% empregados qualificados/oficiais, 1,3% 
desempregados/não qualificados. 
○ Tamanho do Assentamento: Média de 0,28 (áreas rurais). 
○ Este grupo representa jovens trabalhadores qualificados, muitos casados ou 
em relacionamentos, vivendo em áreas rurais com renda moderada.

## Cluster 2: "Desempregados Solteiros de Renda Baixa em Áreas Rurais" 
○ Tamanho: 534 indivíduos. 
○ Idade: Média de 35,8 anos, mediana de 35, desvio padrão de 9,49. 
○ Renda: Média de 89.885, mediana de 84.779, desvio padrão de 23.377. 
○ Sexo: 100% do mesmo gênero (valor 0, possivelmente masculino). 
○ Estado Civil: 85,7% solteiros, 14,3% não solteiros. 
○ Educação: 74,8% com ensino médio, 25% com nível desconhecido/outro, 
0,2% com universidade. 
○ Ocupação: 100% desempregados/não qualificados. 
○ Tamanho do Assentamento: Média de 0,12 (majoritariamente áreas rurais). 
○ Este grupo é formado por indivíduos desempregados ou não qualificados, 
com baixa renda, vivendo em áreas rurais e majoritariamente solteiros. 

## Cluster 3: "Desempregadas Jovens de Renda Baixa em Áreas Rurais" 
○ Tamanho: 272 indivíduos. 
○ Idade: Média de 32,9 anos, mediana de 30, desvio padrão de 5,12. 
○ Renda: Média de 87.327, mediana de 86.319, desvio padrão de 20.671. 
○ Sexo: Média de 0,96 (quase todos do gênero oposto, possivelmente 
feminino). 
○ Estado Civil: 69,1% solteiros, 30,9% não solteiros. 
○ Educação: 71,7% com ensino médio, 28,3% com nível desconhecido/outro. 
○ Ocupação: 100% desempregados/não qualificados. 
○ Tamanho do Assentamento: Média de 0 (todos em áreas rurais). 
○ Este grupo é similar ao Cluster 2, mas com predominância de mulheres 
jovens, também desempregadas e com baixa renda. 

## Cluster 4: "Jovens Casados de Renda Média-Alta em Áreas Urbanas" 
○ Tamanho: 361 indivíduos. 
○ Idade: Média de 28,1 anos, mediana de 28, desvio padrão de 5,12. 
○ Renda: Média de 127.664, mediana de 118.428, desvio padrão de 30.789. 
○ Sexo: Média de 0,57 (mistura de gêneros). 
○ Estado Civil: 100% não solteiros. 
○ Educação: 99,5% com ensino médio, 0,5% com universidade. 
○ Ocupação: 82% empregados qualificados/oficiais, 15,8% 
gerentes/autônomos/funcionários altamente qualificados, 2,2% 
desempregados/não qualificados. 
○ Tamanho do Assentamento: Média de 1,21 (cidades médias ou grandes). 
○ Este grupo é formado por jovens casados, com boa renda, vivendo em áreas 
urbanas e trabalhando em posições qualificadas. 

## Cluster 5: "Profissionais Mais Velhos de Alta Renda e Educação Superior" 
○ Tamanho: Possivelmente vazio (verificação necessária). 
○ Idade: Média de 55,9 anos, mediana de 57, desvio padrão de 10,45. 
○ Renda: Média de 159.967, mediana de 149.410, desvio padrão de 44.328. 
○ Sexo: Média de 0,48 (gêneros equilibrados). 
○ Estado Civil: 31,3% solteiros, 68,7% não solteiros. 
○ Educação: 14,5% com ensino médio, 85,5% com nível universitário. 
○ Ocupação: 57,8% empregados qualificados/oficiais, 29,3% 
gerentes/autônomos/funcionários altamente qualificados, 12,9% 
desempregados/não qualificados. 
○ Tamanho do Assentamento: Média de 1,15 (cidades médias ou grandes). 
○ Este grupo representa profissionais mais velhos, com alta educação e renda, 
vivendo em áreas urbanas e ocupando posições variadas, incluindo cargos 
de liderança.

# Conclusão 
A análise de clustering identificou cinco grupos distintos com base em variáveis 
socioeconômicas, revelando padrões claros relacionados à renda, idade, estado civil, 
educação, ocupação e localização geográfica. O KMeans foi eficaz para uma segmentação 
inicial, destacando grupos como profissionais de alta renda em áreas urbanas (Clusters 0, 4 
e 5) e desempregados de baixa renda em áreas rurais (Clusters 2 e 3). No entanto, a 
sobreposição entre clusters e a possibilidade de o Cluster 5 estar vazio (necessitando 
verificação) sugerem que algoritmos baseados em densidade (como DBSCAN) ou 
tratamento de outliers podem melhorar os resultados. Esta análise pode ser aplicada em 
contextos de políticas públicas (ex.: suporte a grupos de baixa renda em áreas rurais) e 
estratégias de mercado (ex.: segmentação de consumidores urbanos de alta renda). A 
experiência reforça a importância da preparação dos dados, da análise exploratória e da 
avaliação de diferentes abordagens de clustering como etapas essenciais de um pipeline de 
aprendizado de máquina não supervisionado.

