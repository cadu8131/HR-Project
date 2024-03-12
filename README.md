# Uma solução para um problema de RH

<p align="justify"> Uma empresa indiana surge com a seguinte problemática: em média, 15% dos funcionários se demitem todos os anos. Isso quer dizer que projetos de atrasam, o nome da empresa no mercado fica em risco, com outros funcionários e com clientes, e além disso, gera um custo adicional com o processo de seleção de novos funcionários. Possuindo diversos dados dessa empresa, precisamos estudar a situação dos funcionários ao longo de um ano (que se demitiram e também os que ainda continuam) e analisar possíveis causas desses eventos. Além disso, iremos desenvolver um modelo de Machine Learning para realizar previsões e orientar os executivos dessa empresa, que nos contraram, a tomar as melhores decisões com finalidade de evitar esses pedidos de demissões excessivos.

Nosso dataset é composto por quatro tabelas, sendo elas:

manager_survey_data: Contém informações dos gestores a respeito dos funcionários
employee_survey_data: Contém informações dos funcionários a respeito do que estão achando da experiência de trabalhar no local. \
in_time e out_time: Duas tabelas contendo informações a respeito do horário de chegada e de larga dos funcionários no período de um ano, sem contar os finais de semana. _ general_data: Essa é a maior tabela. Ela possui dados gerais a respeito dos funcionários, como salário, cargo, tempo na empresa, entre outros. \
general_data: Essa é a maior tabela. Ela possui dados gerais a respeito dos funcionários, como salário, cargo, tempo na empresa, entre outros.

### O perfil dos funcionários

Vamos entender inicialmente o perfil dos funcionários, a começar pela distribuição da idade
![Logo](Imagens\1.png) 
<p align="justify"> é notório que a distribuição da idade está centrada nos adultos entre 30 e 40 anos, isso se confirma pela média da idade das pessoas que se demitem ser menor que a média da idade das pessoas que continuam na empresa (respectivamente 33 e 37). Além disso, a empresa possui uma considerável quantidade a mais de homens que mulheres 
![Logo](R\2.png) 


Como sabemos, é comum existir disparidade salarial entre homens e mulheres nas empresas, acima de tudo, no mesmo cargo. Vamos investigar

![Logo](Imagens\3.png) 

![Logo](Imagens\17.png) 

![Logo](Imagens\4.png) 

![Logo](Imagens\5.png) 

<p align="justify"> logo, podemos observar que existem cargos em que os homens costumam ganhar mais e também cargos em que as mulheres costumam ganhar mais. Como é possível ver, o aumento salarial das pessoas que possuem um maior nível de educação não é expressivo, como podemos ver abaixo

![Logo](Imagens\6.png) 

é notável que as pessoas que possuem mestrado (4) são as menos remuneradas na empresa, em média. É possível observar que o salário também não aumenta conforme o funcionario passa mais tempo na empresa, mesmo as que possuem performance acima da média

![Logo](Imagens\7.png)
![Logo](Imagens\8.png)
![Logo](Imagens\9.png)

por fim, vamos mostrar a correlação de Spearman entre as variáveis do problema

![Logo](Imagens\10.png)
### Entendendo os motivos da insatisfação dos funcionários

<p align="justify"> Vamos agora entender o motivo da insatisfação dos funcionários. Para isso, faremos uso de alguns classificadores que a empresa costuma medir algumas coisas como: satisfação com o emprego, satisfação com o ambiente (físico) de trabalho, balanço entre vida pessoal e o trabalho e a performance.

![Logo](Imagens\11.png)
![Logo](Imagens\16.png)

<p align="justify"> podemos ver que, pelo menos, entre 27,1% e 32,1% estão com um baixo balanço entre vida pessoal e o trabalho, independente da satisfação com o emprego. Isso se acentua nas pessoas que possuem maior satisfação no emprego. Além disso, é notório que pelo menos 37,2% dos funcionários não estão satisfeitos com o ambiente (físico) de trabalho.

<p align="justify"> Precisamos também entender diretamente as pessoas que saíram da empresa. Esses dados podem nos fornecer insights valiosos pois estamos falando diretamente com as pessoas que fizeram o que estamos evitando que aconteça novamente

![Logo](Imagens\12.png)
![Logo](Imagens\13.png)
![Logo](Imagens\14.png)
![Logo](Imagens\15.png)

<p align="justify"> Aqui nós temos um problema sério: das pessoas que saíram, aproximadamente metade não estavam muito satisfeitas com o trabalho e com o ambiente de trabalho. Além disso, aproximadamente 33% das pessoas que saíram da empresa não estavam envolvidas com o trabalho e 82.7% mostraram performance inferior.

