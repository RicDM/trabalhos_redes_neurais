# Repositório de Redes Neurais Artificiais (PPGCC / DCCMAPI / UFMA)

Repositório acadêmico desenvolvido por **Ricardo Diniz Mendes** para as atividades práticas da disciplina de **Redes Neurais Artificiais** do **Programa de Pós-Graduação em Ciência da Computação (PPGCC / DCCMAPI / UFMA)** sob orientação do **Prof. Dr. Areolino de Almeida Neto**.

---

## 📚 Trabalhos da Disciplina (Google Colab)

| Trabalho | Arquitetura | Base de Dados | Notebook Interativo |
| :--- | :--- | :--- | :--- |
| **Trabalho 1** | Perceptron Multicamadas (**MLP**) | 1 falante (`dados/dataset/`, 423 sílabas) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RicDM/trabalhos_redes_neurais/blob/main/MLP/reconhecimento_fonemas_mlp.ipynb) |
| **Trabalho 2** | Funções de Base Radial (**RBF**) | 1 falante (`dados/dataset/`, 423 sílabas) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RicDM/trabalhos_redes_neurais/blob/main/RBF/reconhecimento_fonemas_rbf.ipynb) |
| **Trabalho 3** | Múltiplas RNAs Sem Coordenador (**MRNA**) | 3 falantes (`dados/dataset_3pessoas/`, 879 sílabas) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RicDM/trabalhos_redes_neurais/blob/main/MRNA/reconhecimento_fonemas_mrna.ipynb) |

---

## 🏗️ Estrutura do Repositório

```text
.
├── README.md                                 # Documentação e links para o Google Colab
├── .gitignore                                # Configurações de exclusão do Git
│
├── dados/                                    # Bases de dados acústicos (16 kHz, 16-bit PCM mono)
│   ├── dataset/                              # 423 sílabas (1 falante — Trabalhos 1 e 2)
│   │   ├── DI/, REI/, TA/                    # 68 amostras por sílaba de DIREITA
│   │   └── ES/, QUER/, DA/                   # 73 amostras por sílaba de ESQUERDA
│   └── dataset_3pessoas/                     # 879 sílabas / 293 palavras (3 falantes — Trabalho 3)
│       ├── DI/, REI/, TA/                    # 145 amostras por sílaba (p1 + p2 + p3)
│       └── ES/, QUER/, DA/                   # 148 amostras por sílaba (p1 + p2 + p3)
│
├── MLP/
│   └── reconhecimento_fonemas_mlp.ipynb      # Trabalho 1: MLP implementada em NumPy puro
├── RBF/
│   └── reconhecimento_fonemas_rbf.ipynb      # Trabalho 2: RBF (WTA + KNN + Ridge) em NumPy puro
└── MRNA/
    └── reconhecimento_fonemas_mrna.ipynb     # Trabalho 3: MRNA Sequencial (MLP + RBF + MLP) em NumPy puro
```

---

## 🎙️ Base Multi-Falante (Trabalho 3 — MRNA)
O corpus `dados/dataset_3pessoas/` reúne vocalizações das palavras **DIREITA** e **ESQUERDA** de **3 pessoas diferentes**:
- **Pessoa 1 (`p1`):** Locutor original (68 `DIREITA`, 73 `ESQUERDA` — 423 sílabas);
- **Pessoa 2 (`p2`):** Voz masculina `s023` do *FLA-Dataset* (52 `DIREITA`, 46 `ESQUERDA` — 294 sílabas);
- **Pessoa 3 (`p3`):** Voz feminina `s006` do *FLA-Dataset* (25 `DIREITA`, 29 `ESQUERDA` — 162 sílabas).

---

## 🚀 Execução e Reprodutibilidade

### 1. Execução no Google Colab via GitHub
Todos os notebooks contam com detecção e configuração automática de ambiente:
1. Clique no badge **Open In Colab** do trabalho desejado na tabela acima.
2. Ao executar a primeira célula, o Colab detecta o ambiente em nuvem, instala a biblioteca `soundfile` caso necessário e clona automaticamente os dados deste repositório (`RicDM/trabalhos_redes_neurais`).
3. Execute as células sequencialmente sem necessidade de upload manual de arquivos.

### 2. Execução Local
1. Clone o repositório:
   ```bash
   git clone https://github.com/RicDM/trabalhos_redes_neurais.git
   cd trabalhos_redes_neurais
   ```
2. Instale as dependências:
   ```bash
   pip install numpy scipy matplotlib soundfile scikit-learn
   ```
3. Abra e execute o notebook desejado (por exemplo, o Trabalho 3):
   ```bash
   jupyter notebook MRNA/reconhecimento_fonemas_mrna.ipynb
   ```
