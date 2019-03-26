# Conversion de magnitudes
Ariane Ducellier  
13 janvier 2015  







# Comparaison des magnitudes de durée

## Analyse des données

Les magnitudes de durée sont fournies par l'observatoire de Trinidad, celui de Fort-de-France et plusieurs autres sources. Parmi les autres sources, nous comptons le nombre de magnitudes de durée fournies par chaque observatoire.


```
## mdsrc_autre
## BBL;  BIM BIM; BPA;  CAR CAR; CRM; DEG; DOG; FUNV MGG; MGH; MPR; MVM;  PAG 
##    2    2    1    1   12    1    1   58    2  114    2    1   87    6    9 
## PAG; RSPR TAG; ZAM; 
##   38 5236   18    4
```

Seul l'observatoire de Porto Rico (RSPR) semble avoir assez de données pour les comparer avec les données des deux autres observatoires. Nous n'allons donc conserver que celles-ci pour la suite de l'analyse.



Nous analysons brièvement la distribution des magnitudes de durée pour chacun des trois observatoires considérés (Figure 1).

![Distribution des magnitudes de durée](./analyse_files/figure-html/unnamed-chunk-6-1.png) 

- Observatoire de Trinidad


```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
##   0.500   2.600   3.000   2.961   3.400   7.300   27955
```

- Observatoire de Fort-de-France


```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
##    0.60    2.10    2.50    2.57    3.00    7.30   32544
```

- Observatoire de Porto Rico


```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
##    2.00    2.90    3.20    3.19    3.40    6.10   34797
```



Il y a 2939 données en commun entre l'observatoire de Trinidad et celui de Fort-de-France, 269 données en commun entre l'observatoire de Trinidad et celui de Porto Rico, et 95 données en commun entre l'observatoire de Fort-de-France et celui de Porto Rico.

## Régressions linéaires

Pour vérifier si les magnitudes de durée fournies par les différents observatoires sont cohérentes entre elles, nous effectuons des régressions linéaires de l'une par rapport à l'autre.

### Comparaison entre les magnitudes de durée fournies par Trinidad et Fort-de-France



La relation entre les deux magnitudes de durée est :

$M_{d, FDF}$ = 0.923(+- 0.027) $M_{d, TRN}$ + 0.053(+- 0.087)

0.8 < $M_{d, TRN}$ < 7.3

0.7 < $M_{d, FDF}$ < 7.3

$R^2$ = 0.698, $\sigma$ = 0.91, n = 2939

$R^2_{pred}$ = 0.677 (validation croisée), $R^2_{pred}$ = 0.678 (bootstrap)

La Figure 2 représente les magnitudes de durée fournies par l'observatoire de Fort-de-France en fonction des magnitudes de durée fournies par l'observatoire de Trinidad. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire, et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de durée fournies par l'observatoire de Trinidad et celles fournies par l'observatoire de Fort-de-France](./analyse_files/figure-html/unnamed-chunk-12-1.png) 

### Comparaison entre les magnitudes de durée fournies par Fort-de-France et Trinidad



La relation entre les deux magnitudes de durée est :

$M_{d, TRN}$ = 0.757(+- 0.022) $M_{d, FDF}$ + 0.914(+- 0.067)

0.7 < $M_{d, FDF}$ < 7.3

0.8 < $M_{d, TRN}$ < 7.3

$R^2$ = 0.698, $\sigma$ = 0.824, n = 2939

$R^2_{pred}$ = 0.662 (validation croisée), $R^2_{pred}$ = 0.681 (bootstrap)

La Figure 3 représente les magnitudes de durée fournies par l'observatoire de Trinidad en fonction des magnitudes de durée fournies par l'observatoire de Fort-de-France. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire, et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de durée fournies par l'observatoire de Fort-de-France et celles fournies par l'observatoire de Trinidad](./analyse_files/figure-html/unnamed-chunk-14-1.png) 

