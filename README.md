![317315020-06e97046-048c-44b8-bd22-3dbd7963e864](https://github.com/user-attachments/assets/444e3177-f80e-41f5-bb3a-a4cadfeb1fa2)

<h1>Estácio - Trabalho Prático | DGT2823 Tecnologias para desenv.
de soluções de big data</h1>



Faculdade Estácio - Polo Castelo - Belo Horizonte - MG.
 
Curso: Desenvolvimento Full Stack.
 
Disciplina: Tecnologias Para Desenv. de Solucoes de Big Data.
 
Número da Turma: 2025.1
 
Semestre Letivo: 5.

Integrante: Samantha Karina Barbosa Torres.

<hr>

<h2>Trabalho Prático   💻</h2>

Através dessa atividade o aluno realizará a limpeza de um conjunto de dados,
tornando-o apto a ser usado em tarefas de mineração/análise de dados.

Contextualização

Como Analista de Dados, você recebeu, em um novo projeto, um conjunto de dados.
Sua principal tarefa é tratar os dados desse conjunto a fim de que possam ser
utilizados para a descoberta de conhecimento através de sua posterior análise e
interpretação. Para tal tarefa, você deverá utilizar a linguagem Python e a biblioteca
Pandas. O passo-a-passo de todo o processo de tratamento dos dados é apresentado a
seguir, no roteiro de prática.

Roteiro de prática 📝

- Material necessário para a prática

  Interpretador Python ou ambiente de codificação (JupyterLab / Jupyter Notebooks /
   Google Colab);
   Biblioteca pandas;
   Editor ou IDE (caso vá utilizar o interpretados python para execução dos scripts
   criados).

 <hr>

- Procedimentos


   Para essa atividade você deverá, obrigatoriamente, utilizar o conjunto de dados
   (fornecido anteriormente, na seção “Contextualização”) composto pelas colunas
   ID;Duration;Date;Pulse;Maxpulse;Calories
   Crie um novo arquivo/script;
   Leia o conteúdo do CSV fornecido, atentando-se para a necessidade ou não de
   incluir parâmetros adicionais como os relativos ao separador dos dados, a engine e
   o enconding;
   Atribua os dados lidos a uma variável;
   Verifique se os dados foram importados adequadamente:
   Imprima as informações gerais sobre o conjunto de dados;
   Imprima as primeiras e últimas N linhas do arquivo.
   Crie uma nova variável e atribua a ela uma cópia do conjunto de dados original
   (variável criada no passo 4);
    Nessa nova variável, contendo uma cópia dos dados:
    Substitua todos os valores nulos da coluna ‘Calories’ por 0;
    Imprima o conjunto de dados para verificar se a mudança acima foi aplicada com
    sucesso;
    Ainda na nova variável:
    Substitua os valores nulos da coluna ‘Date’ por ‘1900/01/01’;
    Imprima o conjunto de dados e confira se a mudança foi aplicada com sucesso;
    Transforme os dados da coluna ‘Date’ em datetime usando o método
    ‘to_datetime’;
    Tendo seguido todas as instruções anteriores, ao executar o passo anterior você
    deverá ter encontrado um erro informando que o valor ‘1900/01/01’ não
    corresponde ao formato ‘%Y/%m/%d’. Para resolver esse problema:
    Substitua, na coluna ‘Date’, o valor ‘1900/01/01’ por ‘NaN’;
    Utilizando o método ‘to_datetime’, repita o passo de transformação dos dados da
    coluna ‘Date’ para datetime;
    Imprima o conjunto de dados para verificar se as mudanças acima foram
    aplicadas com sucesso;
    Nesse ponto, você deverá ter esbarrado em outro erro, informando agora que o valor
    "20201226" não corresponde ao formato "'%Y/%m/%d'" . Você precisará, agora, na
    coluna ‘Date”, transformar especificamente esse valor, atualmente uma string, para
    o formato datetime. Para isso você deverá combinar os métodos ‘replace’ e
    ‘to_datetime’;
    Após o passo anterior, execute novamente a transformação de todos os dados da
    coluna ‘Date’ para o formato datetime (usando o to_datetime). Imprima o conjunto
    de dados atual para verificar se todas as transformações foram executadas com
    sucesso;
    Por fim, remova os registros contendo valores nulos. Nesse ponto, apenas a coluna
    ‘Date’ possui um registro que atende a essa premissa (linha 22). Logo, utilize-a
    como base para realizar a transformação solicitada;
    Imprima o dataframe e verifique se todas as transformações foram executadas
    conforme solicitado nos passos anteriores.
<hr>
   <h1> ✨Conclusão Geral✨</h1> 
   
Com esse trabalho, consegui praticar de maneira clara como usar o Python e o Pandas para realizar leitura, análise e manipulação de dados. Seguindo o roteiro de prática, comecei pela leitura do arquivo CSV e, em seguida, explorei as informações do dataset, identificando erros e inconsistências. Foi possível corrigir problemas como datas fora do padrão e valores faltando, o que tornou a base muito mais organizada.

Depois de todas as correções, percebi na prática como a preparação dos dados é uma etapa essencial antes de qualquer análise. O trabalho me ajudou a entender melhor todo esse processo e mostrou o quanto o Pandas facilita as transformações necessárias. No final, consegui desenvolver mais confiança para manipular dados, visualizar informações importantes e preparar um conjunto de dados para estudos e análises futuras.

Além disso, percebi o quanto o Python e o Pandas são ferramentas incríveis para trabalhar com dados. Com eles dá para automatizar tarefas repetitivas, lidar com grandes volumes de informações de forma prática e deixar tudo organizado e consistente para análise. Isso facilita muito a exploração dos dados e deixa o processo de análise mais rápido e confiável, sem tanta dor de cabeça.
<hr>

<h2> Codigos🎯 </h2>

# As atividades foram desenvolvidas no Google Colab

{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyPrTEm5JRCkY9nqrHdIbgbW",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/samzinha23/Trabalho-Pr-tico-/blob/main/trabalho_pratico_SAM.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": 96,
      "metadata": {
        "id": "0yGQGIAs5X8z"
      },
      "outputs": [],
      "source": [
        "import pandas as pd\n",
        "import numpy as np"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df = pd.read_csv(\"pico_web.csv\", sep=\";\")"
      ],
      "metadata": {
        "id": "oDkWcnYkFg8S"
      },
      "execution_count": 97,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "print(\" Informações gerais 📌\")\n",
        "print(df.info())\n",
        "\n",
        "print(\"Primeiras linhas\")\n",
        "print(df.head())\n",
        "\n",
        "print(\"Últimas linhas\")\n",
        "print(df.tail())\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "47p-E8-R8eOh",
        "outputId": "0a1717f2-eadf-412f-9887-6a6c80686e00"
      },
      "execution_count": 98,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            " Informações gerais 📌\n",
            "<class 'pandas.core.frame.DataFrame'>\n",
            "RangeIndex: 32 entries, 0 to 31\n",
            "Data columns (total 6 columns):\n",
            " #   Column    Non-Null Count  Dtype  \n",
            "---  ------    --------------  -----  \n",
            " 0   ID        32 non-null     int64  \n",
            " 1   Duration  32 non-null     int64  \n",
            " 2   Date      31 non-null     object \n",
            " 3   Pulse     32 non-null     int64  \n",
            " 4   Maxpulse  32 non-null     int64  \n",
            " 5   Calories  30 non-null     float64\n",
            "dtypes: float64(1), int64(4), object(1)\n",
            "memory usage: 1.6+ KB\n",
            "None\n",
            "Primeiras linhas\n",
            "   ID  Duration          Date  Pulse  Maxpulse  Calories\n",
            "0   0        60  '2020/12/01'    110       130    4091.0\n",
            "1   1        60  '2020/12/02'    117       145    4790.0\n",
            "2   2        60  '2020/12/03'    103       135    3400.0\n",
            "3   3        45  '2020/12/04'    109       175    2824.0\n",
            "4   4        45  '2020/12/05'    117       148    4060.0\n",
            "Últimas linhas\n",
            "    ID  Duration          Date  Pulse  Maxpulse  Calories\n",
            "27  27        60  '2020/12/27'     92       118    2410.0\n",
            "28  28        60  '2020/12/28'    103       132       NaN\n",
            "29  29        60  '2020/12/29'    100       132    2800.0\n",
            "30  30        60  '2020/12/30'    102       129    3803.0\n",
            "31  31        60  '2020/12/31'     92       115    2430.0\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df2 = df.copy()"
      ],
      "metadata": {
        "id": "LjEuyyWe93pB"
      },
      "execution_count": 99,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "df2[\"Calories\"] = df2[\"Calories\"].fillna(0)\n",
        "print(df2)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "-XMjXc2o9-YB",
        "outputId": "714186bf-ab77-4cf9-b0c0-ab71578d99ad"
      },
      "execution_count": 100,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "    ID  Duration          Date  Pulse  Maxpulse  Calories\n",
            "0    0        60  '2020/12/01'    110       130    4091.0\n",
            "1    1        60  '2020/12/02'    117       145    4790.0\n",
            "2    2        60  '2020/12/03'    103       135    3400.0\n",
            "3    3        45  '2020/12/04'    109       175    2824.0\n",
            "4    4        45  '2020/12/05'    117       148    4060.0\n",
            "5    5        60  '2020/12/06'    102       127    3000.0\n",
            "6    6        60  '2020/12/07'    110       136    3740.0\n",
            "7    7       450  '2020/12/08'    104       134    2533.0\n",
            "8    8        30  '2020/12/09'    109       133    1951.0\n",
            "9    9        60  '2020/12/10'     98       124    2690.0\n",
            "10  10        60  '2020/12/11'    103       147    3293.0\n",
            "11  11        60  '2020/12/12'    100       120    2507.0\n",
            "12  12        60  '2020/12/12'    100       120    2507.0\n",
            "13  13        60  '2020/12/13'    106       128    3453.0\n",
            "14  14        60  '2020/12/14'    104       132    3793.0\n",
            "15  15        60  '2020/12/15'     98       123    2750.0\n",
            "16  16        60  '2020/12/16'     98       120    2152.0\n",
            "17  17        60  '2020/12/17'    100       120    3000.0\n",
            "18  18        45  '2020/12/18'     90       112       0.0\n",
            "19  19        60  '2020/12/19'    103       123    3230.0\n",
            "20  20        45  '2020/12/20'     97       125    2430.0\n",
            "21  21        60  '2020/12/21'    108       131    3642.0\n",
            "22  22        45           NaN    100       119    2820.0\n",
            "23  23        60  '2020/12/23'    130       101    3000.0\n",
            "24  24        45  '2020/12/24'    105       132    2460.0\n",
            "25  25        60  '2020/12/25'    102       126    3345.0\n",
            "26  26        60      20201226    100       120    2500.0\n",
            "27  27        60  '2020/12/27'     92       118    2410.0\n",
            "28  28        60  '2020/12/28'    103       132       0.0\n",
            "29  29        60  '2020/12/29'    100       132    2800.0\n",
            "30  30        60  '2020/12/30'    102       129    3803.0\n",
            "31  31        60  '2020/12/31'     92       115    2430.0\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df2[\"Date\"] = df2[\"Date\"].fillna(\"1900/01/01\")\n",
        "print(df2)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "oV9-QImf-B9h",
        "outputId": "f1c821ef-4222-44a6-abc0-8e31342e516f"
      },
      "execution_count": 101,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "    ID  Duration          Date  Pulse  Maxpulse  Calories\n",
            "0    0        60  '2020/12/01'    110       130    4091.0\n",
            "1    1        60  '2020/12/02'    117       145    4790.0\n",
            "2    2        60  '2020/12/03'    103       135    3400.0\n",
            "3    3        45  '2020/12/04'    109       175    2824.0\n",
            "4    4        45  '2020/12/05'    117       148    4060.0\n",
            "5    5        60  '2020/12/06'    102       127    3000.0\n",
            "6    6        60  '2020/12/07'    110       136    3740.0\n",
            "7    7       450  '2020/12/08'    104       134    2533.0\n",
            "8    8        30  '2020/12/09'    109       133    1951.0\n",
            "9    9        60  '2020/12/10'     98       124    2690.0\n",
            "10  10        60  '2020/12/11'    103       147    3293.0\n",
            "11  11        60  '2020/12/12'    100       120    2507.0\n",
            "12  12        60  '2020/12/12'    100       120    2507.0\n",
            "13  13        60  '2020/12/13'    106       128    3453.0\n",
            "14  14        60  '2020/12/14'    104       132    3793.0\n",
            "15  15        60  '2020/12/15'     98       123    2750.0\n",
            "16  16        60  '2020/12/16'     98       120    2152.0\n",
            "17  17        60  '2020/12/17'    100       120    3000.0\n",
            "18  18        45  '2020/12/18'     90       112       0.0\n",
            "19  19        60  '2020/12/19'    103       123    3230.0\n",
            "20  20        45  '2020/12/20'     97       125    2430.0\n",
            "21  21        60  '2020/12/21'    108       131    3642.0\n",
            "22  22        45    1900/01/01    100       119    2820.0\n",
            "23  23        60  '2020/12/23'    130       101    3000.0\n",
            "24  24        45  '2020/12/24'    105       132    2460.0\n",
            "25  25        60  '2020/12/25'    102       126    3345.0\n",
            "26  26        60      20201226    100       120    2500.0\n",
            "27  27        60  '2020/12/27'     92       118    2410.0\n",
            "28  28        60  '2020/12/28'    103       132       0.0\n",
            "29  29        60  '2020/12/29'    100       132    2800.0\n",
            "30  30        60  '2020/12/30'    102       129    3803.0\n",
            "31  31        60  '2020/12/31'     92       115    2430.0\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "print(\"\\n Tentativa de conversão (deve gerar erro):\")\n",
        "try:\n",
        "    pd.to_datetime(df2[\"Date\"], format=\"%Y/%m/%d\")\n",
        "except Exception as e:\n",
        "    print(\"ERRO GERADO :\", e)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "r_W81ok8Vye6",
        "outputId": "bb45c0a8-0525-4a97-ea5c-134bfc8a1432"
      },
      "execution_count": 102,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            " Tentativa de conversão (deve gerar erro):\n",
            "ERRO GERADO : time data \"'2020/12/01'\" doesn't match format \"%Y/%m/%d\", at position 0. You might want to try:\n",
            "    - passing `format` if your strings have a consistent format;\n",
            "    - passing `format='ISO8601'` if your strings are all ISO8601 but not necessarily in exactly the same format;\n",
            "    - passing `format='mixed'`, and the format will be inferred for each element individually. You might want to use `dayfirst` alongside this.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df2[\"Date\"] = df2[\"Date\"].replace(\"1900/01/01\", np.nan)\n",
        "print(\"\\nApós remover '1900/01/01':\")\n",
        "print(df2)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "PAA0IdmVNq0z",
        "outputId": "4d419704-3092-478b-e642-2e73249747ae"
      },
      "execution_count": 103,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            "Após remover '1900/01/01':\n",
            "    ID  Duration          Date  Pulse  Maxpulse  Calories\n",
            "0    0        60  '2020/12/01'    110       130    4091.0\n",
            "1    1        60  '2020/12/02'    117       145    4790.0\n",
            "2    2        60  '2020/12/03'    103       135    3400.0\n",
            "3    3        45  '2020/12/04'    109       175    2824.0\n",
            "4    4        45  '2020/12/05'    117       148    4060.0\n",
            "5    5        60  '2020/12/06'    102       127    3000.0\n",
            "6    6        60  '2020/12/07'    110       136    3740.0\n",
            "7    7       450  '2020/12/08'    104       134    2533.0\n",
            "8    8        30  '2020/12/09'    109       133    1951.0\n",
            "9    9        60  '2020/12/10'     98       124    2690.0\n",
            "10  10        60  '2020/12/11'    103       147    3293.0\n",
            "11  11        60  '2020/12/12'    100       120    2507.0\n",
            "12  12        60  '2020/12/12'    100       120    2507.0\n",
            "13  13        60  '2020/12/13'    106       128    3453.0\n",
            "14  14        60  '2020/12/14'    104       132    3793.0\n",
            "15  15        60  '2020/12/15'     98       123    2750.0\n",
            "16  16        60  '2020/12/16'     98       120    2152.0\n",
            "17  17        60  '2020/12/17'    100       120    3000.0\n",
            "18  18        45  '2020/12/18'     90       112       0.0\n",
            "19  19        60  '2020/12/19'    103       123    3230.0\n",
            "20  20        45  '2020/12/20'     97       125    2430.0\n",
            "21  21        60  '2020/12/21'    108       131    3642.0\n",
            "22  22        45           NaN    100       119    2820.0\n",
            "23  23        60  '2020/12/23'    130       101    3000.0\n",
            "24  24        45  '2020/12/24'    105       132    2460.0\n",
            "25  25        60  '2020/12/25'    102       126    3345.0\n",
            "26  26        60      20201226    100       120    2500.0\n",
            "27  27        60  '2020/12/27'     92       118    2410.0\n",
            "28  28        60  '2020/12/28'    103       132       0.0\n",
            "29  29        60  '2020/12/29'    100       132    2800.0\n",
            "30  30        60  '2020/12/30'    102       129    3803.0\n",
            "31  31        60  '2020/12/31'     92       115    2430.0\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df2[\"Date\"] = df2[\"Date\"].replace(\"20201226\", \"2020/12/26\")"
      ],
      "metadata": {
        "id": "sbtMDvNdN1-6"
      },
      "execution_count": 104,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "df2[\"Date\"] = pd.to_datetime(df2[\"Date\"], format=\"%Y/%m/%d\")\n",
        "\n",
        "print(\"\\nApós conversão completa para datetime:\")\n",
        "print(df2)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 508
        },
        "id": "sCr2an1_BGFy",
        "outputId": "3b3f373a-d817-418a-89ec-15505a60845f"
      },
      "execution_count": 105,
      "outputs": [
        {
          "output_type": "error",
          "ename": "ValueError",
          "evalue": "time data \"'2020/12/01'\" doesn't match format \"%Y/%m/%d\", at position 0. You might want to try:\n    - passing `format` if your strings have a consistent format;\n    - passing `format='ISO8601'` if your strings are all ISO8601 but not necessarily in exactly the same format;\n    - passing `format='mixed'`, and the format will be inferred for each element individually. You might want to use `dayfirst` alongside this.",
          "traceback": [
            "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
            "\u001b[0;31mValueError\u001b[0m                                Traceback (most recent call last)",
            "\u001b[0;32m/tmp/ipython-input-2117971595.py\u001b[0m in \u001b[0;36m<cell line: 0>\u001b[0;34m()\u001b[0m\n\u001b[0;32m----> 1\u001b[0;31m \u001b[0mdf2\u001b[0m\u001b[0;34m[\u001b[0m\u001b[0;34m\"Date\"\u001b[0m\u001b[0;34m]\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0mpd\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mto_datetime\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mdf2\u001b[0m\u001b[0;34m[\u001b[0m\u001b[0;34m\"Date\"\u001b[0m\u001b[0;34m]\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mformat\u001b[0m\u001b[0;34m=\u001b[0m\u001b[0;34m\"%Y/%m/%d\"\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m      2\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m      3\u001b[0m \u001b[0mprint\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0;34m\"\\nApós conversão completa para datetime:\"\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m      4\u001b[0m \u001b[0mprint\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mdf2\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n",
            "\u001b[0;32m/usr/local/lib/python3.12/dist-packages/pandas/core/tools/datetimes.py\u001b[0m in \u001b[0;36mto_datetime\u001b[0;34m(arg, errors, dayfirst, yearfirst, utc, format, exact, unit, infer_datetime_format, origin, cache)\u001b[0m\n\u001b[1;32m   1065\u001b[0m             \u001b[0mresult\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0marg\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mmap\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mcache_array\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m   1066\u001b[0m         \u001b[0;32melse\u001b[0m\u001b[0;34m:\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m-> 1067\u001b[0;31m             \u001b[0mvalues\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0mconvert_listlike\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0marg\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0m_values\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mformat\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m   1068\u001b[0m             \u001b[0mresult\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0marg\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0m_constructor\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mvalues\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mindex\u001b[0m\u001b[0;34m=\u001b[0m\u001b[0marg\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mindex\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mname\u001b[0m\u001b[0;34m=\u001b[0m\u001b[0marg\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mname\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m   1069\u001b[0m     \u001b[0;32melif\u001b[0m \u001b[0misinstance\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0marg\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0;34m(\u001b[0m\u001b[0mABCDataFrame\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mabc\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mMutableMapping\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m:\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n",
            "\u001b[0;32m/usr/local/lib/python3.12/dist-packages/pandas/core/tools/datetimes.py\u001b[0m in \u001b[0;36m_convert_listlike_datetimes\u001b[0;34m(arg, format, name, utc, unit, errors, dayfirst, yearfirst, exact)\u001b[0m\n\u001b[1;32m    431\u001b[0m     \u001b[0;31m# `format` could be inferred, or user didn't ask for mixed-format parsing.\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m    432\u001b[0m     \u001b[0;32mif\u001b[0m \u001b[0mformat\u001b[0m \u001b[0;32mis\u001b[0m \u001b[0;32mnot\u001b[0m \u001b[0;32mNone\u001b[0m \u001b[0;32mand\u001b[0m \u001b[0mformat\u001b[0m \u001b[0;34m!=\u001b[0m \u001b[0;34m\"mixed\"\u001b[0m\u001b[0;34m:\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m--> 433\u001b[0;31m         \u001b[0;32mreturn\u001b[0m \u001b[0m_array_strptime_with_fallback\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0marg\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mname\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mutc\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mformat\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mexact\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0merrors\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m    434\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m    435\u001b[0m     result, tz_parsed = objects_to_datetime64(\n",
            "\u001b[0;32m/usr/local/lib/python3.12/dist-packages/pandas/core/tools/datetimes.py\u001b[0m in \u001b[0;36m_array_strptime_with_fallback\u001b[0;34m(arg, name, utc, fmt, exact, errors)\u001b[0m\n\u001b[1;32m    465\u001b[0m     \u001b[0mCall\u001b[0m \u001b[0marray_strptime\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0;32mwith\u001b[0m \u001b[0mfallback\u001b[0m \u001b[0mbehavior\u001b[0m \u001b[0mdepending\u001b[0m \u001b[0mon\u001b[0m \u001b[0;34m'errors'\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m    466\u001b[0m     \"\"\"\n\u001b[0;32m--> 467\u001b[0;31m     \u001b[0mresult\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mtz_out\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0marray_strptime\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0marg\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mfmt\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mexact\u001b[0m\u001b[0;34m=\u001b[0m\u001b[0mexact\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0merrors\u001b[0m\u001b[0;34m=\u001b[0m\u001b[0merrors\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mutc\u001b[0m\u001b[0;34m=\u001b[0m\u001b[0mutc\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m    468\u001b[0m     \u001b[0;32mif\u001b[0m \u001b[0mtz_out\u001b[0m \u001b[0;32mis\u001b[0m \u001b[0;32mnot\u001b[0m \u001b[0;32mNone\u001b[0m\u001b[0;34m:\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m    469\u001b[0m         \u001b[0munit\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0mnp\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mdatetime_data\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mresult\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mdtype\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m[\u001b[0m\u001b[0;36m0\u001b[0m\u001b[0;34m]\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n",
            "\u001b[0;32mstrptime.pyx\u001b[0m in \u001b[0;36mpandas._libs.tslibs.strptime.array_strptime\u001b[0;34m()\u001b[0m\n",
            "\u001b[0;32mstrptime.pyx\u001b[0m in \u001b[0;36mpandas._libs.tslibs.strptime.array_strptime\u001b[0;34m()\u001b[0m\n",
            "\u001b[0;32mstrptime.pyx\u001b[0m in \u001b[0;36mpandas._libs.tslibs.strptime._parse_with_format\u001b[0;34m()\u001b[0m\n",
            "\u001b[0;31mValueError\u001b[0m: time data \"'2020/12/01'\" doesn't match format \"%Y/%m/%d\", at position 0. You might want to try:\n    - passing `format` if your strings have a consistent format;\n    - passing `format='ISO8601'` if your strings are all ISO8601 but not necessarily in exactly the same format;\n    - passing `format='mixed'`, and the format will be inferred for each element individually. You might want to use `dayfirst` alongside this."
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df2 = df2.dropna(subset=[\"Date\"])\n",
        "print(\"DataFrame Final ✨\")\n",
        "print(df2)\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "i3CAyvFrBVNZ",
        "outputId": "9249db3f-394f-489b-fa11-5738f5cb8b4a"
      },
      "execution_count": 106,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "DataFrame Final ✨\n",
            "    ID  Duration          Date  Pulse  Maxpulse  Calories\n",
            "0    0        60  '2020/12/01'    110       130    4091.0\n",
            "1    1        60  '2020/12/02'    117       145    4790.0\n",
            "2    2        60  '2020/12/03'    103       135    3400.0\n",
            "3    3        45  '2020/12/04'    109       175    2824.0\n",
            "4    4        45  '2020/12/05'    117       148    4060.0\n",
            "5    5        60  '2020/12/06'    102       127    3000.0\n",
            "6    6        60  '2020/12/07'    110       136    3740.0\n",
            "7    7       450  '2020/12/08'    104       134    2533.0\n",
            "8    8        30  '2020/12/09'    109       133    1951.0\n",
            "9    9        60  '2020/12/10'     98       124    2690.0\n",
            "10  10        60  '2020/12/11'    103       147    3293.0\n",
            "11  11        60  '2020/12/12'    100       120    2507.0\n",
            "12  12        60  '2020/12/12'    100       120    2507.0\n",
            "13  13        60  '2020/12/13'    106       128    3453.0\n",
            "14  14        60  '2020/12/14'    104       132    3793.0\n",
            "15  15        60  '2020/12/15'     98       123    2750.0\n",
            "16  16        60  '2020/12/16'     98       120    2152.0\n",
            "17  17        60  '2020/12/17'    100       120    3000.0\n",
            "18  18        45  '2020/12/18'     90       112       0.0\n",
            "19  19        60  '2020/12/19'    103       123    3230.0\n",
            "20  20        45  '2020/12/20'     97       125    2430.0\n",
            "21  21        60  '2020/12/21'    108       131    3642.0\n",
            "23  23        60  '2020/12/23'    130       101    3000.0\n",
            "24  24        45  '2020/12/24'    105       132    2460.0\n",
            "25  25        60  '2020/12/25'    102       126    3345.0\n",
            "26  26        60    2020/12/26    100       120    2500.0\n",
            "27  27        60  '2020/12/27'     92       118    2410.0\n",
            "28  28        60  '2020/12/28'    103       132       0.0\n",
            "29  29        60  '2020/12/29'    100       132    2800.0\n",
            "30  30        60  '2020/12/30'    102       129    3803.0\n",
            "31  31        60  '2020/12/31'     92       115    2430.0\n"
          ]
        }
      ]
    }
  ]
}


