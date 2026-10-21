# Websitecheck-rapporten (rapport.go4itstudio.com)

Persoonlijke klantpagina's van de websitecheck van GO 4IT-Studio. Elke check staat in `r/<id>/`:
- `index.html`: laadt `/bekijk.js`;
- `data.json`: het rapport, versleuteld met AES-256-GCM.

De sleutel staat alleen in de link die Goran de klant stuurt: `https://rapport.go4itstudio.com/r/<id>/#<sleutel>`. Hij komt nooit in deze repository en gaat ook niet naar de server. Zonder die link is een rapport niet te lezen.

Een pagina komt hier pas na goedkeuring door Goran (`publiceer_klant.py` in websitecheck-motor) en verloopt na een jaar. `publiceer_klant.py --opruimen` haalt verlopen rapporten weg. AIS-rapporten staan op een eigen adres (rapport.ais-groep.nl), nooit hier.
