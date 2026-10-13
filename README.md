# Sanasto — finská slovní zásoba

Statická webová aplikace pro procvičování finské slovní zásoby z databáze `vocabulary_db.json`.

## Funkce

- Studijní kartičky s hodnocením „Umím“ / „Ještě procvičit“
- Samostatná denní karta s až 10 novými nebo právě splatnými slovy a počítadlem procvičení napříč cvičeními
- Studijní lekce po nejvýše 10 slovech, s interním přepínáním, přehledem postupu a animací po dokončení
- Rozložené opakování známých slov s intervaly 1, 3, 7 a 14 dní
- Orientační A1–C2 podle relativního pořadí četnosti v načtené databázi; ruční úroveň nebo platné CEFR záznamy mají přednost
- Volba jazyka překladů (čeština nebo angličtina); při volbě angličtiny se přepne celé rozhraní
- Návrh překladu jednotlivého slova přes MyMemory; při překladu se ukazují také kontexty z databáze
- Samostatná karta pro rychlé doplňování překladů: návrh vždy pro jedno slovo, Enter překlad uloží, Escape slovo vyřadí z učení a uložený překlad lze upravit
- Samostatné procvičování: kartičky, napsání překladu, doplnění finského tvaru do kontextu volbou ze čtyř možností a výběr překladu ze čtyř možností
- Kontextová nápověda ukáže překlad a přibližný gramatický tvar; v kontextu i při výběru překladu fungují klávesy 1–4, Enter pokračuje a po odpovědi se cvičení samo posune za dvě sekundy
- Párovací hra: pět finských slov a pět samostatně promíchaných uložených překladů; správné dvojice se neodhalují před výběrem, každá se počítá jako procvičení a po dokončení kola se za 2 sekundy spustí další
- Slovník s filtrem podle úrovně, slovního druhu, tématu a stavu učení; zobrazuje slova s četností alespoň 0,1 % celkových výskytů a umožňuje je vyřadit z procvičování
- Oprava importovaného lemmatu i slovního druhu; při duplicitě lze lemmata sloučit včetně četností, tvarů, kontextů a pokroku
- Více významů u jednoho lemmatu s přiřazením konkrétních kontextových vět ke každému významu
- Automatické návrhy sémantických témat (například zvířata, jídlo, domov a cestování), které lze ve slovníku změnit
- Série učení a víceúrovňové odznaky za pravidelné učení, překlady, procvičování i správné odpovědi za sebou
- Potvrzení překladu klávesou Enter a ukládání pokroku v místním úložišti prohlížeče
- Export studijního pokroku jako zálohy

## Spuštění na GitHub Pages

1. Vytvoř nový repozitář s názvem například `sanasto-finnish-vocabulary`.
2. Nahraj do kořene repozitáře soubory `index.html` a `README.md`.
3. V nastavení repozitáře otevři **Settings → Pages**.
4. Jako zdroj vyber **Deploy from a branch**, větev `main` a složku `/(root)`, pak ulož.
5. Po zveřejnění otevři URL, kterou GitHub Pages ukáže v sekci Pages.

## Vlastní slovník a soukromí

Aplikace začíná v ukázkovém režimu s ilustračními větami. Stiskni **Načíst slovník JSON** a vyber svůj `vocabulary_db.json`, který vytváří Python skript. Osobní slovní databázi do veřejného repozitáře nepřidávej. Importovaná databáze, překlady, úrovně, opravy lemmat, témata, vyřazení slov a hodnocení zůstávají v místním úložišti prohlížeče. Odhad úrovně řadí lemmata podle četnosti v právě načteném slovníku a orientačně je rozděluje do šesti pásem A1–C2. Jde pouze o pomocné pořadí uvnitř osobní databáze, nikoli o oficiální CEFR hodnocení. Platné úrovně ze zdrojových polí `level`/`cefr` a ruční volba mají přednost. Překlady navrhuje MyMemory; před prvním dotazem se aplikace zeptá na souhlas a odešle jen jedno finské lemma, nikoli větu nebo celý slovník. Návrh může být nepřesný, proto jej vždy zkontroluj před uložením. Export studijního pokroku zahrnuje i opravy slov, témata, vyřazená slova, sérii a odznaky.

## Lokální spuštění

Otevři `index.html` v moderním prohlížeči. Není potřeba sestavení ani serverová část.
