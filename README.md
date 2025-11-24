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
 <img width="629" height="789" alt="Captura de tela 2025-11-24 195111" src="https://github.com/user-attachments/assets/7b696803-6883-437b-8337-b3a93123846d" />



