a) ¿Cuál es la función de los componentes y servicios? (i.e. cuándo se debe 
utilizar cada uno de ellos)

Els components defineixen les vistes, que són conjunts d'elements en la pantalla que Angular pot triar i modificar segons la lògica i les dades del programa. Els components utilitzen serveis, que proporcionen una funcionalitat específica no relacionada directament amb les visualitzacions.

Quan una part d'html es repeteix amb una funcionalitat similar, sempre és millor agrupar-la en un Component, on aquest es pot cridar sempre que es requereixi la mateixa funcionalitat. En canvi, els Serveis, són classes senzilles amb mètodes i atributs, són unitats centrals per a algunes funcions comunes en tota l'aplicació. 

b) ¿Qué es la <<inyección de dependencias>>? ¿Para qué sirve el decorador @Injectable?

El decorador @Injectable, actualment, no te cap valor per a nosaltres, però és un decorador recomanat sempre que es treballi amb serveis, ja que és un indicador per al sistema d'injecció de dependència Angular que el servei amb el cual estem treballant, pot tindre altres dependències. Amb aquest decorador, Angular s'encarregarà d'injectar-los al nostre servei.

c) Explica los siguientes conceptos de la programación reactiva que se usan en 
RxJS:
    • Observable: funció que converteix el flux normal de dades en un flux de dades observable. Emet els senyals complets quan el flux es completa o un senyal d'error si el flux s'error. L'observable comença a emetre valors només quan algú s'hi subscriu.
    • Subscription: connecta l'observador amb esdeveniments observables. Sempre que es fa qualsevol canvi en aquests observables, s'executa un codi i s'observen els resultats o canvis mitjançant el mètode de subscripció.
    • Operators: peces essencials que permeten compondre fàcilment un codi asíncron complex de manera declarativa.
    • Subject: tipus especial d'observable que permet que els valors siguin multicastats per a molts observadors. Els subjectes també són observadors perquè poden subscriure's a un altre observable i obtenir valor d'ell, que es multidifusió a tots els seus subscriptors.
    • Schedulers: permet definir en quin context d'execució un observable lliurarà notificacions al seu observador, és a dir, gestiona l'ordre i el temps d'execució de les operacions a Observable. 

d) ¿Cuál es la diferencia entre promesas y observables?

Les promeses operen en un únic esdeveniment asíncron, mentre que els observables ens permeten fer front a un flux de zero o més esdeveniments asíncrons.

Mentre que les promeses no es poden cancel·lar, i haurà un moment que es trucarà al gestor d'èxit o d'error de la promesa, en els observables es pot cancel·lar la subscripció i no processar les dades.

Els observables ens permeten compondre i crear una cadena de transformacions fàcilment. Els operadors que proporciona fora de la caixa permeten algunes composicions fortes i potents, i operacions com reintentar i reproduir fan que la gestió d'alguns casos d'ús habituals sigui trivial. Tot això alhora que podem reutilitzar el nostre codi de subscripció.

e) ¿Cuál es la función de la tubería (pipe) async?

La funció de la tubería async, permet unir-nos a Observable. Angular s'encarregaria d'esperar que els esdeveniments s'emetin a l'observable i de mostrar directament el valor resultant. Ens estalvia aquest pas d'haver de subscriure's manualment a l'observable. Solament és útil en algunes situacions en què les dades retornades per una trucada d'API són quelcom que podem mostrar directament. 