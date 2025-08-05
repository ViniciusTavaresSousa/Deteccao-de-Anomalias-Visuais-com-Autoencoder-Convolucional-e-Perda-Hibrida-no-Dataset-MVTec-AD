<div align="center">

# Detecção de Anomalias Visuais com Autoencoder Convolucional e Perda Híbrida no Dataset MVTec AD

----------

[![python](https://img.shields.io/badge/python-3.11.13-green)]()
[![tensorflow](https://img.shields.io/badge/tensorflow-2.18.0-orange)]()
[![numpy](https://img.shields.io/badge/numpy-2.0.2-blue)]()

----------

<div align="left">

## Introdução

Este projeto apresenta uma implementação simples de um Autoencoder Convolucional para detecção de anomalias visuais em imagens industriais do dataset MVTec AD. O modelo é treinado de forma não supervisionada usando imagens sem defeitos e emprega uma função de perda híbrida que combina Erro Quadrático Médio (MSE) e Índice de Similaridade Estrutural (SSIM), visando melhorar a sensibilidade à detecção de defeitos.

## Dataset

O dataset MVTec AD contém imagens de 15 categorias diferentes de produtos industriais com e sem defeitos. Este projeto foca na categoria *bottle*, que possui imagens de alta resolução com defeitos variados, como *broken_large*, *broken_small* e *contamination*.


### Estrutura de Diretórios

As imagens devem estar organizadas conforme a estrutura abaixo na pasta `/content/drive/MyDrive/Autoencoder_MVTecAD/mvtec`:

```text
bottle
├── train
│   └── good        
└── test
    ├── broken_large
    ├── broken_small
    ├── contamination
    └── good
```

### Arquivo `.npy` para Treinamento

Você também pode carregar diretamente o arquivo `.npy` com as imagens pré-processadas (em escala de cinza e redimensionadas) da categoria *bottle*:

🔗 [Download do dataset `bottle_dataset.npy` no Google Drive](https://drive.google.com/file/d/1e0pE247lPZv9-veQOlGr9qhkM4XUlS5A/view?usp=drive_link)

## Dependências

As principais bibliotecas utilizadas neste projeto são:

* `tensorflow >= 2.18`  (para construção e treinamento do modelo, incluindo cálculo SSIM)
* `numpy >= 2.0`        (manipulação e processamento de arrays)
* `matplotlib`          (visualização de resultados)
* `opencv-python`       (carregamento e pré-processamento das imagens)

## Resultados

<div align="center">

<img src="resultados/bottle_broken_large.png" width="400" alt="Bottle - Broken Large"/>
<img src="resultados/bottle_broken_small.png" width="400" alt="Bottle - Broken Small"/>
<img src="resultados/bottle_contamination.png" width="400" alt="Bottle - Contamination"/>
<img src="resultados/capsule_crack.png" width="400" alt="Capsule - Crack"/>

</div>

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.

## Referências

* https://github.com/ViniciusTavaresSousa/Deteccao-de-Anomalias-Visuais-com-Autoencoder-Convolucional-e-Perda-Hibrida-no-Dataset-MVTec-AD  

</div>

