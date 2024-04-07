Lag en valutakalkulator med valutakursene lagret i et array på server. En "Valuta" er et objekt med 
to attributter, valutasort (USD, SEK, etc.) og valutakurs. Applikasjonen skal ha to HTML-sider.
Den første HTML-siden initierer valutakursene i arrayet på server. Denne må kalles etter applikasjonen 
har startet, før valutakalkulatoren kan brukes.

Arrayet på server kan være:

private ArrayList<Valuta> valutaRegister = new ArrayList<>();
Den andre HTML-siden skal inneholde to inputfelter, én for valutasort og én for verdien
man ønsker å omforme til NOK. Når så en knapp trykkes skal de to inputfeltene overføres som et 
"Valuta"-objekt (nå med beløpet i attributtet/feltet for valutakurs) til server. Der skal man så 
bruke valutasorten til å finne den tilsvarende valutakursen i arrayet. Så skal man beregne norske 
kroner fra dette, returnere beløpet til klienten og vise det der. (Alternativt kan det lages en egen 
klasse for overføringen av beløp og valutasort til server for 
å unngå å bruke "Valuta"-klassen til to ulike konsepter.)
