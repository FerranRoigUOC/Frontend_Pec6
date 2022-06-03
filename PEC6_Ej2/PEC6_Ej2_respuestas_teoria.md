¿Cuál es la diferencia entre definir un servicio usando el decorador @Injectable o @NgModule?

Amb el @NgModule, serveix per especificar que un servei s'ha de proporcionar en un modul particular i no per a totes les aplicacions. En canvi, amb el @Injectable, proporciones el servei per a tots els moduls.


b. ¿Qué otras opciones admiten el decorador @Injectable para la propiedad ProvidedIn? ¿Para qué sirven las otras configuraciones? 

root: que serà l'injector a nivell d'aplicació en la majoria d'aplicacions.
platform: que seria l'injector especial de plataforma singleton compartit per totes les aplicacions de la pàgina.
