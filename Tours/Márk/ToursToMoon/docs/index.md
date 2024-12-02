# Dokumentáció


## Adatbázis ER-Diagram leírása
### Entitások
1.   Utak 
- Fő entitás, ami meghatározza egy út azonosítószámát, nevét, a leírását, kategóriáját és az időtartamát.
2.  Országok
-  Országok listája, kapcsolattal az utakhoz.
3.  Utak_hossza
- Az utak időbeli bontása (napokra), kapcsolattal összeláncolva a programokhoz.
4.  Programok
- Az utakhoz tartozó napi programok részletezése (például: helyszínre, időpontra, tevékenységre).
5.  Városok
- Az utazás országon belüli elhelyezkedését határozza meg, az adott országgal összekapcsolva.

### Attribútumok
[Utak] -ban:
-   utak_azon [PK]
-   orszag_azon [FK] érték
-   ut_neve
-   leiras
-   uatazas_kat
-   idotartam


[Utak_hossza] -ban:
-   utido_azon [PK]
-   utak_azon [FK] érték
-   nap_sorszam

[Programok] -ban:
-   program_azon [PK]
-   utido_azon [FK]
-   programleiras
-   idopont
-   helyszin