# Gestionarea unei biblioteci

Aplicație desktop pentru evidența cărților din bibliotecă și gestionarea împrumuturilor și retururilor.

## Funcționalități principale
- Vizualizarea catalogului de cărți, căutare și filtrare;
- Înregistrarea unei cărți noi;
- Înregistrarea împrumuturilor și a retururilor.

## Arhitectura modulară
<<<<<<< HEAD

```text
+-------------------------------------------------------------------+
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
+-------------------------------------------------------------------+
```

* **Interfața grafică (UI):** Aici stau doar ecranele și butoanele din prototipul Figma (catalogul, filtrele, adăugarea unei cărți, împrumutul și returul). Am păstrat interfața separată de calcule ca să fie curată și ușor de modificat.
* **Logica aplicației:** Aici se verifică dacă datele sunt valide, dacă o carte are exemplare libere și se actualizează stocul când se înregistrează un împrumut sau un retur[cite: 10].
* **Stratul de date:** Aici se salvează și se încarcă evidența cărților, cititorilor și împrumuturilor, separat de ecran și de regulile aplicației[cite: 10].
=======
- **Interfața grafică (UI):** ecranele și butoanele (catalog, filtre, adăugare carte, împrumut și retur), care preiau acțiunile utilizatorului și afișează rezultatele.
- **Logica aplicației:** validează datele introduse, verifică disponibilitatea exemplarelor și actualizează numărul de exemplare la împrumut sau retur.
- **Stratul de date:** salvează și încarcă evidența cărților, cititorilor și împrumuturilor.
>>>>>>> 0950c3e (Restore modular architecture list in README)

## Diagrama UML (Use Case)
![Diagrama Use Case](diagrams/Diagrama_UML%20%28Use_Case%29.drawio.png)

* **Prototype:** [Deschide prototipul interactiv](https://www.figma.com/proto/GKkqS0BvgeBqCndGNkt3Mi/Gestionarea-unei-biblioteci?node-id=2-2&t=TaeBguUucwHsayIT-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A2)
* **Edit:** [Deschide fișierul în editorul Figma](https://www.figma.com/design/GKkqS0BvgeBqCndGNkt3Mi/Gestionarea-unei-biblioteci?node-id=0-1&t=XQth13cqwQ1Nyxrl-1)

## Structura proiectului
- `prototype/` — imaginile PNG ale ecranelor din Figma
- `diagrams/` — diagrama UML Use Case
- `docs/` — documentația arhitecturii modulare și exportul PDF
- `README.md` — prezentarea proiectului
