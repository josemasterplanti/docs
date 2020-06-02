# Lote de produção

Um **lote de produção** é um conjunto de informações que caracteriza determinado produto, de quantidade limitada, originado de processo produtivo ou compra, estando em processo de produção ou não, identificado por uma sequência alfanumérica (**"Lote"**) e por um código sequencial (**"Código"**).



#### Exemplos de lotes de produção

| CÓDIGO |  LOTE  |    DATA    |    ORIGEM     | PRODUTO                  |    UN    | QTDADE. |
| :----: | :----: | :--------: | :-----------: | ------------------------ | :------: | ------: |
| 000001 | AA0001 | 01/01/2020 |    SEMEIO     | MUDA DE ALFACE           | BANDEJAS |     100 |
| 000002 | AA0002 | 03/04/2019 | ESTAQUEAMENTO | ALECRIM                  |   VASO   |    1000 |
| 000003 | AA0003 | 28/08/2018 | MULTIPLICAÇÃO | BANANA                   | EXPLANTE |     200 |
| 000004 | AA0004 | 12/03/2020 |  EMBALAMENTO  | BANDEJA DE TOMATE        | UNIDADE  |      50 |
| 000005 | AA0005 | 15/04/2020 |   COLHEITA    | PIMENTÃO                 |  CAIXA   |      80 |
| 000006 | AA0006 | 07/02/2020 |   ENXERTIA    | MUDA DE CITROS           | UNIDADE  |   25000 |
| 000007 | AA0009 | 25/01/2020 |    COMPRA     | ABOBRINHA BRANCA         |  CAIXA   |      65 |
| 000008 | AA0009 | 01/02/2020 | CLASSIFICAÇÃO | ABOBRINHA BRANCA GRANEL  |  CAIXA   |      90 |
| 000009 | AA0011 | 05/05/2020 |    PLANTIO    | VASO DE ANTÚRIO          | UNIDADE  |     980 |
| 000010 | AA0012 | 07/03/2020 |    PLANTIO    | MUDA PRÉ BROTADA DE CANA | UNIDADE  |   80000 |
| 000011 | AA0013 | 08/04/2020 |   ENXERTIA    | TOMATE                   | UNIDADE  |  128000 |



#### Identificação de lotes de produção

Para facilitar a identificação dos lotes de produção, utiliza-se a informação **"Lote"**, que é composta por duas letra e quatro números, preenchido sequencialmente de AA0001 até ZZ9999, reiniciando após a ultima serie, esta identificação de  **"Lote"** também pode ser informada manualmente respeitando o limite de 6 caracteres.

Como a informação **"Lote"** pode ser compartilhada para mais de um produto, é utilizada a informação **"Código"** (Numeração sequencial) para identificação única de um lote produção ou de uma fração do lote de produção original.



#### Identificação de lotes de produção fracionados

Um lote de produção pode ser fracionado pelos mais diversos motivos, exemplo:

1. Formação do lote original

| ESTUFA | CÓDIGO | CÓDIGO <br />REFERÊNCIA | CODIGO <br />ORIGEM |  LOTE  | PRODUTO      | QUANTIDADE |
| ------ | :----: | :---------------------: | :-----------------: | :----: | ------------ | ---------: |
| EST01  | 000001 |         000001          |       000001        | AA0001 | MUDA DE CAFÉ |      10000 |

2. Divisão do lote de produção original em duas estufas

| ESTUFA | CÓDIGO | CÓDIGO <br />REFERÊNCIA | CODIGO <br />ORIGEM |  LOTE  | PRODUTO      | QUANTIDADE |
| ------ | :----: | :---------------------: | :-----------------: | :----: | ------------ | ---------: |
| EST02  | 000002 |         000001          |       000001        | AA0001 | MUDA DE CAFÉ |       5000 |
| EST03  | 000003 |         000001          |       000001        | AA0001 | MUDA DE CAFÉ |       5000 |

3. Sub-divisão das frações dos lotes de produção em duas estufas

| ESTUFA | CÓDIGO | CÓDIGO <br />REFERÊNCIA | CODIGO <br />ORIGEM |  LOTE  | PRODUTO      | QUANTIDADE |
| ------ | :----: | :---------------------: | :-----------------: | :----: | ------------ | ---------: |
| EST04  | 000004 |         000001          |       000003        | AA0001 | MUDA DE CAFÉ |       2500 |
| EST05  | 000005 |         000001          |       000003        | AA0001 | MUDA DE CAFÉ |       2500 |
| EST04  | 000006 |         000001          |       000002        | AA0001 | MUDA DE CAFÉ |       1000 |
| EST06  | 000007 |         000001          |       000002        | AA0001 | MUDA DE CAFÉ |       4000 |



#### Rastreabilidade do Código

Um lote de produção, além da informação **"Lote"** e **"Código"**, possui mais duas informações que permite o rastreamento do lote de produção, são elas:

- **Código Referência**

   Todas as frações do lote compartilham o mesmo código referência do lote original.

- **Código Origem**

  Armazena o código do lote precedente, ou seja que originou a fração do lote. 



![Rastreabilidade do Código](https://mpimages.blob.core.windows.net/docs/lote_de_producao_rastreabilidade_codigo.png)

