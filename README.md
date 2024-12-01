```markdown
# Análise de Agrupamento com K-Means no Dataset UCI HAR

## Objetivo do Projeto
Este projeto tem como objetivo aplicar o algoritmo K-Means para realizar agrupamento de dados do *UCI Human Activity Recognition Dataset*. O conjunto de dados contém medições de sensores de smartphones, com 561 features extraídas de sinais de acelerômetro e giroscópio, associadas a 6 atividades humanas distintas.

## Instruções para Execução
1. **Clone o Repositório**:
   ```bash
   git clone <https://github.com/meirelesgc/restic-kmeans.git>
   cd <restic-kmeans>
   ```

2. **Instale as Dependências**:
   Utilize um ambiente virtual Python e instale os pacotes necessários:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # No Windows, use .venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Execute o Código**:
   Para rodar o código, basta executar o notebook, abra o arquivo `kmeans.ipynb` em um ambiente de notebook, como Jupyter ou VS Code, e execute as células sequencialmente.

## Principais Conclusões
- **Número de Clusters**:
  O método do cotovelo sugeriu que o número ideal de clusters (k) seria 3 ou 4, mas utilizamos k=6 para refletir as 6 atividades do dataset.
  
- **Resultados de Agrupamento**:
  - O *Silhouette Score* foi de **0.1086**, indicando baixa coesão interna e separação entre os clusters.
  - O índice Rand ajustado foi de **0.4197**, demonstrando uma correspondência limitada entre os agrupamentos gerados e os rótulos reais das atividades.

- **Visualização**:
  A redução de dimensionalidade com PCA mostrou sobreposição significativa entre os clusters, destacando as limitações do K-Means para lidar com dados de classes sobrepostas.

- **Considerações Finais**:
  O algoritmo K-Means não conseguiu identificar os padrões de forma satisfatória. Recomenda-se a aplicação de métodos mais avançados, como DBSCAN ou redes neurais, para melhorar os resultados.

## Contribuições
Sinta-se à vontade para abrir *issues* ou enviar *pull requests* para melhorias no projeto.
```