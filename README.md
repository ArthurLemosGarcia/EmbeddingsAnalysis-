Análise de Embeddings e Redução da Dimensionalidade com BERT
Este projeto consiste em um Jupyter Notebook que explora o uso de modelos de linguagem (BERT) para transformar textos em vetores numéricos (embeddings), visualizá-los em espaços de baixa dimensão e realizar agrupamento (clustering) semântico.

📋 Visão Geral
O objetivo principal é demonstrar como máquinas "entendem" o significado de frases. O fluxo de trabalho abrange:

Geração de Embeddings: Conversão de frases em vetores de 768 dimensões usando BERT.

Redução de Dimensionalidade: Compressão desses vetores para 2 dimensões para visualização gráfica.

Clusterização: Agrupamento automático de frases similares.

Classificação: Criação de uma função para categorizar novos textos baseada nos grupos formados.

🛠️ Tecnologias Utilizadas
O projeto foi desenvolvido em Python utilizando as seguintes bibliotecas:

Transformers (Hugging Face): Para carregar o modelo BERT pré-treinado.

PyTorch: Backend para processamento do modelo.

Scikit-Learn: Para PCA, t-SNE e K-Means.

UMAP-learn: Para a técnica de redução UMAP.

Matplotlib: Para plotagem dos gráficos.

NumPy: Para manipulação de arrays e vetores.
