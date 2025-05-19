# Diagnóstico de Farol de Bicicleta com Rede Bayesiana

Este projeto é o 2º trabalho da disciplina de Inteligência Artificial, com o objetivo de modelar e implementar um sistema de diagnóstico de falha em faróis de bicicleta usando redes bayesianas no **ProbLog**.

## Descrição do Problema

Modelamos a probabilidade da **luz (Li)** estar acesa ou não com base em variáveis como:

- **Str** – Condição da rua: `dry`, `wet`, `snow_covered`
- **Flw** – Volante do dínamo desgastado: `true/false`
- **R** – Dínamo deslizante: `true/false`
- **V** – Dínamo mostra tensão: `true/false`
- **B** – Lâmpada ok: `true/false`
- **K** – Cabo ok: `true/false`
- **Li** – Luz ligada: `true/false`

A estrutura da rede foi construída com base nas independências fornecidas no enunciado e os CPTs foram definidos com valores plausíveis.

## Estrutura dos Arquivos

- `codigoProblog.pl` – Arquivo principal com a rede bayesiana implementada em ProbLog.
- `README.md` – Este arquivo de instruções.

## Como Executar

### 1. Instale o ProbLog

Você pode rodar via navegador ou instalar localmente:

#### Usando o navegador

- Acesse: [https://dtai.cs.kuleuven.be/problog](https://dtai.cs.kuleuven.be/problog)
- Copie e cole o conteúdo do arquivo `codigoProblog.pl` na interface.
- Clique em **Evaluate**.

#### Localmente

1. Requer Python 3.6+ e `pip`
2. Instale o ProbLog via pip:

```bash
pip install problog

3. Execute o código

```bash
problog codigoProblog.pl

