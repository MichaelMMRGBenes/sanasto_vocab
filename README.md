# Sanasto — finská slovní zásoba

Statická webová aplikace pro procvičování finské slovní zásoby z databáze `vocabulary_db.json`.

## Funkce

- Studijní kartičky s hodnocením „Umím“ / „Ještě procvičit“
- Kvíz na doplňování lemmat do vět
- Vyhledávání, filtrování a řazení slovníku
- Ukládání českých významů a pokroku v místním úložišti prohlížeče
- Export studijního pokroku jako zálohy

## Spuštění na GitHub Pages

1. Vytvoř nový repozitář s názvem například `sanasto-finnish-vocabulary`.
2. Nahraj do kořene repozitáře soubory `index.html` a `README.md`.
3. V nastavení repozitáře otevři **Settings → Pages**.
4. Jako zdroj vyber **Deploy from a branch**, větev `main` a složku `/(root)`, pak ulož.
5. Po zveřejnění otevři URL, kterou GitHub Pages ukáže v sekci Pages.

## Vlastní slovník a soukromí

Aplikace začíná v ukázkovém režimu s ilustračními větami. Stiskni **Načíst slovník JSON** a vyber svůj `vocabulary_db.json`, který vytváří Python skript. Skutečná slovní databáze není součástí tohoto balíčku. Pokud nechceš zveřejnit věty z osobních přepisů, nenahrávej databázi do veřejného repozitáře. Importovaná databáze, české významy a hodnocení se ukládají v místním úložišti daného prohlížeče a aplikace je sama neodesílá na GitHub.

## Lokální spuštění

Otevři `index.html` v moderním prohlížeči. Není potřeba sestavení ani serverová část.