### Comparaison entre les magnitudes de durée fournies par Trinidad et Porto Rico



La relation entre les deux magnitudes de durée est :

$M_{d, RSPR}$ = 0.577(+- 0.052) $M_{d, TRN}$ + 1.791(+- 0.198)

2.1 < $M_{d, TRN}$ < 5.8

2.1 < $M_{d, RSPR}$ < 6.1

$R^2$ = 0.433, $\sigma$ = 0.466, n = 269

$R^2_{pred}$ = 0.411 (validation croisée), $R^2_{pred}$ = 0.443 (bootstrap)

La Figure 4 représente les magnitudes de durée fournies par l'observatoire de Porto Rico en fonction des magnitudes de durée fournies par l'observatoire de Trinidad. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire, et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de durée fournies par l'observatoire de Trinidad et celles fournies par l'observatoire de Porto Rico](./analyse_files/figure-html/unnamed-chunk-16-1.png) 

### Comparaison entre les magnitudes de durée fournies par Fort-de-France et Porto Rico



La relation entre les deux magnitudes de durée est :

$M_{d, RSPR}$ = 0.352(+- 0.088) $M_{d, FDF}$ + 2.659(+- 0.353)

2.4 < $M_{d, FDF}$ < 5.9

2.4 < $M_{d, RSPR}$ < 5.2

$R^2$ = 0.165, $\sigma$ = 0.483, n = 95

$R^2_{pred}$ = -0.272 (validation croisée), $R^2_{pred}$ = 0.127 (bootstrap)

La Figure 5 représente les magnitudes de durée fournies par l'observatoire de Porto Rico en fonction des magnitudes de durée fournies par l'observatoire de Fort-de-France. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire, et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de durée fournies par l'observatoire de Fort-de-France et celles fournies par l'observatoire de Porto Rico](./analyse_files/figure-html/unnamed-chunk-18-1.png) 

Les magnitudes de durée fournies par l'observatoire de Trinidad et celles fournies par l'observatoire de Fort-de-France sont relativement cohérentes entre elles. En revanche, les magnitudes de durée fournies par l'observatoire de Porto Rico sont significativement différentes de celles fournies par les deux autres observatoires.

# Comparaison des magnitudes de durée et des magnitudes de moment

## Analyse des données



Il y a 1548 données en commun entre la magnitude de moment et la magnitude de durée de l'observatoire de Trinidad, 77 données en commun entre la magnitude de moment et la magnitude de durée de l'observatoire de Fort-de-France, et 23 données en commun entre la magnitude de moment et la magnitude de durée de l'observatoire de Porto Rico

La relation entre magnitude de durée et magnitude de moment proposée par Drouet *et al.* (2011, équation 10) est :

$M_{W}$ = 1.01(+- 0.01) $M_{d}$ + 0.50(+- 0.03)

## Vérification du modèle de Drouet



Nous reprenons les données utilisées par Drouet *et al.* (2011, tableau 5) pour déterminer la relation entre la magnitude de durée (observatoire de Fort-de-France) et la magnitude de moment. Il y a 475 observations.

La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 0.815(+- 0.034) $M_{d}$ + 1.049(+- 0.097)

1.4 < $M_{d}$ < 6

2.3 < $M_{W}$ < 6.3

$R^2$ = 0.775, $\sigma$ = 0.395, n = 475

$R^2_{pred}$ = 0.748 (validation croisée), $R^2_{pred}$ = 0.77 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant les données du tableau 5, on obtient un coefficient de détermination égal à :

$R^2$ = 0.73

La Figure 6 représente les magnitudes de moment en fonction des magnitudes de durée fournies par l'observatoire de Fort-de-France issues du tableau 5 de Drouet *et al.* (2011). La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du tableau 5, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par l'observatoire de Fort-de-France](./analyse_files/figure-html/unnamed-chunk-21-1.png) 