<p align="justify"> Estamos trabalhando com dados de uma empresa em que um grande número de pessoas pede demissão e nosso objetivo inicialmente é descobrir as razões, dando insights baseados em análise de dados e estatística. É primordial o entendimento dos dados para que possamos tomar decisões a respeito, antes de fazer quaisquer providências para melhorar esse aspecto da empresa. A instituição é composta em sua maioria por homens e a idade que prevalece entre os funcionários é a média idade (entre 30 e 40 anos). A média salarial entre homens e mulheres é aproximadamente a mesma (com a dos homens sendo um pouco maior), além disso, em porcentagem, mais homem deixam a empresa que mulheres (diferença menor que 2%). </p>

<p align="justify">> A empresa possui três departamentos: Human Resources, Sales e Research and Development, que são do menor para o maior, em termos de número de funcionários. Para os homens, a média salarial aumenta conforme o nível da educação também aumenta, mas decai bruscamente quando o homem possui doutorado. Já nas mulheres, acontece uma queda nas que possuem mestrado e um pico nas que possuem doutorado. Observando a média salarial das mulheres com mestrado e que deixaram a empresa, podemos notar que o salário é 10% menor que o dos homens, além de ser 11% menor que a média das mulheres na empresa. Isso pode indicar que as mulheres com mestrado estão deixando a empresa pela falta de valorização, visto que estão recebendo abaixo da média. </p>

<p align="justify"> Uma boa parte dos funcionários possui uma relação de mediana para boa com o trabalho. Observamos que mais da metade possui um bom envolvimento, bem como possuem um considerável balanço entre a vida e o trabalho. Não podemos ignorar que entre 25 e 30% dos funcionários não possuem um bom balanço na vida pessoal e com o trabalho e, essa mesma porcentagem, possuem um baixo envolvimento com o trabalho (falo das categorias 1 e 2), coisas que estão diretamente relacionadas. Além disso, entre 35 e 45% dos funcionários não estão tão satisfeitos com o ambiente de trabalho, o que é quase metade. Novas medidas devem ser tomadas de forma a deixar o ambiente melhor para os trabalhadores.

<p align="justify"> Além disso, das pessoas que saíram, 48% não estavam satisfeitas com o ambiente de trabalho 47,12% não gostavam do trabalho em si e 33% admitiram não estar envolvidas com o trabalho, sendo que 82.7% teve uma baixa performance. Está claro que precisamos focar na valorização dos profissionais, é necessário um aumento de salário para os profissionais mais bem qualificados, uma vez que a média salarial quase não aumenta com a qualificação. A falta de valorização profissional faz com que na primeira oportunidade, ele saíra da empresa em busca de algo melhor. Além disso, precisamos tornar o ambiente de trabalho mais propício para trabalhar, 48% das pessoas que saíram indicaram que não estavam gostando do ambiente de trabalho, o que é praticamente metade.

Para resolver o problema, podemos inserir algumas novas coisas ao ambiente de trabalho. Dentre elas:

1- Podemos oferecer um desenvolvimento profissional, oferecendo workshops e mais treinamentos,

2- Uma vez que as pessoas demoram em média, mais tempo com o mesmo gestor que para ser promovida, uma estratégia saudável que pode ser implementada é a implantação de uma Comunicação Transparente, onde os funcionários podem se sentir confortáveis em dar feedbacks e expor suas preocupações,

3- Promover um maior equilíbrio entre a vida profissional e pessoal: oferecer mais trabalhos remotos e tornar o ambiente físico de trabalho mais confortável e acolhedor, com espaços para descanso e áreas verdes e ventiladas.

4- Promover mais eventos e atividades sociais ligadas a empresa, como Happy Hours e confraternizações.

# Modelo de Machine Learning

<p align="justify"> Vamos agora falar de uma parte importante e um mais técnica. Como estamos lidando com um modelo de classificação (o nosso objetivo é prever a variável Attrition, isto é, se a pessoa se demitiu ou não) faremos uso de um modelo, o RandomForest com tunagem de parâmetros. Além disso, fizemos uso do IsolationForest para remoção dos Outliers.

![Logo](Imagens\20.png)
<p align="justify"> Dividiremos nosso dataset em treino, validação e teste, dessa forma conseguimos um bom treino, um conjunto de dados separado para validar se aqueles dados estão sendo bem treinados e não só "viciados" no padrão de dados em que treinaram e, por fim, dados para que testem a eficácia do modelo. Essa divisão foi feita de forma que 60% dos dados serão destinados ao treino, 20% validação e 20% de treino.

![Logo](Imagens\18.png)
<p align="justify"> Como estamos lidando com dados desbalanceados (uma quantidade muito maior de pessoas não saíram da empresa com relação as que saíram) precisamos calcular os pesos referentes a esses valores, pois assim, fica mais difícil do modelo se "viciar" em classificar uma pessoa aleatória sempre como "não"
![Logo](Imagens\19.png)

<p align="justify"> agora, precisamos realizar as transformações nas variáveis numéricas e nas categóricas. Nas numéricas, aplicaremos SimpleImputer, para preencher dados vazios, StandardScaler para a padronização e normalização dos dados e o IsolationForest. Enquanto nas categóricas, o TargetEncoder, para separar as classes categóricas em 0 e 1 de maneira inteligente e também o SimpleImputer.

