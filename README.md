# Sanasto — finská slovní zásoba

Statická webová aplikace pro procvičování finské slovní zásoby z databáze `vocabulary_db.json`.

## Funkce

- Studijní kartičky s hodnocením „Umím“ / „Ještě procvičit“
- Viditelný denní seznam až 10 nových nebo právě splatných slov, vybíraných s ohledem na četnost
- Rozložené opakování známých slov s intervaly 1, 3, 7 a 14 dní
- Orientační A1–C2 podle relativního pořadí četnosti v načtené databázi; ruční úroveň nebo platné CEFR záznamy mají přednost
- Volba jazyka vlastních překladů (čeština nebo angličtina) z rozbalovací nabídky
- Návrh překladu přes MyMemory po potvrzení; na kartičce se při odhalení připraví automaticky a před uložením jej lze upravit
- Režim „Napiš překlad“ pro aktivní vybavování vedle běžných kartiček
- Párovací hra: spojení pěti finských slov s pěti českými nebo anglickými překlady
- Vyhledávání, filtrování a řazení slovníku
- Potvrzení překladu klávesou Enter a ukládání pokroku v místním úložišti prohlížeče
- Export studijního pokroku jako zálohy

## Spuštění na GitHub Pages

1. Vytvoř nový repozitář s názvem například `sanasto-finnish-vocabulary`.
2. Nahraj do kořene repozitáře soubory `index.html` a `README.md`.
3. V nastavení repozitáře otevři **Settings → Pages**.
4. Jako zdroj vyber **Deploy from a branch**, větev `main` a složku `/(root)`, pak ulož.
5. Po zveřejnění otevři URL, kterou GitHub Pages ukáže v sekci Pages.

## Vlastní slovník a soukromí

Aplikace začíná v ukázkovém režimu s ilustračními větami. Stiskni **Načíst slovník JSON** a vyber svůj `vocabulary_db.json`, který vytváří Python skript. Osobní slovní databázi do veřejného repozitáře nepřidávej. Importovaná databáze, překlady, úrovně a hodnocení zůstávají v místním úložišti prohlížeče. Odhad úrovně řadí lemmata podle četnosti v právě načteném slovníku a orientačně je rozděluje do šesti pásem A1–C2. Jde pouze o pomocné pořadí uvnitř osobní databáze, nikoli o oficiální CEFR hodnocení. Platné úrovně ze zdrojových polí `level`/`cefr` a ruční volba mají přednost. Překlady můžeš dostat od MyMemory při odhalení kartičky nebo v párovací hře; před prvním dotazem se aplikace zeptá na souhlas a odešle jen jednotlivé finské lemma, nikoli větu nebo celý slovník. V párovací hře návrhy před použitím uprav nebo potvrď. Návrhy mohou být nepřesné.

## Lokální spuštění

Otevři `index.html` v moderním prohlížeči. Není potřeba sestavení ani serverová část.