On ne retrouve pas le même modèle que Drouet *et al.* (2011). En effet, la pente de la régression est un peu plus faible. Cela peut être dû au fait que Drouet *et al.* (2011) ne précisent pas sur quel intervalle de magnitudes leur régression a été effectuée. Cependant, le modèle de Drouet *et al.* (2011) est assez bon, même s'il ne permet pas de modéliser les données aussi bien que la régression effectuée dans cette étude.

## Régressions linéaires

### Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par Trinidad

#### Avec les données de Funvisis



La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 1.02(+- 0.035) $M_{d, TRN}$ + -0.251(+- 0.119)

1.6 < $M_{d, TRN}$ < 7.3

1.9 < $M_{W}$ < 7.7

$R^2$ = 0.707, $\sigma$ = 0.789, n = 1548

$R^2_{pred}$ = 0.707 (validation croisée), $R^2_{pred}$ = 0.728 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = -0.342

La Figure 7 représente les magnitudes de moment en fonction des magnitudes de durée fournies par l'observatoire de Trinidad. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par l'observatoire de Trinidad](./analyse_files/figure-html/unnamed-chunk-23-1.png) 

#### Sans les données de Funvisis

Si on enlève les magnitudes de moment fournies par Funvisis, il n'y a plus que 107 données en commun entre la magnitude de moment et la magnitude de durée de l'observatoire de Trinidad.



La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 0.983(+- 0.062) $M_{d, TRN}$ + 0.296(+- 0.298)

3.6 < $M_{d, TRN}$ < 7.3

3.5 < $M_{W}$ < 7.7

$R^2$ = 0.756, $\sigma$ = 0.395, n = 107

$R^2_{pred}$ = 0.526 (validation croisée), $R^2_{pred}$ = 0.699 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.528

La Figure 8 représente les magnitudes de moment en fonction des magnitudes de durée fournies par l'observatoire de Trinidad. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par l'observatoire de Trinidad (sans les données de Funvisis)](./analyse_files/figure-html/unnamed-chunk-25-1.png) 

### Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par Fort-de-France

#### Avec les données de Funvisis



La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 1.05(+- 0.098) $M_{d, FDF}$ + -0.414(+- 0.43)

2.5 < $M_{d, FDF}$ < 7.3

2.8 < $M_{W}$ < 7.7

$R^2$ = 0.63, $\sigma$ = 0.602, n = 77

$R^2_{pred}$ = -0.327 (validation croisée), $R^2_{pred}$ = 0.517 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = -0.011

La Figure 9 représente les magnitudes de moment en fonction des magnitudes de durée fournies par l'observatoire de Fort-de-France. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par l'observatoire de Fort-de-France](./analyse_files/figure-html/unnamed-chunk-27-1.png) 

#### Sans les données de Funvisis

Si on enlève les magnitudes de moment fournies par Funvisis, il n'y a plus que 23 données en commun entre la magnitude de moment et la magnitude de durée de l'observatoire de Fort-de-France.



La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 0.842(+- 0.095) $M_{d, FDF}$ + 1.185(+- 0.467)

3.7 < $M_{d, FDF}$ < 7.3

4 < $M_{W}$ < 7.7

$R^2$ = 0.805, $\sigma$ = 0.334, n = 23

$R^2_{pred}$ = -3.707 (validation croisée), $R^2_{pred}$ = 0.382 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.739

La Figure 10 représente les magnitudes de moment en fonction des magnitudes de durée fournies par l'observatoire de Fort-de-France. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par l'observatoire de Fort-de-France (sans les données de Funvisis)](./analyse_files/figure-html/unnamed-chunk-29-1.png) 

#### Avec les données de Drouet *et al.* (2011) et sans les données de Funvisis



La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 0.868(+- 0.025) $M_{d}$ + 0.911(+- 0.075)

1.4 < $M_{d}$ < 7.3

2.3 < $M_{W}$ < 7.7

$R^2$ = 0.862, $\sigma$ = 0.394, n = 498

