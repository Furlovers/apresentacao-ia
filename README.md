# Classificação de Raças de Cachorros

Notebook da apresentação de Inteligência Artificial: transfer learning com TensorFlow Hub (MobileNetV2) para identificar a raça de um cachorro a partir de uma foto.

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Furlovers/apresentacao-ia/blob/main/DogBreeds_Apresentacao.ipynb)

## Como rodar

**No Google Colab (mais simples):** abra pelo botão acima, escolha um ambiente com GPU (*Ambiente de execução → Alterar o tipo de ambiente → T4*) e use *Ambiente de execução → Executar tudo*. A primeira célula instala o que faltar e baixa os dados. A última célula abre o botão de upload para você enviar a foto de um cachorro.

**No computador (testado com Python 3.12; o TensorFlow ainda não tem versão estável para o 3.14):**

```bash
git clone https://github.com/Furlovers/apresentacao-ia.git
cd apresentacao-ia
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute --inplace DogBreeds_Apresentacao.ipynb
```

Ou abra o notebook no VS Code ou no Jupyter e rode todas as células. Fora do Colab, a inferência usa uma foto da validação (ou a foto cujo caminho você puser em `CAMINHO_IMAGEM`).

## Dados

Imagens de treino e rótulos da competição [Dog Breed Identification](https://www.kaggle.com/competitions/dog-breed-identification/data) do Kaggle (10.222 fotos, 120 raças). O notebook baixa os dois arquivos da release [`v1.0-dados`](https://github.com/Furlovers/apresentacao-ia/releases/tag/v1.0-dados) deste repositório (`train.zip`, 345 MB, e `labels.csv`) para a pasta `dados/` (no Colab, `/content/dados`), só na primeira vez. Não precisa de conta no Kaggle.
