Passo 1: Baixando os dados do Kaggle
O primeiro bloco do script solicita que você insira o link/identificador do dataset do Kaggle (ex: usuario/nome-do-dataset).

O código irá:

Baixar os arquivos automaticamente para uma pasta temporária.

Localizar o arquivo .csv dentro dessa pasta.

Perguntar com qual nome você deseja salvar o arquivo final na sua máquina.

Passo 2: Análise Exploratória e Visualização
Com o arquivo salvo, o script carrega os dados (configurado por padrão para ler o arquivo da Netflix) e gera duas visualizações principais:

Distribuição de Notas: Um gráfico de barras (countplot) mostrando a frequência de cada nota.

Evolução Temporal: Um gráfico de área empilhada que mostra como a quantidade de cada nota variou ao longo dos meses/anos analisados.

📊 Visualizações Geradas
O script manipula colunas de datas para extrair o período (Ano-Mês) e plota os seguintes insights:

🔹 Distribuição de Notas
Um gráfico robusto utilizando a paleta viridis para entender a volumetria das avaliações por score.

🔹 Distribuição de Notas ao Longo do Tempo
Utiliza o método .groupby() e .unstack() para transformar os dados e plotar um gráfico de área, ideal para identificar tendências de comportamento dos usuários ao longo dos meses.

📂 Estrutura do Código
kagglehub.dataset_download(): Conecta à API do Kaggle.

os.listdir() e os.path.join(): Gerenciam os caminhos dos arquivos de forma dinâmica.

pd.to_datetime() e .dt.to_period('M'): Tratam e convertem os campos de texto para o formato de data correto (Ano-Mês).
