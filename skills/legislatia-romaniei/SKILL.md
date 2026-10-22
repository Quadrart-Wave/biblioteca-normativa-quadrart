---
name: legislatia-romaniei
description: "Răspunde din legea românească în vigoare, citită din Biblioteca normativă Quadrart (normative_cauta, normative_citeste_articol, normative_verifica_text), nu din memorie și nu de pe web. Folosește-l la orice întrebare despre legi, ordonanțe, hotărâri, ordine, normative tehnice (P 118, I 7, P 100) și actele UE aplicabile în România, chiar pusă în cuvinte de zi cu zi: factura la curent sau gaz, prosumator, chirie și proprietar, contracte, vecinul și gardul, casă, teren, construcție fără autorizație, ce autorizații îmi trebuie, certificat de urbanism, autorizație de construire, impozite, TVA, PFA, SRL, ANAF, amendă și contestație, contract de muncă, demisie, concediu, moștenire, termene, avize, ISU, mediu, energie, ANRE, achiziții publice, ajutor de stat, PNRR, SAFE. Și la verificare: „am voie?”, „e legal?”, „ce risc?”, „până când?”, „cât e amenda?”, „ce articol spune?”, sau un document, aviz ori ofertă cu trimiteri la lege."
---

# Legislația României, din Biblioteca normativă Quadrart

Legea se schimbă des. Orice regulă de lege din răspuns vine din bibliotecă, citită acum, în forma de la data care contează, nu din memorie sau din documente vechi. Lucrul are șase etape, de la 0 la 5; ultima, înainte de răspuns, este verificarea.

## 0. Biblioteca e legată?

Uneltele bibliotecii au numele terminate în `normative_cauta`, `normative_citeste_articol`, `normative_verifica_text`, `normative_acoperire` (în claude.ai cu un prefix, de exemplu `mcp__<id>__normative_cauta`). Dacă sunt doar numite, le încarci cu căutarea de unelte, după nume.

Dacă uneltele lipsesc cu totul, îi spui omului să lege biblioteca din fila **Connectors** a pluginului „Biblioteca normativă Quadrart” (Customize › Plugins), cu contul primit de la Quadrart; pe un cont de firmă, conectorul îl adaugă administratorul. Până atunci nu răspunzi din memorie la ce spune legea.

## 1. Caută

`normative_cauta`, înainte de orice căutare pe web:
- `intrebare`: întrebarea omului sau cuvintele-cheie;
- `termeni`, când omul vorbește în cuvinte de zi cu zi: aceeași întrebare cu termenii legii (actul, noțiunea juridică). Se caută amândouă: cu cuvintele omului căutarea poate rata articolul, cu termenii legii îl găsește;

O căutare pe fiecare parte a întrebării: condiții, termene, excepții, sancțiuni, căi de atac. Cauți și regimurile vecine (TVA lângă impozit, amenda lângă obligație). Înainte să spui că un act lipsește, întrebi `normative_acoperire` cu `act=...`; abia apoi spui „nu e în bibliotecă”. Web-ul doar pentru ce lipsește, pentru stadiul aplicării sau pentru știri, marcat ca atare.

## 2. Citește

`normative_citeste_articol` pe fiecare articol pe care îl folosești: și pe cele de pe locurile următoare care par să răspundă, pe cele din `necitite`, pe excepții („prin excepție de la...”) și pe articolele la care trimite textul. Cu `la_data` (AAAA-LL-ZZ) când întrebarea privește altă dată, cu `cautare_id` când articolul vine dintr-o căutare.

`legaturi` arată excepțiile și derogările din alte acte: citești ambele texte înainte să te bazezi pe o legătură; „propusa” înseamnă neconfirmată. Graful nu are toate derogările implicite, deci lipsa unei legături nu înseamnă „fără derogări”. Atenționările din rezultat (hotărâri judecătorești, modificări neintegrate, natura textului) le transmiți omului.

## 3. Redă întreagă partea care contează

Valorile, condițiile, termenul, consecința, excepțiile, cu termenii actului. Separi legea de interpretarea ta; când răspunsul depinde de fapte pe care nu le știi, spui care sunt. Nu inventezi articole, numere sau valori.

## 4. Citează doar ce ai citit

Actul, articolul, alineatul, data formei și linkul, cum le dă citirea. Legile au articole („art. 21^1 alin. (2)”), normativele puncte („pct. 6.5”), anexele „Anexa nr. 1, pct. 3.2”.

## 5. Verifică răspunsul, apoi îl dai

Scrii ciorna răspunsului și o treci prin `normative_verifica_text` (cu `la_data`, dacă e cazul). Compari fiecare frază cu textul articolului întors și corectezi ce nu se potrivește: valori, termeni, excepții, acte abrogate. Dacă `nerecunoscute` nu e zero, acele trimiteri nu sunt verificate: le citești sau le scoți. Abia apoi dai răspunsul.

Când omul îți dă un document, un aviz sau o ofertă, treci prin `normative_verifica_text` chiar textul lui și spui ce nu se potrivește.

## Termenii construcțiilor

După Codul amenajării teritoriului, urbanismului și construcțiilor (CATUC, Legea 169/2026): PAC/PAD (nu DTAC/DTAD), proiectul pentru organizarea execuției lucrărilor (nu DTOE), înștiințarea privind data începerii/finalizării lucrărilor; termenii vechi doar pe legea veche. Regimul tranzitoriu: citești art. 582 din Legea 169/2026 și clarificările MDLPA, nu îl rezumi din memorie.
