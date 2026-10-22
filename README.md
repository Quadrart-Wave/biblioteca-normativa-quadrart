# Biblioteca normativă Quadrart

Pluginul aduce în Claude legislația României și actele UE aplicabile, în forma consolidată, cu data formei: construcții și urbanism, energie, mediu, normative tehnice, codurile, fiscal, muncă, achiziții publice. Odată cu biblioteca vine și felul de lucru: Claude caută legea în bibliotecă, citește articolul în forma de la data care contează, citează doar ce a citit și își verifică răspunsul cu biblioteca înainte să ți-l dea.

## Ce conține

- conectorul bibliotecii, `punte` (`https://punte.quadrart.ro/mcp`);
- skill-ul `legislatia-romaniei`, care îi spune lui Claude ordinea muncii: caută (`normative_cauta`), citește (`normative_citeste_articol`), citează, verifică (`normative_verifica_text`).

## Ce îți trebuie

- un cont Claude plătit (Pro, Max, Team sau Enterprise); pe contul gratuit nu se pot adăuga pluginuri;
- fișierul `biblioteca-normativa-quadrart.zip`, primit de la Quadrart;
- utilizatorul și parola pentru Biblioteca normativă Quadrart, primite de la Quadrart.

## Cum îl legi

1. În Claude: **Customize › Plugins › Add › Upload plugin** și alegi fișierul `biblioteca-normativa-quadrart.zip`, fără să-l dezarhivezi.
2. Deschizi pluginul, fila **Connectors**, și apeși **Connect** la „punte”.
3. Intri cu utilizatorul și parola primite și accepți accesul pentru Claude; la prima intrare ți se pot cere și termenii de folosire. Biblioteca apare **Connected**.
4. **Lași Claude să folosească biblioteca fără să te întrebe.** În aceeași filă **Connectors**, la „punte”, **Tool permissions › Always allow**. Altfel Claude îți cere aprobarea la fiecare căutare și citire.

Pe un cont Team sau Enterprise, administratorul (Owner) adaugă întâi conectorul pentru firmă; fiecare om face apoi pașii 2-4 cu contul lui.

## Ce trebuie să fie pornit

Dacă pluginul nu pare să lucreze, verifici:
1. **Settings › Capabilities › Code execution and file creation** e pornit; skill-urile au nevoie de el. Pe Team și Enterprise îl pornește administratorul.
2. Skill-ul `legislatia-romaniei` e pornit în **Customize › Skills** (se pornește odată cu pluginul).
3. Conectorul apare **Connected** în fila **Connectors** a pluginului.

## Cum îl folosești

Întrebi cum ai întreba un coleg, și în cuvinte de zi cu zi. De regulă, Claude pornește singur skill-ul când întrebarea e despre lege; îl poți chema și tu, scriind `/` în conversație și alegându-l din listă. Dacă biblioteca nu e legată, Claude îți spune să faci pașii 2 și 3, în loc să răspundă din memorie.

## Ce date trimite

La serverul bibliotecii, `punte.quadrart.ro`, legat cu contul tău Quadrart, ajung:
- textul căutărilor, adică cuvintele-cheie sau întrebarea, așa cum le formulează Claude;
- articolele cerute la citire;
- textele trecute prin verificare: documentele pe care le dai spre verificare și ciorna răspunsului lui Claude.

Serverul ține un jurnal al acestor apeluri, legat de cont. Din textele verificate jurnalul păstrează doar o amprentă (suma de control) și lungimea, nu textul. Jurnalul se păstrează 12 luni, apoi se anonimizează; la cerere, rândurile contului tău se anonimizează mai devreme. Răspunsul final al lui Claude nu ajunge la server. Pluginul nu ține date pe calculatorul tău și nu conține programe sau chei.

## Linkuri

- Confidențialitate: https://punte.quadrart.ro/confidentialitate
- Documentație: https://punte.quadrart.ro/documentatie

## Versiunea

0.1.0. Versiunile noi le trimite Quadrart, împreună cu felul în care se înlocuiesc.

Pluginul e proprietatea Quadrart și se folosește doar cu acordul Quadrart (vezi `LICENSE`).
