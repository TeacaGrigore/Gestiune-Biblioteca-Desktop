# Gestionarea unei biblioteci

Aplicație desktop pentru evidența cărților din bibliotecă și gestionarea împrumuturilor și retururilor.

## Funcționalități principale
- Vizualizarea catalogului de cărți, căutare și filtrare;
- Înregistrarea unei cărți noi;
- Înregistrarea împrumuturilor și a retururilor.

## Arhitectura modulară
""+-------------------------------------------------------------------+
|                     1. INTERFAȚA GRAFICĂ (UI)                     |
|  - Catalog cărți (căutare / filtrare)                             |
|  - Fereastră adăugare carte nouă                                 |
|  - Fereastră împrumut / retur                                     |
|  * Ce face: primește ce apasă sau caută utilizatorul și arată     |
|    rezultatele pe ecran, fără reguli grele în interfață.         |
+---------------------------------+---------------------------------+
                                  | cere acțiuni / trimite date
                                  v
+-------------------------------------------------------------------+
|                     2. LOGICA APLICAȚIEI                          |
|  - Verifică câmpurile introduse (să nu fie goale sau greșite)   |
|  - Controlează dacă mai sunt exemplare disponibile                |
|  - Calculează și actualizează stocul la împrumut sau retur        |
|  * Ce face: decide ce are voie să se întâmple și aplică regulile   |
|    bibliotecii înainte să salveze ceva.                           |
+---------------------------------+---------------------------------+
                                  | citește / salvează înregistrări
                                  v
+-------------------------------------------------------------------+
|                     3. STRATUL DE DATE                            |
|  - Evidența cărților                                              |
|  - Evidența cititorilor                                           |
|  - Evidența împrumuturilor și retururilor                          |
|  * Ce face: păstrează datele salvate și le încarcă când deschizi  |
|    aplicația, separat de ecran și de regulile de calcul.          |
+-------------------------------------------------------------------+ ""

## Diagrama UML (Use Case)
![Diagrama Use Case](diagrams/Diagrama_UML%20%28Use_Case%29.drawio.png)

* **Prototype:** [Deschide prototipul interactiv](https://www.figma.com/proto/GKkqS0BvgeBqCndGNkt3Mi/Gestionarea-unei-biblioteci?node-id=2-2&t=TaeBguUucwHsayIT-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A2)
* **Edit:** [Deschide fișierul în editorul Figma](https://www.figma.com/design/GKkqS0BvgeBqCndGNkt3Mi/Gestionarea-unei-biblioteci?node-id=0-1&t=XQth13cqwQ1Nyxrl-1)

## Structura proiectului
- `prototype/` — imaginile PNG ale ecranelor din Figma
- `diagrams/` — diagrama UML Use Case
- `docs/` — documentația arhitecturii modulare și exportul PDF
- `README.md` — prezentarea proiectului