$R^2_{pred}$ = 0.828 (validation croisée), $R^2_{pred}$ = 0.867 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant l'ensembe des données du tableau 5 de Drouet *et al.* (2011) et du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.839

La Figure 11 représente les magnitudes de moment en fonction de l'ensemble des magnitudes de durée issues du tableau 5 et des magnitudes de durée issues du catalogue CDSA fournies par l'observatoire de Fort-de-France. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du tableau 5 et du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et l'ensemble des magnitudes de durée fournies par l'observatoire de Fort-de-France](./analyse_files/figure-html/unnamed-chunk-31-1.png) 

### Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par Porto Rico

#### Avec les données de Funvisis



La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 0.714(+- 0.129) $M_{d, RSPR}$ + 1.53(+- 0.631)

4.1 < $M_{d, RSPR}$ < 6.1

4.1 < $M_{W}$ < 6.1

$R^2$ = 0.605, $\sigma$ = 0.309, n = 23

$R^2_{pred}$ = -0.249 (validation croisée), $R^2_{pred}$ = 0.279 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = -0.297

La Figure 12 représente les magnitudes de moment en fonction des magnitudes de durée fournies par l'observatoire de Porto Rico. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par l'observatoire de Porto Rico](./analyse_files/figure-html/unnamed-chunk-33-1.png) 

#### Sans les données de Funvisis

Si on enlève les magnitudes de moment fournies par Funvisis, il n'y a plus que 22 données en commun entre la magnitude de moment et la magnitude de durée de l'observatoire de Porto Rico.



La relation entre la magnitude de moment et la magnitude de durée est :

$M_{W}$ = 0.684(+- 0.118) $M_{d, RSPR}$ + 1.705(+- 0.58)

4.1 < $M_{d, RSPR}$ < 6.1

4.1 < $M_{W}$ < 6.1

$R^2$ = 0.637, $\sigma$ = 0.282, n = 22

$R^2_{pred}$ = -1.143 (validation croisée), $R^2_{pred}$ = 0.418 (bootstrap)

En utilisant la relation proposée par Drouet *et al.* (2011) pour calculer la magnitude de moment à partir de la magnitude de durée en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = -0.293

La Figure 13 représente les magnitudes de moment en fonction des magnitudes de durée fournies par l'observatoire de Porto Rico. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Drouet *et al.* (2011), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes de durée fournies par l'observatoire de Porto Rico (sans les données de Funvisis)](./analyse_files/figure-html/unnamed-chunk-35-1.png) 

Un modèle linéaire permet assez bien d'expliquer la relation entre magnitudes de moment et magnitudes de durée. Pour les données fournies par les observatoires de Trinidad et de Fort-de-France, le coefficient de pente obtenu à l'aide des données du catalogue CDSA est proche de celui du modèle de Drouet *et al.* (2011), mais l'intercept est très différent. Cependant, pour les données fournies par l'observatoire de Porto Rico, le coefficient de pente est différent du modèle de Drouet *et al.* (2011). Si on effectue les régressions linéaires en ne tenant pas compte des magnitudes de moment fournies par Funvisis, le modèle linéaire obtenu à l'aide des données du catalogue CDSA se rapproche du modèle de Drouet *et al.* (2011) pour les données fournies par l'observatoire de Trinidad. En revanche, pour les données fournies par les observatoires de Fort-de-France et de Porto Rico, le coefficient de pente n'est plus du tout correct. Cela peut être du au petit nombre de données disponibles pour ces observatoires.

# Comparaison des magnitudes d'ondes de surface et des magnitudes de moment

## Analyse des données



Il y a 253 données en commun entre la magnitude de moment et la magnitude d'ondes de surface. Pour les magnitudes d'ondes de surface comprises entre 3 et 6.1, il y a 227 données en commun. Pour les magnitudes d'ondes de surface inférieures à 6.47, il y a 247 données en commun.

La relation entre magnitude d'ondes de surface et magnitude de moment proposée par Scordilis (2006, équation 14) est :

