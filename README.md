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

