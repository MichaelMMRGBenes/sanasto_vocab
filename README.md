# Sanasto — finská slovní zásoba

Statická webová aplikace pro procvičování finské slovní zásoby z databáze `vocabulary_db.json`.

## Funkce

- Studijní kartičky s hodnocením „Umím“ / „Ještě procvičit“
- Denní sada až 10 častých slov; nová a splatná slova mají přednost
- Rozložené opakování známých slov s intervaly 1, 3, 7 a 14 dní
- Orientační návrh A1–B2 po uložení překladu podle jeho základního významu a tematických vodítek; odhad má nízkou/střední jistotu a lze ho upravit. Úrovně A1–C2 z polí `level`/`cefr` nebo ruční volba mají přednost
- Volba jazyka vlastních překladů (čeština nebo angličtina) z rozbalovací nabídky
- Návrh překladu přes MyMemory; uživatel ho může upravit, přijmout nebo přepsat
- Režim „Napiš překlad“ pro aktivní vybavování vedle běžných kartiček
- Kvíz na doplňování lemmat do vět
- Rozbalení širšího kontextu věty; otázky kvízu se zobrazí jen tehdy, když lze určit vynechaný tvar
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

Aplikace začíná v ukázkovém režimu s ilustračními větami. Stiskni **Načíst slovník JSON** a vyber svůj `vocabulary_db.json`, který vytváří Python skript. Osobní slovní databáze do veřejného repozitáře nepřidávej. Importovaná databáze, překlady, úrovně a hodnocení zůstávají v místním úložišti prohlížeče. Úroveň se nikdy neodvozuje od četnosti výskytu. Po uložení překladu se aplikace pokusí navrhnout A1–B2 podle významových vodítek v překladu; návrh je orientační, uvádí jistotu a zůstává upravitelný. Když vodítka nestačí, úroveň nenavrhne. Úroveň ze zdrojových polí `level`/`cefr` a ruční volba mají přednost. CEFR neurčuje oficiální seznam jednotlivých finských slov, takže stejné slovo mohou výukové zdroje zařadit různě. Odkaz **Ověřit na Finnly** otevře vyhledání konkrétního lemmatu v jejich veřejných stránkách; Finnly je pouze orientační studijní seznam, nikoli oficiální slovník. Automatické stahování nebo kopírování jejich seznamu aplikace neprovádí, v souladu s [podmínkami Finnly](https://getfinnly.com/terms). Odhad úrovně používá jen lokálně uložený překlad a nic kvůli odhadu neodesílá. Návrh překladu se dotáže služby MyMemory až po potvrzení; odešle jí pouze právě vybrané finské lemma, nikoli kontextovou větu nebo celý slovník. Návrh vždy zkontroluj.

## Lokální spuštění

Otevři `index.html` v moderním prohlížeči. Není potřeba sestavení ani serverová část.