$M_{W}$ = 0.67(+- 0.005) $M_{S}$ + 2.07(+- 0.03)

3 < $M_{S}$ < 6.1

$R^2$ = 0.77, $\sigma$ = 0.17, n = 23921

La relation entre magnitude d'ondes de surface et magnitude de moment proposée par Di Giacomo *et al.* (2014, équation 1) est :

$M_{W}$ = 0.67 $M_{S}$ + 2.13

$M_{S}$ < 6.47

pour le modèle linéaire et :

$M_{W}$ = exp (0.233 $M_{S}$ - 0.222) + 2.863

pour le modèle exponentiel.

## Régressions linéaires

### Avec les données de Funvisis



La relation entre la magnitude de moment et la magnitude d'ondes de surface est :

$M_{W}$ = 0.754(+- 0.035) $M_{S}$ + 1.64(+- 0.149)

2.3 < $M_{S}$ < 6.8

3 < $M_{W}$ < 7.7

$R^2$ = 0.73, $\sigma$ = 0.52, n = 253

$R^2_{pred}$ = 0.667 (validation croisée), $R^2_{pred}$ = 0.69 (bootstrap)

En utilisant la relation proposée par Scordilis (2006, équation 14) pour calculer la magnitude de moment à partir de la magnitude d'ondes de surface en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.629

En utilisant le modèle linéaire proposé par Di Giacomo *et al.* (2014, équation 1) pour calculer la magnitude de moment à partir de la magnitude d'ondes de surface en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.645

En utilisant le modèle exponentiel proposé par Di Giacomo *et al.* (2014, équation 1) pour calculer la magnitude de moment à partir de la magnitude d'ondes de surface en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.575

La Figure 14 représente les magnitudes de moment en fonction des magnitudes d'ondes de surface. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue, la ligne bleue représente le modèle linéaire proposé par Scordilis (2006), la ligne verte représente le modèle linéaire proposé par Di Giacomo *et al.* (2014), la ligne jaune représente le modèle exponentiel proposé par Di Giacomo *et al.* (2014), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes d'ondes de surface](./analyse_files/figure-html/unnamed-chunk-38-1.png) 

### Sans les données de Funvisis

Si on enlève les magnitudes de moment fournies par Funvisis, il y a plus que 159 données en commun entre la magnitude de moment et la magnitude d'ondes de surface. Pour les magnitudes d'ondes de surface comprises entre 3 et 6.1, il y a 145 données en commun. Pour les magnitudes d'ondes de surface inférieures à 6.47, il y a 153 données en commun.



La relation entre la magnitude de moment et la magnitude d'ondes de surface est :

$M_{W}$ = 0.633(+- 0.028) $M_{S}$ + 2.355(+- 0.13)

2.4 < $M_{S}$ < 6.8

3.8 < $M_{W}$ < 7.7

$R^2$ = 0.824, $\sigma$ = 0.313, n = 159

$R^2_{pred}$ = 0.792 (validation croisée), $R^2_{pred}$ = 0.773 (bootstrap)

En utilisant la relation proposée par Scordilis (2006, équation 14) pour calculer la magnitude de moment à partir de la magnitude d'ondes de surface en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.687

En utilisant le modèle linéaire proposé par Di Giacomo *et al.* (2014, équation 1) pour calculer la magnitude de moment à partir de la magnitude d'ondes de surface en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.767

En utilisant le modèle exponentiel proposé par Di Giacomo *et al.* (2014, équation 1) pour calculer la magnitude de moment à partir de la magnitude d'ondes de surface en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.818

La Figure 15 représente les magnitudes de moment en fonction des magnitudes d'ondes de surface. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue, la ligne bleue représente le modèle linéaire proposé par Scordilis (2006), la ligne verte représente le modèle linéaire proposé par Di Giacomo *et al.* (2014), la ligne jaune représente le modèle exponentiel proposé par Di Giacomo *et al.* (2014), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes d'ondes de surface (sans les données de Funvisis)](./analyse_files/figure-html/unnamed-chunk-40-1.png) 

