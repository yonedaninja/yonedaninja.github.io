## Preliminari: categorie arricchite.
La teoria delle categorie arricchite affonda le radici nell'algebra omologica: il primo esempio di tale struttura fu introdotto e studiato da Kelly in [ref] e Eilenberg (per motivi non dissimili da quelli che portarono Grothendieck e Verdier a introdurre le categorie derivate) in [ref]. Scoperto tale interesse comune, Eilenberg e Kelly presero in considerazione strutture con lo stesso comportamento di una categoria, ma dove $\hom(A,B)$ non è più solamente un insieme, quanto piuttosto un intero *complesso di catene* $[A,B]$ (quindi, in paricolare, un gruppo abeliano graduato) e tale per cui le mappe di composizione

$$
c_{ABC} : [A,B]\otimes[B,C]\to [A,C]
$$
sono mappe di catene (definendo opportunamente il prodotto tensoriale a dominio, e il grado della mappa secondo le regole dell'algebra omologica). 

I due si resero però conto piuttosto in fretta che ben pochi dei risultati che saranno poi esposti in [[laJolla](https://link.springer.com/chapter/10.1007/978-3-642-99902-4_22)] dipendono inerentemente dal fatto che gli $\hom(A,B)$ sono complessi di catene; è sufficiente che tali oggetti appartengano a una categoria dove sia definita una operazione di *moltiplicazione* tra oggetti, in maniera debitamente coerente (si pensi ad esempio agli insiemi, agli spazi vettoriali, agli spazi topologici... dove sono definiti il prodotto cartesiano $A\times B$ -con una opportuna topologia prodotto, se $A,B$ sono spazi topologici- oppure il prodotto tensoriale $V\otimes_k W$ di $k$-spazi vettoriali). Chiamiamo le categorie $\mathcal V$ con questa proprietà "categorie monoidali" (o dotate di una "struttura monoidale"), e preleviamo dalla classe degli oggetti di $\mathcal V$ una sotto-classe di $[A,B]$ che si comportino in maniera formalmente analoga agli $\hom(A,B)$ di una categoria, otteniamo oggetti che chiamiamo categorie *arricchite* sulla *base* $\mathcal{V}$.

È bene notare che, sebbene il caso in cui gli $[A,B]$ siano *insiemi* arricchiti di una struttura sia il più frequente nella pratica (e cioè il caso in cui, in particolare, la composizione $[A,B]\otimes[B,C]\to[A,C]$ sia un omomorfismo rispetto alla struttura in questione: questo è il caso in cui gli $[A,B]$ sono gruppi abeliani, spazi vettoriali, complessi di catene, spazi topologici, etc.), questo non è *necessario* alla definizione generale.

Il lavoro [laJolla] si occuperà di stabilire cosa sopravvive della teoria delle categorie classica (dove $\mathcal{V}=\mathbf{Set}$) alla luce di questa osservazione; dallo studio di Eilenberg e Kelly (e da molte successive espansioni) emerge che la teoria si recupera pressoché nella sua totalità: esistono *funtori* arricchiti, trasformazioni naturali arricchite, co/limiti, prefasci, e un "lemma di Yoneda" in una opportuna forma che tiene conto della maggior struttura di un prefascio $[-,X]$. È, allora, solo un caso molto particolare quello della teoria delle categorie *basata su insiemi*; molti risultati classici relativi a una categoria, o a una classe specifica di categorie, "vivono" in un mondo dove sugli hom-set è stata posta una struttura addizionale; molti altri sono naturalmente interpretabili in tal senso, piuttosto che come oggetti pertinenti alla teoria degli insiemi.

In tal senso, l'esempio di apertura è illuminante: la categoria dei complessi di catene è monoidale, rispetto al prodotto di due complessi che è definito dalla posizione

$$
(A\mathop{\underline\otimes} B)_n = \bigoplus_{p+q=n} A_p\otimes B_q
$$
Una categoria arricchita sui complessi di catene si dice una "DG-categoria" (categoria *D*ifferenziale *G*raduata), cosicché per specificare una DG-categoria, per ogni terna di oggetti, e ad ogni grado fissato va specificata una famiglia di mappe bilineari $\varphi_{p,q} : A_p\otimes B_q\to C$; ciascuna di queste famiglie va a formare la componente $n$-esima di una mappa di catene $\varphi : A_*\mathop{\underline\otimes} B_* \to C_*$; e questa descrizione parla solo delle mappe di grado zero...

Appare evidente che una tale interpretazione puramente insiemistica della struttura fortemente annidata delle mappe di composizione $c_{ABC} : [A,B]\mathop{\underline\otimes}[B,C]\to [A,C]$ è improponibile nel caso delle DG-categorie. Diventa allora fondamentale avere a disposizione un formalismo che incapsuli completamente questa complessità in un approccio formale; la struttura monoidale su $\mathbf{Ch}(R)$, dimostrata una e una sola volta, permette di trattare l'intera $c_{ABC}$ come un unico oggetto, e di derivare nuove proprietà da questa descrizione formale.  

La teoria delle categorie arricchite è piuttosto vasta: 

* le categorie monoidali sono oggetti molti ricchi di struttura (nella categoria degli spazi vettoriali di dimensione finita ogni oggetto $V$ ammette un "inverso" $V^\lor$, il suo duale, in modo che esistano delle mappe $V^\lor\otimes V\to k$ e $k\to V\otimes V^\lor$ soddisfacenti a opportune proprietà universali: questo si può astrarre a una richiesta analoga per $\mathcal{V}$). Un resoconto molto utile e pieno di riferimenti che classifica la vasta zoologia di assiomi aggiuntivi da imporre a una categoria monoidale è [ref].
* le categorie monoidali sono oggetti abbastanza ubiquitari: 
    - le categorie *cartesiane*, dove $\otimes$ è il prodotto cartesiano, sono parecchie; una loro opportuna sotto-categoria (quella delle categorie "chiuse") è formata dalle categorie dove è possibile interpretare il $\lambda$-calcolo. Per non parlare poi dei topos elementari (particolari categorie cartesiane chiuse), delle varianti di spazi topologici, e spazi puntati...
    - Le categorie *compatte*, che cioè soddisfano alla proprietà del punto precedente, sono un ambiente naturale per studiare "meccanica quantistica categoriale" [ref,ref,ref] -questa scelta è naturale, dato il ruolo che la categoria $\mathbf{Hilb}$ degli spazi di Hilbert, gioca nella meccanica quantistica. (In un senso opportuno questi due primi esempi sono complementari tra loro: nessuna categoria di spazi di Hilbert può essere cartesiana chiusa.)
    - Dato un gruppo $G$, la categoria delle sue rappresentazioni $k$-lineari $\mathbf{Rep}_k G$ è monoidale, rispetto al prodotto $g\mapsto \rho_V(g)\otimes\rho_W(g)$ (se $\rho_V : G\to \text{Gl}(V), \rho_W : G\to \text{Gl}(W)$ sono le due rappresentazioni); le proprietà della categoria $\mathbf{Rep}_k G$ si traducono in proprietà del gruppo $G$, ed è un'ottima domanda la seguente: quali ipotesi su una categoria monoidale $\mathcal{V}$ assicurano che esiste un gruppo tale per cui $\mathcal{V}\cong \mathbf{Rep}_k G$?

### Definizioni di base
*Definizione.* Una *categoria monoidale* consta di una tupla $(\V_0,\otimes,I,a,l,r)$ in cui
* $\V_0$ è una categoria detta la *categoria sottostante* a $\V$;
* $\otimes : \V_0\times \V_0 \to \V_0$ è un funtore detto *moltiplicazione monoidale*;
* $I$ è un oggetto detto *unità monoidale*;
* $a$ è una famiglia di isomorfismi $a_{XYZ} : X\otimes(Y\otimes Z) \to (X\otimes Y)\otimes Z$ naturale in tutti i suoi argomenti, $l$ è una famiglia di isomorfismi naturali $l_X : I\otimes X\to X$, $r$ è una famiglia di isomorfismi naturali $r_X : X\otimes I \to X$. 

Questi dati sono soggetti ai seguenti *assiomi di coerenza*:

* Esistono due modi di "spostare tutte le parentesi" da $((A\otimes B)\otimes C)\otimes D$ a $A\otimes (B\otimes (C\otimes D))$; il primo assioma di coerenza asserisce che questi due modi coincidono.

$$
\begin{tikzcd}
((A\otimes B)\otimes C)\otimes D \ar[d,"a_{A,B,C}\otimes D"']\ar[r,"a_{AB,C,D}"] & (A\otimes B)\otimes (C\otimes D) \ar[r, "a_{A,B,CD}"] & A\otimes (B\otimes (C\otimes D))\\\\
(A\otimes (B\otimes C))\otimes D \ar[rr,"a_{A,BC,D}"'] && A\otimes ((B\otimes C)\otimes D)\ar[u,"A\otimes a_{B,C,D}"']
\end{tikzcd}
$$
* Il secondo assioma di coerenza stabilisce che l'oggetto $I$ si comporta coerentemente con l'intuizione che esso sia l'unità della moltiplicazione monoidale:

$$
\begin{tikzcd}
(X \otimes I)\otimes Y\ar[dr,"r_X\otimes Y"']\ar[rr,"a_{A,I,Y}"] && X\otimes(I\otimes Y)\ar[dl,"X\otimes l_Y"]\\\\
& X\otimes Y
\end{tikzcd}
$$
Diversi di questi esempi sono già noti a chi conosca i rudimenti della teoria delle categorie: idealmente, tutti sono astrazioni successive dal primo esempio paradigmatico, quello della categoria degli insiemi.

*Esempio (la categoria degli insiemi).* La categoria $\mathbf{Set}$ di insiemi e funzioni è monoidale rispetto al funtore $\times : \mathbf{Set}\times\mathbf{Set}\to\mathbf{Set}$ che manda $(A,B)$ in $A\times B$. L'associatività è data dall'isomorfismo canonico $A\times(B\times C)\cong (A\times B)\times C$ (entrambi gli insiemi soddisfano la stessa proprietà universale) e l'oggetto unità è l'(ogni scelta di un) insieme terminale. La struttura monoidale così determinata è *simmetrica*, ossia $A\times B\cong B\times A$ con un isomorfismo naturale nei due argomenti.

*Definizione (categoria monoidale simmetrica).* Una categoria monoidale si dice *simmetrica* quando oltre alla struttura monoidale $(\otimes,I,al,l,r)$ essa è dotata di una famiglia di *intrecciamenti*
$$
B_{X,Y} \colon X \otimes Y \to Y \otimes X 
$$
uno per ogni coppia di oggetti, che soddisfa al seguente *assioma esagonale* di coerenza:

$$
\begin{tikzcd}
(X\otimes Y)\otimes Z \ar[r,"a_{X,Y,Z}"]\ar[d,"B_{X,Y}\otimes Z"']& X\otimes (Y\otimes Z) \ar[r,"B_{X,Y\otimes Z}"]& (Y\otimes Z)\otimes X\ar[d,"a_{Y,Z,X}"] \\\\
(Y\otimes X)\otimes Z \ar[r,"a_{Y,X,Z}"']& Y\otimes (X\otimes Z) \ar[r,"Y\otimes B_{X,Z}"']& Y\otimes (Z\otimes X)
\end{tikzcd}
$$
e tale per cui $B_{X,Y}\cdot B_{Y,X} = 1$.

*Esempio (la categoria degli spazi topologici).* La categoria $\mathbf{Top}$ di spazi topologici e funzioni continue è monoidale rispetto al funtore $\times : \mathbf{Top}\times\mathbf{Top}\to\mathbf{Top}$ che manda $((A,\tau_A),(B,\tau_B))$ nell'insieme $A\times B$ dotato della *topologia prodotto* che ha per base la collezione dei sottoinsiemi $U\times V\subseteq A\times B$ al variare di $U\in\tau_A,V\in\tau_B$. L'associatività è data dall'isomorfismo canonico $A\times(B\times C)\cong (A\times B)\times C$ (entrambi gli oggetti soddisfano la stessa proprietà universale) e l'oggetto unità è l'(ogni scelta di un) insieme terminale, con l'unica topologia possibile.

*Esempio (la categoria degli insiemi puntati).* La categoria degli insiemi puntati ha per oggetti le coppie $(A,a)$ dove $a\in A$ è un elemento, e per morfismi quelle funzioni $f : (A,a)\to (B,b)$ tali che $f(a)=b$. Definiamo in $\mathbf{Set}_*$ l'operazione di *somma puntata* $A\lor B$ come il pushout

$$
\begin{tikzcd}
{*} \ar[r,"a"]\ar[d,"b"']& A\ar[d] \\\\
B \ar[r] & A\lor B
\end{tikzcd}
$$
Questa posizione definisce una struttura monoidale il cui oggetto unità è l'(ogni scelta di un)oggetto terminale. La proprietà universale di $A\lor(B\lor C)$ è ora la stessa di $(A\lor B)\lor C)$, ciò che implica che i due oggetti sono tra loro isomorfi.

*Esempio (ogni categoria co/cartesiana).* Risulta chiaro come estendere questo esempio ad ogni categoria $\C$ con limiti finiti, dove $\times : \C\times\C\to \C$ è l'aggiunto destro al funtore diagonale $\C \to \C\times\C$ che manda $C$ in $(C,C)$. Dualizzando opportunamente questo risultato, $\C^\text{op}$ diventa monoidale rispetto a $\times^\text{op}$, ovvero (equivalentemente) ogni $\C$ con colimiti finiti diventa monoidale rispetto al *coprodotto* $(C,D)\mapsto C\coprod D$ (l'aggiunto *sinistro* della diagonale $\C \to \C\times\C$).

Data una categoria cartesiana $\C$, la categoria dei funtori $[A,\C]$ eredita i limiti da $\C$ (sono tutti calcolati puntualmente), e dunque $[A,\C]$ è cartesiana; un caso molto speciale (che contiene tutti i dettagli istruttivi di quello generale) è il seguente.

*Esempio (la categoria dei fasci di insiemi).* Un *prefascio di insiemi a valori in $\C$* consta di un funtore $F : \C^\text{op}\to \mathbf{Set}$; nel caso in cui $\C = O(X)$ sia la categoria degli aperti di uno spazio topologico $X$, dove $U\to V$ significa $U\subseteq V$, possiamo definire un *fascio* come un prefascio $F$ tale per cui, in ogni diagramma del tipo

$$
\begin{tikzcd}
	U_\alpha \ar[r, "s_\alpha"]\ar[d, "i_\alpha"']& F \\\\
	U\ar[ur, "t"'] & 
\end{tikzcd}
$$
dove $\{i_\alpha : U_\alpha\subseteq U\}$ sono gli elementi di un ricoprimento di $U\in O(X)$ (confuso con la sua immagine in $[O(X)^\text{op},\Set]$ mediante l'embedding di Yoneda), esista un unica trasformazione naturale $t : y(X) \to F$ tale che $t\cdot i_\alpha = s_\alpha$. Da questa definizione è evidente che i fasci sono una sottocategoria chiusa per prodotti, che cioè se $F,G$ sono fasci lo è il prodotto $F\times G$. 

Diversi altri esempi, non meno elementari, risultano tutti come astrazioni successive da un primo esempio paradigmatico, quello degli spazi vettoriali (o meglio, degli $R$-moduli su un anello).

*Esempio (la categoria degli spazi vettoriali).* (Ci riduciamo a spazi di dimensione finita; l'esempio è comunque istruttivo) Il *prodotto tensoriale* di due spazi vettoriali $V,W$ è lo spazio vettoriale $V\otimes W$ definito dalla proprietà universale di rappresentare il funtore $\text{Bil}(-\times-,k)$, ossia tale per cui le applicazioni *bilineari* $V\times W\to k$ corrispondano mediante un isomorfismo naturale alle mappe lineari

$$
\text{Bil}(V\times W,k)\cong\hom_k(V\otimes W,k).
$$
Vi sono metodi classici per dimostrare che un tale spazio esiste: si prenda, ad esempio, $k^{|V\times W|}$ e lo si quozienti per le relazioni indotte da $(v+v',w)-(v,w)-(v',w)$, $(v,w+w')-(v,w)-(v,w')$ e da $a(v,w)-(av,w)-(v,aw)$. Questa proprietà universale determina $V\otimes W$ a meno di un unico isomorfismo; da ciò è relativamente semplice ricavare un unitore $V\otimes k\cong V\cong k\otimes W$ e un associatore $a$ (farlo esplicitamente è un esercizio). La struttura così determinata è simmetrica (ancora una volta la proprietà universale).

*Lemma.* Esiste un isomorfismo 

$$
\hom_k(V\otimes U,W)\cong \hom_k(V,\hom_k(U,W))
$$
naturale in tutti i suoi argomenti. In altre parole, per ogni oggetto $V\in\mathbf{Vect}$ i funtori $V\otimes-$ e $\hom_k(V,-)$ sono aggiunti (equivalentemente, $V\mapsto (V\otimes-\dashv \hom_k(V,-))$ definisce una *aggiunzione parametrica* nel senso di [Mac Lane, ???]).

*Dimostrazione.* Definiamo unità e counità dell'aggiunzione; verificare le identità triangolari è un esercizio noioso.
* l'unità dell'aggiunzione ha componenti $\eta_{(V),W}  :W \to [V,V\otimes W]$ e manda il vettore $v$ nella mappa lineare che manda $w$ in $v\otimes w$;
* la counità ha componenti $\epsilon_{(V),W} : V\otimes [V,W]\to W$ indotte dalla mappa bilineare che manda la coppia $(v,f)$ in $f(v)$.

*Proposizione.* Il prodotto monoidale di $\mathbf{Vect}$ è *cocontinuo*, ossia vale l'isomorfismo

$$\textstyle
V\otimes \big(\varinjlim_{i\in I} W_i\big)\cong \varinjlim_{i\in I} V\otimes W_i
$$
*Dimostrazione.* Ovvia in virtù del Lemma precedente.

*Esempio (la categoria dei moduli graduati).* Un *modulo graduato* su un anello $R$ consta di una famiglia numerabile di $R$-moduli $(A_n\mid n\ge 0)$; una mappa di moduli graduati consta di una famiglia $f_n : A_n \to B_n$ di omomorfismi di $R$-moduli. Questa posizione definisce la categoria degli $R$-moduli graduati $\mathbf{gMod}_R$. La categoria dei moduli graduati è dotata di un prodotto monoidale $\underline\otimes$ definito dalla seguente catena di osservazioni:

- Esiste un'immersione $\mathbf{Mod}_R \to \mathbf{gMod}_R$ che manda il modulo $A$ nel modulo graduato che ha $A$ al grado $0$ e zero altrove; la struttura monoidale che cerchiamo *estende* nel senso ovvio, quella che si trova su $\mathbf{Mod}_R$ alla stessa maniera degli spazi vettoriali.
- In virtù del lemma precedente, la catena di isomorfismi

  $$\textstyle
  A\mathop{\underline\otimes} B = \big(\bigoplus_{p\ge 0}A_p\big)\otimes\big(\bigoplus_{q\ge 0}B_q\big) \cong \bigoplus_{p\ge 0}\bigoplus_{q\ge 0} A_p\otimes B_q \cong \bigoplus_{n\ge 0}\bigoplus_{p+q=n}A_p\otimes B_q
  $$ 

  ha senso, e questo determina univocamente la componente di grado $n$ di $A\mathop{\underline\otimes} B$ come $\bigoplus_{p+q=n}A_p\otimes B_q$.

*Esempio (la categoria dei complessi di catene).* Un *modulo differenziale graduato* o *complesso di catene* consta di un oggetto $A$ di $\mathbf{gMod}_R$ dotato di mappe 

$$
\dots \to A_{n+1} \xrightarrow{d_{n+1}} A_n \xrightarrow{d_n} A_{n-1}\to \dots
$$
dette *differenziali* del complesso, tali che per ogni $n$ si abbia $d_n d_{n+1}=0$; questo implica che $\ker d_n$ contiene l'immagine di $d_{n+1}$, e permette di definire l'*omologia* del complesso $A$ come il quoziente $H_n(A)\coloneqq \frac{\ker d_n}{\text{im }d_{n+1}}$. Il modulo graduato $A\otimes B$ ottenuto da due complessi di catene, riguardati come oggetti di $\mathbf{gMod}_R$, ottiene una naturale struttura di complesso di catene ponendo il differenziale $d_{A\otimes B} \coloneqq d_A\otimes B + (-1)^{\deg} A\otimes d_B$. 

È un'ottima domanda (difficile, e non molto pertinente al nostro discorso) come poter calcolare l'omologia di $A\otimes B$ a partire da quella di $A$ e di $B$ separatamente. Invece di concentrarsi su questa domanda, però, preferiamo presentare un esempio legato a quelli precedenti, ma leggermente patologico: quello degli *spazi di Banach* reali.

*Definizione (categoria degli spazi di Banach).* La categoria $\Ban$ ha per oggetti gli spazi di Banach (spazi vettoriali reali normati e completi rispetto alla norma), e per morfismi le mappe lineari. È però un fatto noto che affinché una tale mappa lineare sia continua, rispetto alle topologie naturali che sono indotte sugli spazi di Banach, questa deve essere *limitata*, ossia deve essere $\|f\|=\sup\{\|fv\| \mid v\in V; \|v\|\le 1\} <\infty$. Ciò porta alla definizione più naturale della categoria $\Ban_\le$ che ha per oggetti gli spazi di Banach e per morfismi le mappe lineari *corte*, cioè quelle per cui $\|f\|\le 1$.

Ora, costruire strutture monoidali su spazi vettoriali topologici non è semplicissimo, perché spesso e volentieri (sempre in dimensione infinita) il prodotto tensoriale algebrico $V\otimes_\text{Alg} W$ non ha alcun riguardo della topologia che esisteva su $V,W$; vi sono tuttavia due definizioni standard, ottenute *completando* opportune norme su $V\otimes_\text{Alg} W$.

*Definizione (prodotto tensoriale proiettivo e iniettivo).* Dati due spazi di Banach $V,W\in\Ban$ osserviamo anzitutto che ogni elemento di $V\otimes_\text{Alg} W$ si scrive in maniera unica come una combinazione lineare quasi ovunque finita $\sum_i \alpha_i v_i \otimes w_i$; ora, dato un tale elemento $x$ definiamo la sua *norma proiettiva* come

$$
\|x\|_\pi \coloneqq \inf_{\mathcal S} \left\{ \sum {|\alpha_i|} {\|v_i\|_V} {\|w_i\|_W}  \right\}
$$
dove $\mathcal S$ è l'insieme di tutte le scritture $\sum \alpha_i v_i w_i$ che danno $x$ -non sono uniche!; dualmente, se $\lambda,\mu$ sono funzionali lineari $V,W\to \mathbb R$ rispettivamente, allora $\lambda \otimes \mu : V\otimes W \to \mathbb R\otimes\mathbb R \cong \mathbb R$ è un funzionale sul prodotto tensoriale $V \otimes W$. Definiamo, dato $x\in V\otimes W$, la *norma iniettiva* di $x$ come

$$ 
\|x\|_\epsilon \coloneqq \sup_{\lambda,\mu} \left\{ |(\lambda \otimes \mu)x| \right\}.
$$
dove $\mid \|\lambda\|_{V^*}, \|\mu\|_{W^*} \leq 1$. Il prodotto tensoriale proiettivo $V\otimes_\pi W$ è definito come il completamento dello spazio normato $(V\otimes_{\text{Alg}}W,\|\_\|_\pi)$, laddove il prodotto tensoriale iniettivo $V\otimes_\epsilon W$ è definito come il completamento dello spazio normato $(V\otimes_{\text{Alg}}W,\|\_\|_\pi)$

*Proposizione.* La tupla $(\Ban_\le,\otimes_\pi,\mathbb R)$ è una categoria monoidale, dotata delle coerenze ovvie ereditate da quelle di $\mathbf{Vect}$.

*Dimostrazione.* Omessa. $V\otimes_\pi W$ esiste in quanto oggetto di $\mathbf{Vect}$ è ovvia; resta da dimostrare che gli associatori e unitori ereditati da $\mathbf{Vect}$ sono effettivamente mappe in $\Ban_\le$.

*Proposizione.* $\Ban_\le(\mathbb R, V)$ coincide con la palla unitaria di $V$, ossia col sottospazio topologico dei vettori $x\in V$ tali che $\|x\|_V\le 1$.

*Dimostrazione.* Esiste un isomorfismo di spazi vettoriali $\Ban(\mathbb R,V)\cong V$ indotto dalla mappa $f\mapsto f(1_\mathbb R)$; è tuttavia facile notare che questo isomorfismo induce per trasporto di topologie un omeomorfismo con $V$, e che $\Ban_\le$ corrisponde al sottospazio di $V$ dei vettori $\{v\mid \|v\|\le 1\}$ (l'isomorfismo è isometrico nelle norme). Questa è esattamente la palla unitaria di $V$.

Due esempi a loro stanti meritano una certa attenzione:

*Esempio (Endofuntori di $\cal C$).* Se $\C$ è una qualsiasi categoria, possiamo considerare (eventualmente in un universo più grande) la categoria $[\C,\C]$ degli *endofuntori* di $\C$, che ha per morfismi le trasformazioni naturali. Questa categoria ha una struttura monoidale data dalla *composizione* di funtori, per cui l'oggetto unità è il funtore identico. Ovviamente, la coerenza data dall'associatore e dagli unitori è una vacuità, dato che la composizione di funtori $F(GH)=(FG)H$ è strettamente associativa e unitaria. 

*Definizione (categoria monoidale stretta).* In tali circostanze (quando cioè $A\otimes (B\otimes C)$ non è solo isomorfo a $(A\otimes B)\otimes C$, ma è proprio lo stesso oggetto, e lo stesso accade per $I\otimes A,A\otimes I$) la categoria monoidale si dice *stretta*. 

Un altro esempio di categoria monoidale stretta è dato dall'insieme $\mathbb R_{\ge,*} = \mathbb R_\ge \cup\{\infty\}$ dei numeri reali non negativi, possibilmente infiniti, denotato per brevità $[0,\infty]$.

*Esempio (L'esempio dei numeri reali).* La categoria $([0,\infty],\ge)$ (dove esiste un morfismo $x\to y$ se e solo se $y\le x$) su definita ha una struttura di categoria monoidale stretta, rispetto alla somma di numeri reali; la struttura è evidentemente simmetrica e stretta.

*Definizione (Categoria monoidale chiusa).* Una categoria monoidale $(\V,\otimes,I)$ si dice *chiusa* quando ciascun endofuntore $V\otimes\_ : \V \to \V$ ha un aggiunto destro $[V,-]$. Questo realizza l'isomorfismo

$$
\V(V\otimes W,Z)\cong \V(V, [W,Z])\cong \V(W, [V,Z]).
$$
*Esempi.* La categoria degli insiemi, degli insiemi puntati, degli spazi vettoriali, dei moduli graduati e $[0,\infty]$ sono tutte chiuse:
* In $\mathbf{Set}$, $[A,B]$ è l'insieme delle funzioni $f : A\to B$
* In $\mathbf{Set}_*$, $[(A,a),(B,b)]_*$ è l'insieme delle funzioni $f : (A,a)\to (B,b)$ per cui $f(a)=b$, e questo insieme ha come punto privilegiato la funzione costante in $b$.
* In $\mathbf{gMod}_R$, $[X,Y]$ è il modulo graduato $[X,Y]_n := \prod_{i \in \mathbb{Z}} \hom_R(X_i, Y_{i+n})$; in caso $X,Y$ siano dei complessi di catene, il differenziale agisce come $d f := d_Y \cdot f - (-1)^{n} f \cdot d_X$.
* In $[0,\infty]$ definiamo $\langle s,t\rangle$ (chiaramente non possiamo usare $[s,t]$...) come $\max\{t-s,0\}$ (verificare che questa è davvero una chiusura: a cosa si riduce l'isomorfismo della definizione?).

Abbiamo ora raccolto una quantità di esempi sufficiente a introdurre l'oggetto di questo primo capitolo: le categorie *arricchite* su una categoria monoidale.

*Definizione ($\V$-categoria).* Una *categoria arricchita sulla base monoidale $\V$*, o brevemente una *$\V$-categoria* $\enA$, consta di 
* una classe di oggetti $\enA_0$; 
* un oggetto $\enA[A,B]\in\V$ per ogni coppia di oggetti $A,B\in\mathbf{A}_0$;
* una famiglia di *composizioni* $c_{ABC} : \enA[A,B]\otimes \enA[B,C]\to \enA[A,C]$, una per ogni terna di oggetti di $\enA$;
* una famiglia di *identità* $i_A : I \to \enA[A,A]$, una per ogni oggetto di $\enA$.

Questi dati sono soggetti agli assiomi seguenti:

* La composizione è associativa, tramite l'associatore di $\V$; ossia il diagramma 
  
  $$ \begin{tikzcd}
\big(\enA[C,D]\otimes \enA[B,C]\big)\otimes \enA[A,B]\ar[d,"c_{BCD}\otimes 1"']\ar[rr,"a"] && \enA[C,D]\otimes \big(\enA[B,C]\otimes \enA[A,B]\big) \ar[d,"1\otimes c_{BCD}"]\\\\
\enA[B,D]\otimes \enA[A,B]\ar[dr, "c_{ABD}"'] && \enA[C,D]\otimes\enA[A,C]\ar[dl, "c_{ACD}"]\\\\
& \enA[A,D] & 
\end{tikzcd} $$
  è commutativo.
* La composizione ha le $i_A$ come identità, ossia i due diagrammi
  
  $$ \begin{tikzcd}
  \enA[B,B]\otimes\enA[A,B] \ar[r,"c_{ABB}"]& \enA[A,B] &\ar[l, "c_{AAB}"'] \enA[A,B]\otimes\enA[A,A]\\\\
  I\otimes\enA[A,B]\ar[u, "i_B\otimes 1"] \ar[ur]&&\enA[A,B]\otimes I\ar[u, "1\otimes i_A"'] \ar[ul]
  \end{tikzcd} $$
  sono commutativi.

*Osservazione.* La definizione non ne ha bisogno, ma i nostri esempi di elezione coinvolgeranno sempre categorie monoidali *simmetriche* e *chiuse*, e molto spesso anche dotate di tutti i limiti e i colimiti.

*Esempio (la categoria $\Cat$).* È un ottimo esercizio mostrare che la categoria delle $\Set$-categorie (quando $\Set$ è considerata con la sua struttura cartesiana su menzionata) coincide con la categoria $\Cat$: un $\Set$-funtore è precisamente un funtore tra categorie (dove ogni $\C[A,B]$ è un insieme), e una trasformazione $\Set$-naturale è precisamente una trasformazione naturale.

*Esempio (la categoria $\mathbf{Ab}\text{-}\Cat$).* La categoria delle categorie *preadditive* coincide con la categoria delle $\mathbf{Ab}$-categorie, dove ogni $\enA[A,A']$ è un gruppo abeliano; è un fatto interessante e classico (vedi ad esempio [Freyd]) che ipotesi addizionali di completezza su $\C$ inducano naturalmente un $\mathbf{Ab}$-arricchimento canonico.

*Esempio (la categoria $\text{DG}\text{-}\Cat$).* Questo è l'esempio con cui abbiamo iniziato l'introduzione. In una DG-categoria ogni $\enA[A,A']$ è un complesso di catene; la composizione è una mappa di catene
$$
c_{ABC} : \enA[A,A']\mathop{\underline\otimes}\enA[A',A''] \to \enA[A,A'']
$$
definita dal dominio $\enA[A,A']\mathop{\underline\otimes}\enA[A',A''] = \bigoplus_{n\ge 0} \bigoplus_{p+q=n}\enA[A,A']_p\otimes \enA[A',A'']_q$.

*Esempio (la categoria degli spazi metrici generalizzati).* Una categoria (piccola) arricchita su $\mathbb R_{\ge,*}$, seguendo la definizione, è un insieme su cui è definita una funzione $d_X : (x,y) \mapsto d(_X(x,y)$ tale per cui $d_X(x,x)\ge 0$ e $d(x,y)\le d_X(x,z)+d_X(z,y)$. A meno della simmetria, e del fatto che è possibile $d_X(x,y)=\infty$, questo è esattamente uno spazio metrico (tali generalizzazioni si dicono infatti *spazi metrici generalizzati*).

Segretamente, questo è l'esempio che motiva questa introduzione.

*Esempio (la categoria $\Cat\text{-}\Cat$).* La categoria $\Cat$ è cartesiana, rispetto al prodotto di categorie; questa struttura monoidale può essere usata per considerare categorie arricchite in $\Cat$, dove cioè ogni $\enA[A,A']$ è una *categoria*, e composizione $c_{ABC} : \enA[A,B]\times\enA[B,C]\to \enA[A,C]$ e identità sono funtori. 

Una categoria arricchita in $\Cat$ si indica brevemente con il nome *2-categoria* (stretta: ma ignoriamo questo aggettivo per il momento). L'obiettivo delle lezioni successive sarà uno studio ragionato di questa particolare categoria.

Questa procedura si presta a una definizione induttiva: per ogni $n\ge 1$, esiste una "categoria delle categorie arricchite in $(n-1)$-categorie", detta categoria delle $n$-categorie (strette, ma ignoriamo questo aggettivo) $n\text{-}\Cat \coloneqq ((n-1)\text{-}\Cat)\text{-}\Cat$.

Il fatto che, con la scelta di $[\C,\D]$ come la categoria dei funtori $F,G : \C\to \D$, $\Cat$ diventi una 2-categoria $\underline{\Cat}$ porta alla seguente

*Proposizione.* Se $\V$ è monoidale *chiusa*, essa si può sempre considerare come categoria arricchita su sé stessa; la indichiamo $\underline{\V}$, e $\underline{\V}[V,V']$ è dato dall'hom interno $[V,V']$. Gli assiomi di $\V$-categoria sono immediatamente verificati.

Definiamo ora la nozione di *funtore* tra $\V$-categorie; si tratta di una astrazione della definizione classica, che rende evidente il rifiuto (o l'impossibilità) di fare ricorso a nozioni di teoria degli insiemi: un $\V$-funtore, ora, non è più determinato da una funzione sui morfismi, ma da una *famiglia* di morfismi di $\V$, uno per ogni coppia di oggetti di $\enA$, che soddisfa determinati assiomi.

*Definizione ($\V$-funtore).* Fissate una coppia di $\V$-categorie $\enA,\enB$ un *$\V$-funtore* $F : \enA\to \enB$ consiste di una funzione di classe $F_0 : \enA_0\to \enB_0$ e di una famiglia $F_{AB} : \enA[A,B] \to \enB[F_0A,F_0B]$ tale che i diagrammi

$$ \begin{tikzcd}
\enA[B,C]\otimes \enA[A,B] \ar[r]\ar[d] & \enA[A,C]\ar[d] \\\\
\enB[FB,FC]\otimes\enB[FA,FB] \ar[r] & \enB[FA,FC]
\end{tikzcd} \qquad\qquad \begin{tikzcd}
&I\ar[dr]\ar[dl]&\\\\
\enA[A,A]\ar[rr] && \enB[FA,FA]
\end{tikzcd} $$
siamo commutativi. Diciamo che un tale $F$ è *pienamente fedele* quando tutti i $F_{AB}$ sono isomorfismi in $\V$; è questo il caso quando (ad esempio) $F_0$ è l'inclusione di una sottoclasse $\enA_0\subseteq \enB_0$.

*Osservazione.* I $\V$-funtori si possono comporre; esiste una definizione di "$\V$-funtore identico" per cui $\VCat$ diventa una categoria.

È tuttavia possibile rendere la collezione dei $\V$-funtori $\enA\to\enB$ più di un insieme: la prossima definizione si occupa di ciò.

*Definizione ($\V$-trasformazione naturale).* Fissati due $\V$-funtori $F,G$ diciamo *$\V$-trasformazione naturale* $\alpha : F\Rightarrow G$ una famiglia di morfismi di $\V$ $\alpha_A : I \to \enB[FA,GA]$ tali che il diagramma

$$ \begin{tikzcd}
I \otimes \enA[A,B] \ar[r]& \enB[FB,GB]\otimes \enB[FA,FB] \ar[d]\\\\
\enA[A,B] \ar[u]\ar[d]& \enB[FA,GB]\\\\
\enA[A,B]\otimes I\ar[r] & \enB[GA,GB]\otimes\enB[FA,GA]\ar[u]
\end{tikzcd} $$

È possibile definire
* Una *composizione verticale* di trasformazioni $\V$-naturali, definita con componenti
  $$ I\cong I\otimes I \xrightarrow{\alpha_A\otimes\beta_A} \enB[FA,GA]\otimes\enB[GA,HA] \xrightarrow{c_{FA,GA,HA}} \enB[FA,HA]$$ 
* Una *composizione orizzontale* di trasformazioni $\V$-naturali, definita dal diagramma commutativo
  $$ I \cong  I\otimes I \xrightarrow{\alpha_A\otimes I} \enB[FA,GA]\otimes I \xrightarrow{H_{FA,GA}\otimes I} \C[HFA,HGA]\otimes I \xrightarrow{\C[HFA,HGA]\otimes\beta_{GA}} \C[HFA,HGA] \otimes \C[HGA,KGA] \xrightarrow{c_{HFA,HGA,KGA}} \C[HFA,KGA] $$

È evidente che la strategia con cui queste definizioni sono state presentate vuole suggerire che stiamo tentando di riprodurre la struttura della categoria $\Cat$ che raccoglie tutte le categorie, e dove ogni $\hom(\C,\mathcal D)$ è una categoria (i cui oggetti sono i funtori $F : \C\to\mathcal D$ e i cui morfismi sono le trasformazioni naturali $\alpha : F\Rightarrow G$). Questo è un atto volontario: l'oggetto di questo corso è in un certo senso lo studio delle $\Cat$-categorie, ossia della totalità delle strutture che condividono questa stessa proprietà con $\Cat$.

Resta inteso, allora, che il nostro esempio base di 2-categoria (quello ciò a cui cercheremo di riportare ogni nuova nozione che introduciamo, lungo la discussione) è allora quello delle $\V$-categorie.

La prossima sottosezione ha lo scopo di rendere precisa, ed estendere, questa osservazione informale.

### La struttura di $\VCat$

Una caratteristica essenziale della categoria $\Cat$ è quella di essere cartesiana: avendo limiti finiti (e in effetti, limiti di ogni cardinalità) $\Cat \times\Cat\to\Cat$ definisce una struttura monoidale cartesiana, dove $\C\times\D$ è il *prodotto* di categorie, cioè la categoria che ha per oggetti la classe prodotto $\C_0\times\D_0$ e per morfismi $\C\times\D((C,D), (C',D'))$ il prodotto cartesiano $\C(C,C')\times\D(D,D')$ di insiemi. In più, esiste una *categoria* di funtori $\C\to \D$ che rende vero l'isomorfismo naturale

$$
\Cat(\C\times\D,\mathcal{E})\cong\Cat(\C,[\D,\mathcal{E}])\cong \Cat(\D,[\C,\mathcal E])
$$
È evidente che nel gergo introdotto in questa sezione, $\Cat$ è una categoria (cartesiana) monoidale chiusa. Ci proponiamo di dimostrare che questo vale in generale per ogni altra $\VCat$.

*Proposizione.* La categoria $\VCat$ delle $\V$-categorie ha una struttura monoidale.

*Dimostrazione.* Date due $\V$-categorie $\enA,\enB$ definiamo $\enA\otimes\enB$ come la $\V$-categoria con $\enA_0\times\enB_0$ per oggetti, e dove $\enA\otimes\enB((A,B),(A',B')) \coloneqq \enA(A,A')\otimes\enB(B,B')$ (il prodotto monoidale di $\V$); composizione e identità sono definite di conseguenza. Dalla validità degli assiomi di associatività e identità per $\enA,\enB$ segue che $\enA\otimes\enB$ è una $\V$-categoria.

La $\V$-categoria $\underline{*}$, "libera" sulla categoria terminale, che ha un solo oggetto e tale per cui $\underline{*}(*,*)=I$, fa da oggetto unità. Associatori e unitori seguono dalla presenza degli associatori e unitori in $\V$.

*Osservazione.* Per dimostrare che questa struttura monoidale è chiusa, non è sufficiente invocare la definizione di $\V$-trasformazione naturale: se è vero che $[\enA,\enB]$ ha un candidato naturale per classe degli oggetti, è ugualmente vero che $[\enA,\enB](F,G)$ deve essere un oggetto di $\V$, e non solo l'*insieme* delle trasformazioni $\V$-naturali tra funtori $F,G$. 

È tuttavia vero che

*Proposizione.* Se $\V$ è una fissata categoria monoidale, la classe delle $\V$-categorie, $\V$-funtori e trasformazioni $\V$-naturali diventa una $\Cat$-categoria. 

*Dimostrazione.* Esercizio.

Una procedura standard per confrontare categorie arricchite su basi diverse è sfruttare una aggiunzione tra le basi di arricchimento $\V,\W$ e indurre una analoga aggiunzione tra le $\V$-categorie e le $\W$-categorie. Per introdurre questa nozione abbiamo bisogno della 

*Definizione (funtore monoidale).* Date due categorie monoidali $(\V,\otimes_{\V},I),(\W,\otimes_{\W},J) $ un *funtore monoidale* $F : \V\to \W$ consta di una funzione di classe tra le categorie $\V_0\to \W_0$ e di
* Una famiglia di isomorfismi $\varphi_{AB} : FA\otimes_{\W}FB \to F(A\otimes_{\V} B)$ naturali nei due argomenti;
* Un morfismo $\varphi_0 : J \to F(I)$

tali che i seguenti assiomi siano soddisfatti

* *Associatività delle $\varphi_{AB}$*: il diagramma
$$ \begin{tikzcd}
FA \otimes FB \otimes FC \ar[r]\ar[d]& FA \otimes F(B\otimes C) \ar[d]\\\\
F(A\otimes B)\otimes FC \ar[r] &F(A\otimes B\otimes C)
\end{tikzcd} $$
è commutativo (questo attesta che i due modi distinti di passare da $FA\otimes FB\otimes FC$ a $F(A\otimes B\otimes C)$ coincidono).
* *Unitalità di $\varphi_0$*: i due diagrammi
$$ \begin{tikzcd}
I\otimes FA \ar[d]& \ar[d]\ar[l]FA & FA\otimes I \ar[d]& \ar[d]\ar[l]FA \\\\
FI \otimes FA \ar[r]& F(I\otimes A) & FA\otimes FI \ar[r]& F(A\otimes I)
\end{tikzcd} $$
sono commutativi (questo attesta che i due modi distinti di passare da $FA$ a $F(A\otimes I) ,F(I\otimes A) $ coincidono).

*Osservazione.* Questa definizione è ciò che in letteratura si dice funtore monoidale *forte*; esistono restrizioni e rilassamenti di tale nozione,
* Un funtore monoidale è *stretto* se $F(A\otimes B)$ e $FA\otimes FB$ sono lo stesso oggetto, e analogamente anche le altre coerenze si riducono a delle identità.
* Un funtore monoidale è *lasco* se esistono morfismi (non necessariamente invertibili) $FA\otimes FB\to F(A\otimes B)$ e $J\to F(I)$; dualmente, un funtore *colasco* ha dei morfismi (non necessariamente invertibili) $FA\otimes FB\leftarrow F(A\otimes B)$ e $J\leftarrow F(I)$.

Non ci preoccupiamo di ispezionare queste definizioni; sebbene il caso veramente generale sia quello di un funtore co/lasco ci limitiamo al caso in cui $F$, nella definizione seguente, sia forte.

*Definizione (cambio di base).* Dato un funtore monoidale $F : \V\to\W$ tra categorie monoidali definiamo il *cambio di base mediante $F$* come il funtore $F_\dag : \VCat \to \WCat$ che manda una $\V$-categoria $\enA$ nella $\W$-categoria $F_\dag\enA$ che ha gli stessi oggetti, e dove $F_\dag(\enA)[A,A'] = F(\enA[A,A])$.

*Esempio (la 2-categoria associata a una categoria simpliciale).* Se $\enA$ è una categoria simpliciale, il funtore $\tau_1 : \mathbf{sSet} \to \Cat$ definisce un cambio di base $\tau_{1,\dag} : \mathbf{sSet}\text{-}\Cat \to \text{2-}\Cat$ che manda una categoria simpliciale in una 2-categoria "naturalmente" associata ad essa.

*Esempio (la categoria sottostante a una $\V$-categoria).* Il funtore $\V(I,\_) : \V \to \Set$ definisce un cambio di base $(\_)_o : \VCat \to \Cat = \Set\text{-}\Cat$ che manda una $\V$-categoria nella categoria $\enA_0$ che ha gli stessi oggetti, e dove $\enA[A,A']$ è stato declassato all'insieme $\V(I,\enA[A,A'])$.

<!-- 
- Cambio di base (questo resterà un esempio standard di 2-funtore; fatto tutto nei dettagli)
- Proprietà del 2-funtore di confronto $\VCat\to \Cat$
 -->

### [**PRIMO FOGLIO DI ESERCIZI**](./esercizi/foglio1.pdf)

