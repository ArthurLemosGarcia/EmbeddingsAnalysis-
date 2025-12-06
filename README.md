# 🧠 Análise de Embeddings e Redução de Dimensionalidade com BERT

## 🚀 Sobre o Projeto

O objetivo deste notebook é desmistificar como as máquinas "entendem" o contexto das palavras. Ao invés de apenas contar palavras, utilizamos _Deep Learning_ para capturar nuances.

O projeto passa por quatro etapas principais:
1.  **Extração de Features:** Uso do BERT para gerar vetores de 768 dimensões.
2.  **Visualização:** Compressão desses vetores para 2D usando PCA, t-SNE e UMAP.
3.  **Clusterização:** Uso do K-Means para encontrar tópicos automaticamente.
4.  **Classificação:** Um sistema simples para categorizar novas frases com base nos clusters aprendidos.

---

## 🛠 Tecnologias Utilizadas

| Biblioteca | Função Principal |
| :--- | :--- |
| **Transformers** | Acesso ao modelo pré-treinado `bert-base-uncased`. |
| **PyTorch** | Backend para processamento dos tensores do modelo. |
| **Scikit-Learn** | Algoritmos de PCA, t-SNE e K-Means. |
| **UMAP-Learn** | Técnica avançada de redução de dimensionalidade (preserva estrutura global). |
| **Matplotlib** | Plotagem dos gráficos de dispersão. |

---

## 🔬 Pipeline de Análise

### 1. Geração de Embeddings
Cada frase da base de dados é tokenizada e passada pelo modelo BERT. Utilizamos a média da última camada oculta (_last hidden state_) para criar uma representação vetorial densa da frase.

### 2. Redução de Dimensionalidade
Para visualizar os dados, comparamos três técnicas:
* **PCA:** Rápido, focado na variância global.
* **t-SNE:** Excelente para agrupar vizinhos locais, mas computacionalmente pesado.
* **UMAP:** O melhor dos dois mundos; rápido e preserva tanto a estrutura global quanto a local.

### 3. Agrupamento (Clustering)
Utilizamos o algoritmo **K-Means** com `k=4`. O modelo identificou automaticamente os seguintes temas nos textos:
* 🍳 **Culinária**
* 🌍 **Geografia**
* 📈 **Finanças**
* 🤖 **Tecnologia/IA**
