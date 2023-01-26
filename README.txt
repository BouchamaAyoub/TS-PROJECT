Réalisation d un modem de fréquence selon la recommandation V21 de 
           l'Union Internationale des Télécommunications (UIT)
**************************************************************************************************************************************************************************************************************************************	
Ecole : INP-ENSEEIHT							
Auteurs : Ayoub BOUCHAMA & Oussama ELGUERRAOUI				
Promotion : 2022/2023							
Groupe : F								
Partie : Code du projet, fonctions et exécution	
**************************************************************************************************************************************************************************************************************************************

***** Codes fournis *****

1/ ( modem_de_frequence.m ) :

*** Fonction ***

=>=>=>	Code matlab implémentant un modem de fréquence en utilisant les fréquences des porteuses F0 = 6000 et F1 = 2000, en créant un signal
	ce code consiste à créer le signal modulé en fréquence à partir du signal NRZ (Non Return to Zero). Ensuite, à partir d’un signal reçu altéré par un canal à bruit
	additif blanc et gaussien (AWGN), il faudra mettre en place le modem de réception permettant de démoduler le signal en utilisant le filtrage pour retrouver l’information binaire.

*** Execution ***

=>=>=>	Il suffit d'éxecuter le code avec le boutton 'Run' dans matlab pour visualiser le tracé de tout les étapes qu'a subit le siganl bruité pour finalement récupérer l'information binaire,
	ainsi vous pouvez bien varier la variable N qui représente la moitié de l'ordre du filtre moins 1 pour constater la variation du taux d'erreur et l'apparition d'un certain retard
	dans le siganl qu'on a géré grace à la méthode du zero-padding. (on peut meme adapter les frequences des porteuses aux normes V21 pour visualiser les differences)

2/ ( modem_V21.m )

*** Fonction ***

=>=>=>	Exploitation d'une nouvelle methode de demodulaton du signal qui consiste à calculer la différence entre les intégrale de chaque porteuse afin de les comparer et finalement 
	déterminer sur quelle fréquence la porteuse était modulée pour chaque bit.

*** Execution ***

=>=>=>	Il suffit d'éxecuter le code avec le boutton 'Run' dans matlab pour constater que le taux d'erreur est nulle ce qui nous assure la démodulation parfaite du signal.

3/ ( modem_phase_porteuse_V21.m )

*** Fonction ***

=>=>=>	Exploitation d'une methode de demodulation qui prend en compte l'erreur de phase contrairement à la méthode précédente.

*** Execution ***

=>=>=>	Il suffit d'éxecuter le code avec le boutton 'Run' dans matlab pour constater que le taux d'erreur est élevé en présence d'une phase aléatoire et en utilisant la methode de demodulation
	précédente, alors que l'erreur revient à 0 lors de l'utilisation de la methode ainsi implementé dans ce fichier.

4/ ( dirac1.m )

=>=>=> 	Fonction dirac fonctionnelle pour un signal d'entrée symétrique par rapport à 0 comme utilisé dans nos code.

5/ ( demoduler.m )

=>=>=> 	Fonction qui demodule un signal d'entrée selon les normes V21.

6/ ( reconstitution_image.m )

=>=>=>	Fonction pour reconstituer le signal démodulé.

7/ ( image_finale.m )

=>=>=> Reconstitution et affichage de l'image finale.

**************************************************************************************************************************************************************************************************************************************
