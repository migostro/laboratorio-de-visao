# MAC5768 EP 2022

| **Nome**                         | **NUSP** |
|:--------------------------------:|:--------:|
| Aldomar Pietro Santana Silva     | 10770162 |
| Arthur Sakayan                   | 10297647 |
| Eduarda Ramos Bezerra de Alencar | 10372540 |
| Mateus Santos Freire             | 11796889 |
| Miguel Pereira Ostrowski         | 10723610 |
| Rafael Badain                    | 10277102 |

# Parte 1: Aquisição de Imagens + Formação do Dataset
1. Captura de imagens [DONE]
2. Organização da base de imagens [DONE]
3. Criação do Jupyter Notebook [TODO]
4. Criação do projeto no GitHub com README explicativo sobre o EP com link para o dataset [DONE]

## Descrição do Dataset
[Link para o Dataset no Google Drive](https://drive.google.com/drive/u/1/folders/1N5sFs_M7oD0psaO6KZeyeMq2CqmY-haO)

### Tabela Sumária

| **Descrição**         | **Valor**                |
|:---------------------:|:------------------------:|
| Número de Classes     | 10                       |
| Número de Imagens     | 1080                     |
| Tamanho da Base       | 2144 MB                  |
| Resolução das Imagens | 4608x3456                |
| dpi                   | 180                      |
| Intensidade de Bits   | 24                       |
| Câmera                | Canon PowerShot SX530 HS |

### Tabela Detalhada por Classe

| **#** | **Classe** | **Número de Objetos** | **Fundos** | **Ambientes** | **Horários** | **Repetições** | **Número de Imagens** |
|:-----:|:----------:|:---------------------:|:----------:|:-------------:|:------------:|:--------------:|:---------------------:|
| 1     | Borracha   | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 2     | Carta      | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 3     | Celular    | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 4     | Concha     | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 5     | Copo       | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 6     | Dado       | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 7     | Estátua    | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 8     | Lápis      | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 9     | Tubo       | 3                     | 3          | 2             | 2            | 3              | 108                   |
| 10    | Vela       | 3                     | 3          | 2             | 2            | 3              | 108                   |

> (3 objetos * (2 horários * 2 ambientes * 3 fundos)) * 3 repetições = 108 fotos por classe

> Fundos: Branco, Preto e Variado

# Parte 2:

## Data Augumentation
1. Converter o dataset em tons de cinza RGB2GRAY
2. Soma de fundo com gradiente de níveis de cinza
3. Logaritmo da Imagem
4. Exponencial da Imagem
5. Filtro da média implementado usando **convolução**

## Normalização
1. Protótipo Médio
2. Histograma Médio
3. Variância do Histograma de cada classe

# Parte 3:

## Segmentação
1. Segmentar manualmente o objeto de interesse e produzir ground truths
2. Elaborar uma função de segmentação automática
3. Elaborar uma função de dextração do bounding box
4. Avaliar os resultados da extração do bounding box e segmentação (comparar com ground truths)

> Como cada classe contém 108 amostras, 108 * 0,15 ~= 16 images são segmentadas manualmente

# Classificação
5. Elaborar uma função para extrair os feature vectors da imagem
6. Usar um algoritmo para classificar os objetos
