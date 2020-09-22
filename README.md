# Machine learning pokemon

[Dataset](https://www.kaggle.com/rounakbanik/pokemon)


Esse conjunto tem 802 pokemons de 7 gerações e todas as informações foram extraidas do [site](http://serebii.net/)

Usei um algoritimo de Machine Learning  para definir se o Pokemon é lendário ou não com base em algumas features, como por exemplo 'Taxa de captura','passos pra chocar ovo','Felicidade', conseguindo um resultado excelente

Verdadeiros positivos e verdadeiros negativos, foram muito superiores em quantidades em relação aos falsos negativos e falsos positivos encontrados, várias vezes que rodei o algoritimo a precisão foi perfeita, mas as vezes 1 ou 2 iam parar na área dos falsos então por convenção vamos falar que a matriz de confusão ficou assim:

Verdadeiros positivos:221

Verdadeiros negativos:18

Falsos negativos:1

Falsos positivios:1


                    precision   recall   f1-score   support

           0           1.00       1.00     1.00       222
           1           0.95      0.95     0.95        19

    accuracy                               0.99       241
    macro avg          0.97      0.97      0.97       241
    weighted avg       0.99      0.99      0.99       241




Obs : Accuracy não é algo muito interessante de se olhar pois temos o numero de pokemons não lendarios muito superiores em relação aos lendários e essa medida pega o todo exemplo:
Tenho um algoritimo que tem 99 pokemons não lendários e 1 lendário e a Accuracy dele é 99%, você deve pensar que é algo bom, mas você pode estar muito enganado, desses 1% que ele não acertou foi o único lendário existente, ou seja talvez seu algoritimo não esteja treinado para identificar lendários

Nesse código usei dois tipos diferentes de algoritimos, Random Forest e Decision Tree, para ver qual tinha a melhor performance, os dois tiveram ótimos resultados mas como esperado o Random Forest saiu na vitória, experimentei KNN mas o resultado foi inferior, mas teve uma perfomance melhor do que eu esperava.

No começo o dataframe tinha 41 colunas, sendo algumas que eu não via motivos para deixar já que eu sabia que não ia alterar em quase nada meu modelo e também a questão de perfomance,random forest é um algoritimo que requer bastante da sua máquina, se eu executasse com 41 colunas e 802 linhas, acho que explodiria.

Algo muito massa que aconteceu nesse dataframe é que não tinha muitas correlações fortes( a mais forte tinha 0,86 uma correlação forte positiva), mas mesmo assim se fosse olhar só por ela o acerto não seria tão bom,mas oque tinha era várias correlações não tão fortes mas que ajudaram a nossos algoritimos perfomar muito melhor, depois de plotar a minha árvore percebi que altura e peso não era uma parte da árvore, ou seja poderia remove-las sem problemas

Teste no Pikachu e no Mewtwo foram realizados, resultando nas respostas correta, outro fator que experimentei foi com pokemon semi lendários(Salamence), que são pokemons com atributos semelhantes dos lendários, mas que no final não são e mesmo assim o algoritimo se performou muito bem

Pokemon foi algo que eu sempre gostei, então nada melhor do que usar os conhecimentos em programação para algo útil, POKEMON!
