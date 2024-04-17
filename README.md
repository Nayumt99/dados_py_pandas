# Análise de Dados de Vendas

Este é um script Python para realizar uma análise de dados de vendas utilizando Pandas e Matplotlib.

## Passos do Projeto

1. Importação das Bibliotecas

Antes de iniciar a análise, é necessário importar as bibliotecas necessárias. No código fornecido, estamos importando Pandas para manipulação de dados.
````
import pandas as pd
````

2. Carregamento dos Dados

O próximo passo é carregar os dados a partir de um arquivo CSV. Certifique-se de substituir 'tabela.csv' pelo caminho onde o arquivo CSV está armazenado.
````
df = pd.read_csv('tabela.csv')
````

3. Análise Exploratória de Dados (EDA)

Nesta etapa, realizamos uma análise inicial dos dados para entender sua estrutura e características.

. Visualizar as primeiras linhas dos dados:
````
print("Primeiras 5 linhas do DataFrame:")
print(df.head())
````
. Verificar o resumo estatístico:
````
print("\nResumo estatístico do DataFrame:")
print(df.describe())
````
. Verificar se há valores nulos ou faltantes:
````
print("\nValores nulos por coluna:")
print(df.isnull().sum())
````

4.  Análise de Vendas

Realizamos uma análise das vendas, neste caso, ao longo do tempo.
````
vendas_por_data = df.groupby('data_venda')['preco'].sum()
print("\nVendas ao longo do tempo:")
print(df.columns)
````

5. Visualização de Dados

Visualizamos os dados utilizando gráficos.

Exemplo de gráfico de vendas ao longo do tempo:
````
import matplotlib.pyplot as plt

plt.figure(figsize=(10, 6))
vendas_por_data.plot()
plt.title('Vendas ao longo do tempo')
plt.xlabel('Data')
plt.ylabel('Vendas')
plt.grid(True)
plt.show()
````


Exemplo de análise de vendas ao longo do tempo:
