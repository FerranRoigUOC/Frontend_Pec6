a) ¿Qué son los interceptores?

Es situen entre el HttpClient i el servidor, permetent-li transformar totes les sol·licituds sortints i escoltar i transformar si es necessàri totes les respostes entrants abans de transmetre-les.

b) Analiza la siguiente cadena de operadores de RxJS, explica cada uno de los 
pasos que se están desarrollando y explica en qué caso usarías este código:

this.wines$ = this.searchSubject
 .startWith(this.searchTerm)
 .debounceTime(300)
 .distinctUntilChanged()
 .merge(this.reloadProductsList)
 .switchMap((query) =>
this.wineService.getWine(this.searchTerm));
