<div align="center">

# Detecção de Anomalias Visuais para Controle de Qualidade

----------

[![python](https://img.shields.io/badge/python-3.8%2B-green)]()
[![tensorflow](https://img.shields.io/badge/tensorflow-2.10%2B-orange)]()
[![numpy](https://img.shields.io/badge/numpy-1.22%2B-blue)]()

----------

<div align="left">

## Introdução

Este projeto apresenta uma implementação simples de um Autoencoder Convolucional para detecção de anomalias visuais em imagens industriais do dataset MVTec AD. O modelo é treinado de forma não supervisionada usando imagens sem defeitos e emprega uma função de perda híbrida que combina Erro Quadrático Médio (MSE) e Índice de Similaridade Estrutural (SSIM), visando melhorar a sensibilidade à detecção de defeitos.

## Dataset

O dataset MVTec AD contém imagens de 15 categorias diferentes de produtos industriais com e sem defeitos. Este projeto foca na categoria \textit{bottle}, que possui imagens de alta resolução com defeitos variados, como \textit{broken\_large}, \textit{broken\_small} e \textit{contamination}.

### Estrutura de Diretórios

As imagens devem estar organizadas conforme a estrutura abaixo na pasta `data/`:

├── bottle
│ ├── test
│ │ ├── broken_large
│ │ ├── broken_small
│ │ ├── contamination
│ │ └── good
│ └── train
│ └── good


## Dependências

As principais bibliotecas utilizadas neste projeto são:

* `tensorflow >= 2.10`
* `numpy >= 1.22`
* `matplotlib`
* `scikit-image` (para cálculo de SSIM)

Consulte o arquivo `requirements.txt` para a lista completa.

## Resultados

<div align="center">

### Exemplo - Imagem com defeito

<img src="imgs/defeito_entrada.png" width="400" alt="Imagem com defeito"/>
<img src="imgs/defeito_reconstrucao.png" width="400" alt="Reconstrução"/>
<img src="imgs/defeito_mapa_erro.png" width="400" alt="Mapa de erro (1-SSIM)"/>

### Exemplo - Imagem normal

<img src="imgs/boa_entrada.png" width="400" alt="Imagem normal"/>
<img src="imgs/boa_reconstrucao.png" width="400" alt="Reconstrução"/>
<img src="imgs/boa_mapa_erro.png" width="400" alt="Mapa de erro (1-SSIM)"/>

</div>

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE.md para detalhes.

## Referências

* Bergmann, Paul, et al. -- Improving unsupervised defect segmentation by applying structural similarity to autoencoders, 2018  
* https://github.com/ViniciusTavaresSousa/Deteccao-de-Anomalias-Visuais-com-Autoencoder-Convolucional-e-SSIM-no-Dataset-MVTec-AD  
* https://github.com/VainF/pytorch-msssim  

</div>

