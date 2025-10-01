# Mini-curso: Análise Preditiva de Dados com IA (CONCCEPAR)

Material do mini-curso apresentado no CONCCEPAR. Foco prático em regressão e modelos de árvore, com exemplos simples e diretos em Python.

## Conteúdo
- **Regressão Linear (1 variável)**: cálculo manual da reta, métricas (MSE, RMSE, R²) e gráfico.
- **Busca de hiperparâmetros para a reta**:
  - Grid Search (varre intervalo para `a` e `b`).
  - Random Search (amostras aleatórias de `a` e `b`).
  - Otimização Bayesiana (com `skopt`/`gp_minimize`).
- **Gradiente Descendente**: estima `a` (inclinação) e `b` (intercepto) por iteração.
- **Regressão Linear Múltipla**: preparo de dados, `train_test_split`, `LinearRegression` e avaliação.
- **Árvore de Decisão (regressão)**: treino, métricas, importância de variáveis e visualização da árvore.
- **Random Forest (regressão)**: treino, métricas e importância de variáveis.
- **Gradient Boosting (regressão)**: treino, métricas e importância de variáveis.

## Requisitos
Python 3.10+ e as bibliotecas:
```
numpy
pandas
matplotlib
seaborn
scikit-learn
scipy
scikit-optimize  # para otimização bayesiana (gp_minimize)
kagglehub        # para baixar dataset de exemplo (casas em Ponta Grossa/PR)
```
> Instale tudo com: `pip install -U numpy pandas matplotlib seaborn scikit-learn scipy scikit-optimize kagglehub`

## Como executar
1. **Clone** o repositório e entre na pasta:
   ```bash
   git clone https://github.com/SEU_USUARIO/SEU_REPO.git
   cd SEU_REPO
   ```

2. (Opcional) **Crie um ambiente virtual**:
   ```bash
   python -m venv .venv
   # Windows
   .venv\Scripts\activate
   # macOS/Linux
   source .venv/bin/activate
   ```

3. **Instale as dependências** (ver “Requisitos”).

4. **Abra o Jupyter/VS Code** e rode o notebook/código na ordem das seções.

## Dataset (regressão múltipla)
- O exemplo usa o dataset público “Casas à venda em Ponta Grossa/PR” via `kagglehub`.
- O `kagglehub` baixa os arquivos para o cache local. **Atenção**: o caminho completo do arquivo pode variar.
- Se necessário, ajuste a variável `caminho_arquivo` para apontar para o CSV baixado na sua máquina.

## Observações rápidas
- Existem trechos com `input()` para simular “prova real” (ex.: estimar peso por altura). Em ambiente notebook, rode a célula e informe o valor no prompt.
- As visualizações usam `matplotlib`/`seaborn` e podem variar conforme a resolução da tela.
- Evite caminhos absolutos. Prefira caminhos relativos ao projeto.

## Estrutura sugerida (simples)
```
.
├─ notebooks/               # (opcional) colocar o .ipynb aqui
├─ data/                    # (opcional) dados locais, se desejar
├─ README.md
└─ LICENSE                  # (opcional) licença do repositório
```

## Métricas usadas
- **MSE** (Erro Quadrático Médio)
- **RMSE** (Raiz do Erro Quadrático Médio)
- **R²** (Coeficiente de Determinação)