Le modèle de Scordilis (2006) et le modèle linéaire de Di Giacome *et al.* (2014) appliqués sur les données du catalogue CDSA expliquent un peu moins bien la relation entre magnitudes de moment et magnitudes d'ondes de surface que la régression linéaire effectuée dans cette étude, mais restent assez bons. La régression effectuée avec les données du catalogue CDSA donne un résultat un peu moins bon que la régression effectuée par Scordilis (2006) avec les données de différents catalogues internationaux. En revanche, le modèle exponentiel de Di Giacomo *et al.* (2014) explique moins bien la relation entre magnitudes de moment et magnitudes d'ondes de surface que la régression linéaire effectuée dans cette étude. Si on effectue les régressions linéaires en ne tenant pas compte des magnitudes de moment fournies par Funvisis, tous les modèles de régression sont meilleurs, en particulier le modèle exponentiel de Di Giacomo *et al* (2014). Cependant, la régression linéaire effectuée dans cette étude explique toujours mieux la relation entre magnitudes de moment et magnitudes d'ondes de surface que les modèles proposés par Scordilis (2006) et Di Giacomo *et al.* (2014).

# Comparaison des magnitudes d'ondes de volume et des magnitudes de moment

## Analyse des données



Il y a 370 données en commun entre la magnitude de moment et la magnitude d'ondes de volume. Pour les magnitudes d'ondes de volume comprises entre 3.5 et 6.2, il y a 353 données en commun.

La relation entre magnitude d'ondes de volume et magnitude de moment proposée par Scordilis (2006, équation 22) est :

$M_{W}$ = 0.85(+- 0.04) $m_{b}$ + 1.03(+- 0.23)

3.5 < $m_{b}$ < 6.2

$R^2$ = 0.53, $\sigma$ = 0.29, n = 39784

La relation entre magnitude d'ondes de volume et magnitude de moment proposée par Di Giacomo *et al.* (2014, équation 2) est :

$M_{W}$ = 1.38 $m_{b}$ - 1.79

pour le modèle linéaire et :

$M_{W}$ = exp (0.859 $m_{b}$ - 4.664) + 4.555

pour le modèle exponentiel.

## Régressions linéaires

### Avec les données de Funvisis



La relation entre la magnitude de moment et la magnitude d'ondes de volume est :

$M_{W}$ = 1.113(+- 0.036) $m_{b}$ + -0.499(+- 0.165)

3.1 < $m_{b}$ < 6.8

2.7 < $M_{W}$ < 7.7

$R^2$ = 0.818, $\sigma$ = 0.511, n = 370

$R^2_{pred}$ = 0.774 (validation croisée), $R^2_{pred}$ = 0.777 (bootstrap)

En utilisant la relation proposée par Scordilis (2006, équation 22) pour calculer la magnitude de moment à partir de la magnitude de volume en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.593

En utilisant le modèle linéaire proposé par Di Giacomo *et al.* (2014, équation 2) pour calculer la magnitude de moment à partir de la magnitude d'ondes de volume en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.76

En utilisant le modèle exponentiel proposé par Di Giacomo *et al.* (2014, équation 2) pour calculer la magnitude de moment à partir de la magnitude d'ondes de volume en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.109

La Figure 16 représente les magnitudes de moment en fonction des magnitudes d'ondes de volume. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Scordilis (2006), la ligne verte représente le modèle linéaire proposé par Di Giacomo *et al*. (2014), la ligne jaune représente le modèle exponentiel proposé par Di Giacomo *et al.* (2014), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes d'ondes de volume](./analyse_files/figure-html/unnamed-chunk-43-1.png) 

### Sans les données de Funvisis

Si on enlève les magnitudes de moment fournies par Funvisis, il y a plus que 187 données en commun entre la magnitude de moment et la magnitude d'ondes de volume. Pour les magnitudes d'ondes de volume entre 3.5 et 6.2, il y a 184 données en commun.