![Logo](Imagens\22.png)

<p align="justify"> e com isso terminamos o pré-processamento, que deve ser feito sempre depois da divisão em treino e teste. Afinal, não queremos "contaminar" os nossos dados de teste com informações dos dados de treino.

![Logo](Imagens\23.png)

<p align="justify"> No nosso modelo de Machine Learning, vamos tunar os parâmetros fazendo uso da Bayesian Search. Além disso, faremos uso da Cross Validation, para evitar os overfitting. Obtemos que os valores ótimos do parâmetro são: max_depth=20 e n_estimators=150.

<p align="justify"> Podemos agora brincar um pouco com o threshold do algoritmo de seleção. Ele atualmente funciona assim: calcula-se a probabilidade de determinada pessoa, se ela for maior que 0.5 será classificado com 1 e se for menor, como 0. Podemos mexer nesse valor 0.5 para cima ou para baixo. Para entender o melhor valor, que maximizará o desempenho do nosso modelo, podemos fazer o seguinte estudo

![Logo](Imagens\24.png)

<p align="justify"> fixando em 0,4 obtemos a seguinte matriz de confusão alida a curva ROC AUC

![Logo](Imagens\25.png)

![Logo](Imagens\26.png)

<p align="justify"> analisando os resultados, dos 882 funcionários: 741 não sairão e nosso modelo conseguiu prever que não sairão, 120 pessoas sairão e nosso modelo também conseguiu prever isso, 21 pessoas sairão e nosso modelo não conseguiu prever. Por fim, 0 pessoas não sairão e nosso modelo conseguiu prever. O resultado disso é uma curva ROC com área 0,98, esse número reflete na facilidade do nosso modelo em classificar pessoas que sairão como "Yes" e pessoas que não sairão como "No".

# TradeOff

<p align="justify"> Segundo a conclusão da nossa análise exploratória de dados, podemos aliar os dados do nosso modelo preditivo (Bayesian Search) para tentar buscar soluções visando melhorar as condições de trabalho e evitar demissões. Ressaltando alguns dados, fica claro que devemos investir em melhor condições de trabalho para que os funcionários consigam trabalhar. Dentre isso, oferecer uma melhor estrutura do ambiente de trabalho. Essa mudança na estrutura exigirá reformas e então mais gastos, mas o que se deve focar é em evitar a saída dos atuais funcionários e além, dos que ainda não entraram. Algumas pesquisas indicam que o custo de contratação de um funcionário está entre 1.5 e 2 vezes o salário do funcionário. Isso pois temos diversos fatos para levar em consideração, como custo do processo seletivo, recrutamento e treinamento. Logo, considerando o salário médio dos funcionários da empresa, podemos colocar que o custo sairia em torno de 90000 (na moeda local).

<p align="justify"> Vamos propor que o um curso de idiomas na escolha do funcionário custa 4000 da moeda local. Segundo nosso modelo, precisaremos comprar 882 (número de funcionários no dataset de teste) desses cursos. Será que é suficiente para evitar perdas na empresa? Bom, o balanço da empresa nesse processo é:

    CUSTO*QUANTIDADE DE FUNCIONÁRIOS - CUSTO DE RECONTRATAÇÃO*FUNCIONÁRIOS QUE SAIRÃO
no nosso caso:

            CUSTO*882 - 90000*141 (120 confirmados e 21 que o modelo não detectou)

que significa que teremos que investir aproximadamente 14387,7 por funcionário para garantirmos que não teremos prejuízo.

![Logo](Imagens\27.png)

logo, utilizaremos um montante de 12689951,4 na moeda local (771.750 reais).

Com o montante visto acima, conseguimos:

- Realizar diversas reformas na estrutura da empresa, de forma que o ambiente fique mais agradável de se trabalhar;
- Promover eventos e atividades de integração: Promova eventos e atividades de integração entre os funcionários, como happy hours, festas temáticas, campeonatos esportivos, voluntariado corporativo, entre outros;
- Fazer algumas viagens comemorativas na empresa;
- Considerar oferecer benefícios extras aos funcionários, como vales-alimentação, vales-refeição, plano de saúde subsidiado, auxílio-creche, vale-cultura, entre outros. Esses benefícios podem aumentar a satisfação e o engajamento dos colaboradores;
- Promover programas de reconhecimento e incentivo: Implementar programas de reconhecimento e incentivo, como premiações, reconhecimento público de desempenho excepcional, bônus por metas alcançadas, entre outros.

<p align="justify"> Ao implementar essas iniciativas, é importante garantir que elas estejam alinhadas com a cultura organizacional e as necessidades específicas dos funcionários. Além disso, é fundamental monitorar e avaliar regularmente o impacto dessas iniciativas na satisfação dos funcionários e nos resultados do negócio.
