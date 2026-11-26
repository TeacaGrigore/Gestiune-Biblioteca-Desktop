# Gestionarea unei biblioteci

Aplicație desktop pentru evidența cărților din bibliotecă și gestionarea împrumuturilor și retururilor.

## Funcționalități principale
- Vizualizarea catalogului de cărți, căutare și filtrare;
- Înregistrarea unei cărți noi;
- Înregistrarea împrumuturilor și a retururilor.

## Arhitectura modulară
- **Interfața grafică (UI):** ecranele și butoanele (catalog, filtre, adăugare carte, împrumut și retur), care preiau acțiunile utilizatorului și afișează rezultatele.
- **Logica aplicației:** validează datele introduse, verifică disponibilitatea exemplarelor și actualizează numărul de exemplare la împrumut sau retur.
- **Stratul de date:** salvează și încarcă evidența cărților, cititorilor și împrumuturilor.

## Diagrama UML (Use Case)
![Diagrama Use Case](diagrams/Diagrama_UML_%28Use_Case%29.drawio.png)

## Prototip Figma
Link prototip: [Vezi prototipul în Figma](https://www.figma.com/design/GKkqS0BvgeBqCndGNkt3Mi/Gestionarea-unei-biblioteci?node-id=0-1&t=XQth13cqwQ1Nyxrl)

## Structura proiectului
- `prototype/` — imaginile PNG ale ecranelor din Figma
- `diagrams/` — diagrama UML Use Case
- `docs/` — documentația arhitecturii modulare și exportul PDF
- `README.md` — prezentarea proiectului