La relation entre la magnitude de moment et la magnitude d'ondes de volume est :

$M_{W}$ = 0.97(+- 0.042) $m_{b}$ + 0.331(+- 0.213)

3.5 < $m_{b}$ < 6.8

3.5 < $M_{W}$ < 7.7

$R^2$ = 0.823, $\sigma$ = 0.346, n = 187

$R^2_{pred}$ = 0.77 (validation croisée), $R^2_{pred}$ = 0.823 (bootstrap)

En utilisant la relation proposée par Scordilis (2006, équation 22) pour calculer la magnitude de moment à partir de la magnitude de volume en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.765

En utilisant le modèle linéaire proposé par Di Giacomo *et al.* (2014, équation 2) pour calculer la magnitude de moment à partir de la magnitude d'ondes de volume en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.663

En utilisant le modèle exponentiel proposé par Di Giacomo *et al.* (2014, équation 2) pour calculer la magnitude de moment à partir de la magnitude d'ondes de volume en utilisant les données du catalogue CDSA, on obtient un coefficient de détermination égal à :

$R^2$ = 0.65

La Figure 17 représente les magnitudes de moment en fonction des magnitudes d'ondes de volume. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, la ligne bleue représente le modèle linéaire proposé par Scordilis (2006), la ligne verte représente le modèle linéaire proposé par Di Giacomo *et al*. (2014), la ligne jaune représente le modèle exponentiel proposé par Di Giacomo *et al.* (2014), et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes de moment et les magnitudes d'ondes de volume (sans les données de Funvisis)](./analyse_files/figure-html/unnamed-chunk-45-1.png) 

Le modèle de Scordilis (2006) appliqué sur les données du catalogue CDSA explique moins bien la relation entre magnitudes de moment et magnitudes d'ondes de volume que la régression linéaire effectuée dans cette étude. Cependant, le modèle de Scordilis (2006) appliqué aux données du catalogue CDSA donne un résultat un peu meilleur que la régression effectuée par Scordilis (2006) avec les données de différents catalogues internationaux. Le modèle linéaire de Di Giacomo *et al.* (2014) explique un peu moins bien la relation entre magnitudes de moment et magnitudes d'ondes de volume que la régression linéaire effectuée dans cette étude, mais il est meilleur que le modèle proposé par Scordilis (2006). Enfin, le modèle exponentiel de Di Giacomo *et al.* (2014) donne de très mauvais résultats. Si on effectue les régressions linéaires en ne tenant pas compte des magnitudes de moment fournies par Funvisis, tous les modèles de régression sont meilleurs, à l'exception du modèle linéaire de Di Giacomo *et al.* (2014). En particulier le modèle exponentiel de Di Giacomo *et al* (2014) est bien meilleur. Il reste cependant moins bon que la régression linéaire effectuée dans cette étude.

# Comparaison des magnitudes de durée et des magnitudes d'ondes de volume

## Analyse des données



Il y a 1032 données en commun entre la magnitude d'ondes de volume et la magnitude de durée de l'observatoire de Trinidad, 479 données en commun entre la magnitude d'ondes de volume et la magnitude de durée de l'observatoire de Fort-de-France, et 224 données en commun entre la magnitude d'ondes de volume et la magnitude de durée de l'observatoire de Porto Rico.

## Régressions linéaires

### Comparaison entre les magnitudes d'ondes de volume et les magnitudes de durée fournies par Trinidad



La relation entre la magnitude d'ondes de volume et la magnitude de durée est :

$m_{b}$ = 0.827(+- 0.042) $M_{d, TRN}$ + 0.676(+- 0.17)

2.8 < $M_{d, TRN}$ < 7.3

2.8 < $m_{b}$ < 6.8

$R^2$ = 0.592, $\sigma$ = 0.64, n = 1032

