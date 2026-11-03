# Repositório de Redes Neurais Artificiais (PPGCC / DCCMAPI / UFMA)

Repositório acadêmico desenvolvido para as atividades práticas da disciplina de **Redes Neurais Artificiais** do **Programa de Pós-Graduação em Ciência da Computação (PPGCC / DCCMAPI / UFMA)** sob orientação do **Prof. Dr. Areolino de Almeida Neto**.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RicDM/trabalhos_redes_neurais/blob/main/MLP/reconhecimento_fonemas_mlp.ipynb)

---

## 🏗️ Estrutura do Repositório

O repositório é organizado para que a base de dados acústicos permaneça centralizada em `dados/dataset/`, permitindo que todas as redes neurais desenvolvidas na disciplina (MLP, RBF, MRNA etc.) acessem diretamente os mesmos dados:

```text
.
├── README.md                 # Documentação e instruções de execução
├── .gitignore                # Configurações de exclusão do Git
│
├── dados/                    # Base de dados acústicos compartilhada
│   └── dataset/              # 423 áudios WAV segmentados das 6 classes de fonemas
│       ├── DI/               # 68 amostras da sílaba DI
│       ├── REI/              # 68 amostras da sílaba REI
│       ├── TA/               # 68 amostras da sílaba TA
│       ├── ES/               # 73 amostras da sílaba ES
│       ├── QUER/             # 73 amostras da sílaba QUER
│       └── DA/               # 73 amostras da sílaba DA
│
└── MLP/                      # Trabalho 1: Multilayer Perceptron (MLP)
    └── reconhecimento_fonemas_mlp.ipynb  # Notebook interativo executado de ponta a ponta
```

---

## 🚀 Execução e Reprodutibilidade

### 1. Execução no Google Colab via GitHub
O notebook [`reconhecimento_fonemas_mlp.ipynb`](MLP/reconhecimento_fonemas_mlp.ipynb) conta com detecção e configuração automática de ambiente:
1. Clique no badge **Open in Colab** no topo deste documento.
2. Ao executar a primeira célula, o Colab detecta o ambiente em nuvem, instala silenciosamente a biblioteca de áudio `soundfile` e clona os dados do repositório (`RicDM/trabalhos_redes_neurais`).
3. Todas as 22 células podem ser executadas sequencialmente sem necessidade de upload manual de arquivos.

### 2. Execução Local
1. Clone o repositório:
   ```bash
   git clone https://github.com/RicDM/trabalhos_redes_neurais.git
   cd trabalhos_redes_neurais
   ```
2. Instale as dependências:
   ```bash
   pip install numpy scipy matplotlib soundfile scikit-learn torch
   ```
3. Abra e execute o notebook:
   ```bash
   cd MLP
   jupyter notebook reconhecimento_fonemas_mlp.ipynb
   ```

---

## 🎯 Próximos Trabalhos
Para os próximos trabalhos da disciplina (como redes RBF ou CNNs), basta criar a respectiva pasta (ex.: `RBF/` ou `CNN/`). Os dados pré-processados já estão prontos e compartilhados em `dados/dataset/`.
