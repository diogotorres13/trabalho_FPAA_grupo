# PathFinder - Solução de Labirintos 2D com o Algoritmo A*

Este projeto utiliza o algoritmo **A*** para determinar o caminho mais curto dentro de um labirinto bidimensional, conectando um ponto inicial (S) a um ponto final (E) enquanto evita obstáculos.

## Descrição do Problema

O desafio consiste em encontrar a rota mínima em um labirinto 2D, onde:

- **'S'** representa o ponto de partida  
- **'E'** indica o destino final  
- **'0'** corresponde a espaços livres  
- **'1'** simboliza obstáculos  

Os movimentos são permitidos apenas nas direções **cima**, **baixo**, **esquerda** e **direita**, e cada passo tem custo **1**.

## Algoritmo A*

O **A*** é um algoritmo de busca heurística que combina:

- **g(n):** custo real do caminho do ponto inicial até o nó atual  
- **h(n):** estimativa do custo do nó atual até o destino  

A função de avaliação é dada por:

```
f(n) = g(n) + h(n)
```

Essa função define a prioridade de exploração dos nós durante a busca.

### Heurística

A heurística utilizada é a **distância de Manhattan**, calculada da seguinte forma:

```
h(n) = |x_atual - x_final| + |y_atual - y_final|
```

## Requisitos

- **Python 3.7+**  
- **NumPy**

## Instalação

1. Clone o repositório:

```bash
git clone https://github.com/diogotorres13/trabalho_FPAA_grupo.git
```

2. Instale as dependências:

```bash
pip install -r requirements.txt
```

## Uso

Para executar o programa:

```bash
python pathfinder.py
```

O script irá:

1. Carregar um labirinto de exemplo  
2. Calcular o menor caminho utilizando o algoritmo A*  
3. Exibir o trajeto em formato de coordenadas  
4. Mostrar o labirinto com o caminho marcado

## Exemplo de Saída

Para o seguinte labirinto:

```
S 0 1 0 0
0 0 1 0 1
0 1 0 0 0
1 0 0 E 1
```

A saída será:

```
Menor caminho (em coordenadas):
[(0, 0), (1, 0), (1, 1), (2, 1), (3, 1), (3, 2), (3, 3)]

Labirinto com o caminho marcado:
S 0 1 0 0
* * 1 0 1
1 * 1 0 0
1 * * E 1
```

## Estrutura do Código

- **`Node`**: Classe que representa um nó dentro do labirinto  
- **`PathFinder`**: Classe principal que implementa o algoritmo A*  
- Funções auxiliares responsáveis pela leitura, manipulação e visualização do labirinto  

# pathfinder