$R^2_{pred}$ = 0.504 (validation croisée), $R^2_{pred}$ = 0.549 (bootstrap)

La Figure 18 représente les magnitudes d'ondes de volume en fonction des magnitudes de durée fournies par l'observatoire de Trinidad. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes d'ondes de volume et les magnitudes de durée fournies par l'observatoire de Trinidad](./analyse_files/figure-html/unnamed-chunk-48-1.png) 

### Comparaison entre les magnitudes d'ondes de volume et les magnitudes de durée fournies par Fort-de-France



La relation entre la magnitude d'ondes de volume et la magnitude de durée est :

$m_{b}$ = 0.494(+- 0.039) $M_{d, FDF}$ + 2.07(+- 0.154)

2.5 < $M_{d, FDF}$ < 7.3

3.1 < $m_{b}$ < 6.8

$R^2$ = 0.4, $\sigma$ = 0.517, n = 479

$R^2_{pred}$ = 0.304 (validation croisée), $R^2_{pred}$ = 0.352 (bootstrap)

La Figure 19 représente les magnitudes d'ondes de volume en fonction des magnitudes de durée fournies par l'observatoire de Fort-de-France. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes d'ondes de volume et les magnitudes de durée fournies par l'observatoire de Fort-de-France](./analyse_files/figure-html/unnamed-chunk-50-1.png) 

### Comparaison entre les magnitudes d'ondes de volume et les magnitudes de durée fournies par Porto Rico



La relation entre la magnitude d'ondes de volume et la magnitude de durée est :

$m_{b}$ = 0.807(+- 0.069) $M_{d, RSPR}$ + 0.645(+- 0.288)

2.9 < $M_{d, RSPR}$ < 6.1

3.2 < $m_{b}$ < 5.9

$R^2$ = 0.534, $\sigma$ = 0.442, n = 224

$R^2_{pred}$ = 0.405 (validation croisée), $R^2_{pred}$ = 0.483 (bootstrap)

La Figure 20 représente les magnitudes d'ondes de volume en fonction des magnitudes de durée fournies par l'observatoire de Porto Rico. La taille et la couleur des cercles sont proportionnelles au nombre d'observations. La ligne rouge représente le modèle linéaire issu du catalogue CDSA, et la ligne en tirets gris représente la première diagonale.

![Comparaison entre les magnitudes d'ondes de volume et les magnitudes de durée fournies par l'observatoire de Porto Rico](./analyse_files/figure-html/unnamed-chunk-52-1.png) 

Les modèles linéaires ne permettent pas très bien d'expliquer la relation entre magnitudes d'ondes de volume et magnitudes de durée, en particulier pour les magnitudes de durée fournies par l'observatoire de Fort-de-France. De plus, le modèle de régression obtenu à l'aide des données fournies par l'observatoire de Fort-de-France est très différent des deux modèles obtenus à l'aide des données fournies par les deux autres observatoires. En revanche, le modèle obtenu à l'aide des données fournies par l'observatoire de Trinidad est proche du modèle obtenu à l'aide des données fournies par l'observatoire de Porto Rico.

# Bibliographie

Di Giacomo D., Bondar I., Storchak D.A., Engdahl E.R., Bormann P., Harris J. (2014) - ISC-GEM: Global instrumental earthquake catalogue (1900-2009), III. Re-computed $M_{S}$ and $m_{b}$, prox $M_{W}$, final magnitude composition and completeness assessment. *Physics of the Earth and Planetary Interiors* in press

Drouet S., Bouin M.-P., Cotton F. (2011) - New moment magnitude scale, evidence of stress drop magnitude scaling and stochastic ground motion model for the French West Indies. *Geophysical Journal International* 187:1625-1644

Scordilis E.M. (2006) - Empirical global relations converting $M_{S}$ and $m_{b}$ to moment magnitude. *Journal of Seismology* 10:225-236

NB: To change the colors, look at http://sape.inf.usi.ch/quick-reference/ggplot2/colour
