# 1. projektfeladat – Hitelkockázat előrejelzése

**Félév:** 2026/2027. tanév, őszi félév  
**Beadási határidő:** november 27, 23:59  
**Az eredmények bemutatása:** december 4.

## A feladat célja

A pénzintézetek számára fontos kérdés, hogy egy hiteligénylő várhatóan képes lesz-e teljesíteni fizetési kötelezettségeit. A rendelkezésre álló adatokból gépi tanulási módszerekkel megbecsülhető a súlyos fizetési késedelem kockázata. A problémát bináris osztályozási feladatként kezeljük: azt szeretnénk előre jelezni, hogy bekövetkezik-e egy adott esemény.

A beadandó során a [Give Me Some Credit](https://www.kaggle.com/c/GiveMeSomeCredit) adathalmazával fogsz dolgozni. A cél annak előrejelzése, hogy egy ügyfél a következő két év során súlyos fizetési késedelembe kerül-e. Az ezt jelző célváltozó a `SeriousDlqin2yrs`, amelynek értéke 0 vagy 1.

A Kaggle már elkülönítette a tanításhoz és a végső értékeléshez használható adatokat. A `cs-training.csv` körülbelül 150 000 címkézett megfigyelést tartalmaz. A `cs-test.csv` állományban a célváltozó értékei nem állnak rendelkezésre: ezekre kell előrejelzést készítened. Az eredeti verseny 2011-ben lezárult, de a Kaggle lehetőséget biztosít az utólagos beküldések (*Late Submission*) értékelésére. **A beadandó részeként a végső előrejelzéseidet a Kaggle felületére is be kell küldened.**

A feladatban a teljes modellezési folyamatot végig kell követned az adatok megismerésétől az eredmények értelmezéséig. **Nem pusztán a minél magasabb Kaggle-pontszám a cél:** legalább ilyen fontos, hogy a módszereket megfelelően alkalmazd, a döntéseidet meg tudd indokolni, és a kísérleteid megismételhetők legyenek.

### Egyéni munka és felhasználható segédeszközök

**A beadandó egyéni feladat:** minden hallgatónak saját megoldást és saját beszámolót kell leadnia. A felhasználható eszközökre és forrásokra ugyanakkor **nincs megkötés**. Bármilyen programozási nyelvet, könyvtárat, fejlesztőkörnyezetet, szakirodalmat, internetes segédanyagot, Kaggle-megoldást, példakódot vagy generatív mesterséges intelligencián alapuló eszközt (például ChatGPT-t) használhatsz.

A felhasznált forrásokat hivatkozással jelöld meg, és röviden jelezd, ha a megoldás egyes részeihez MI-eszközt vettél igénybe. Az értékelés során azt is figyelembe vesszük, hogy **érted-e a beadott kód működését, a választott módszerek lényegét és a kapott eredményeket**, valamint szükség esetén meg tudod-e magyarázni őket.

## Részfeladatok

### 1. Az adatok megismerése és előkészítése

- Ismertesd az adathalmaz felépítését és a változók jelentését. Mutasd be a célváltozó eloszlását, különös tekintettel a két osztály arányára.
- Vizsgáld meg a hiányzó adatokat, a változók eloszlását, valamint a szokatlan és kiugró értékeket. Ha valamelyik adatot módosítod vagy kizárod a vizsgálatból, indokold meg a döntésedet.
- Végezd el a szükséges előfeldolgozást, például a hiányzó értékek pótlását vagy a változók skálázását. Vedd figyelembe, hogy a különböző modellek eltérő előfeldolgozást igényelhetnek.
- **A Kaggle által biztosított tanító- és tesztadatokat kezeld külön.** A `cs-training.csv` állományt használd a modellek fejlesztéséhez és belső értékeléséhez. Nem kell belőle egy további, véglegesen elkülönített teszthalmazt létrehoznod. A modellek összehasonlításához és hiperparamétereik hangolásához alkalmazz **rétegzett keresztvalidációt**, amely az egyes részekben megőrzi az osztályok arányát.
- **A `cs-test.csv` fájlt a végső előrejelzések elkészítéséhez használd.** Mivel a célváltozó értékei nem ismertek, ezen az állományon helyben nem tudsz osztályozási mérőszámokat számítani.
- Az adatokból meghatározott előfeldolgozási beállításokat – például a hiányzó értékek pótlásához szükséges értékeket vagy a skálázás paramétereit – mindig **csak az adott keresztvalidációs rész tanítóadatain** számítsd ki. Ehhez használhatod például a scikit-learn `Pipeline` eszközét. A technikai azonosítókat ne tekintsd automatikusan bemeneti változóknak.

**Fontos:** Ha az előfeldolgozás vagy a modellválasztás során a validációs adatokból olyan információ kerül a tanításba, amelynek ott nem lenne helye, az torzíthatja a teljesítmény becslését. Ezt nevezzük *adatszivárgásnak*. A Kaggle tesztadatain kapott eredményt se használd a modell hiperparamétereinek hangolására.

### 2. Osztályozó modellek tanítása és a hiperparaméterek hangolása

Taníts legalább **három különböző osztályozó modellt**, a következő módszercsaládokból egyet-egyet választva:

1. **Random Forest** (véletlen erdő);
2. **Support Vector Machine (SVM)**, például `LinearSVC` vagy `SVC`;
3. **boostingalapú módszer**, például XGBoost vagy LightGBM.

Érdemes a három modellhez külön notebookokat készíteni (az SVM tanítása lassabb lehet a többi modellhez képest).
Ne elégedj meg az alapértelmezett beállításokkal: vizsgáld meg, hogyan változik a modellek teljesítménye a fontosabb hiperparaméterek módosításakor. A megfelelő beállításokat a `cs-training.csv` adatain végzett **keresztvalidációval** válaszd ki. Az osztályarányok megőrzéséhez például három- vagy ötrészes `StratifiedKFold` eljárást használhatsz. Az összehasonlíthatóság érdekében lehetőség szerint ugyanazt a validációs felosztást alkalmazd a különböző modelleknél.

A hiperparaméterek kereséséhez használhatsz például `GridSearchCV`-t, `RandomizedSearchCV`-t vagy **Optunát**. **Legalább egy modell hiperparamétereit Optunával hangold.** A beszámolóban tüntesd fel, mely paramétereket vizsgáltad, milyen értéktartományokban kerestél, melyik mérőszám alapján választottál, és végül mely beállítások bizonyultak a legjobbnak.

A számítási igényt ésszerű keretek között tarthatod. Egyes SVM-változatok nagy adathalmazon lassan taníthatók, ezért elfogadható, ha az SVM tanításához kisebb, az osztályarányokat megőrző részmintát használsz. A részmintát az adott keresztvalidációs rész **tanítóadataiból** válaszd ki, ne a validációs adatokból. Ismertesd a részminta méretét, kiválasztásának módját és az ebből eredő korlátokat. **A modelleket a címkézett adatokon végzett validáció alapján hasonlítsd össze; a Kaggle tesztadataira a kiválasztott, végleges modellel készíts előrejelzést.**

Érdemes egyszerű viszonyítási alapot is készítened, például `DummyClassifier` vagy logisztikus regresszió segítségével. Így megállapíthatod, hogy az összetettebb modellek valóban jobb eredményt adnak-e.

### 3. Együttes modell készítése (stacking)

Készíts olyan **többszintű, együttes osztályozó modellt (*stacking*)**, amely legalább két különböző alaptanuló előrejelzéseit egy további modell segítségével kombinálja.

A második szinten tanuló modell ne az alaptanulók saját tanítóadataikon készített előrejelzéseiből tanuljon, mert ez félrevezetően kedvező eredményhez vezethet. Ehelyett keresztvalidációval előállított, az adott alaptanuló tanításában nem szereplő megfigyelésekre készített előrejelzéseket használj (*out-of-fold* előrejelzések). A megvalósításhoz a scikit-learn `StackingClassifier` osztályát is választhatod.

Hasonlítsd össze az együttes modell eredményét az egyes modellekével. Vizsgáld meg, hogy a stacking javított-e az előrejelzési teljesítményen, és próbáld megmagyarázni az eredményt.

### 4. A modellek kiértékelése és a hibák elemzése

A **`cs-training.csv` címkézett adatain végzett validáció alapján** minden modellnél számítsd ki az alábbi öt mérőszámot:

- **Kiegyensúlyozott pontosság** (*balanced accuracy*);
- **Érzékenység, illetve visszahívás** (*recall*);
- **Precizitás** (*precision*);
- **F1-mérték** (*F1-score*);
- **ROC-AUC** (a ROC-görbe alatti terület).

Foglald össze az eredményeket egy, a modellek összehasonlítására alkalmas táblázatban. Az értékeléshez használhatsz olyan, keresztvalidációval előállított előrejelzéseket, amelyeknél minden megfigyelésre olyan modell készít becslést, amelynek tanításában az adott megfigyelés nem szerepelt (*out-of-fold* előrejelzések). Készíts legalább egy **tévesztési mátrixot** (*confusion matrix*) és egy **ROC-görbét** is. Mivel a két osztály aránya jelentősen eltér, érdemes a **precision–recall görbét** és az **átlagos precizitást** (*average precision, AP*) is megvizsgálnod.

A hiperparaméterek keresése közben mért teljesítmény kedvezőbb lehet a modell valódi általánosítóképességénél. Ezt vedd figyelembe az eredmények értelmezésekor. Ha pontosabb becslést szeretnél kapni a várható teljesítményről, beágyazott keresztvalidációt is alkalmazhatsz; ez nem kötelező.

Ne csak a mérőszámokat közöld, hanem azt is értelmezd, milyen hibákat követnek el a modellek. Hányszor jeleznek indokolatlanul kockázatot? Milyen gyakran nem ismerik fel a valóban kockázatos eseteket? Ha az adatok lehetővé teszik, vizsgáld meg azt is, hogy eltér-e a hibák aránya például az egyes kor- vagy jövedelemcsoportokban.

**Állítsd fontossági sorrendbe az öt kötelező mérőszámot** a hitelkockázat előrejelzése szempontjából, és indokold meg a választásodat. Térj ki arra is, milyen következményekkel járhat, ha egy kockázatos ügyfelet a modell tévesen alacsony kockázatúnak ítél, vagy fordítva.

Ha a modell **döntési küszöbét** is módosítod, azt a tanítóadatokon végzett validáció alapján válaszd meg. A Kaggle által mért ROC-AUC ugyanakkor nem egyetlen döntési küszöbtől, hanem az előrejelzett kockázati pontszámok sorrendjétől függ.

#### Az előrejelzések beküldése a Kaggle rendszerébe

A modellek fejlesztése és összehasonlítása után válaszd ki a végső modellt, majd tanítsd újra a `cs-training.csv` **teljes címkézett adathalmazán**. Ezt követően készíts előrejelzést a `cs-test.csv` valamennyi megfigyelésére.

- A Kaggle számára az **1-es osztályhoz tartozás becsült valószínűségét** add meg, ne a 0-s vagy 1-es osztálycímkét. Ha a kiválasztott modell nem ad közvetlenül valószínűségi becslést (például a `LinearSVC`), használj megfelelő valószínűségkalibrálási eljárást.
- A beküldendő `.csv` fájl szerkezete feleljen meg a Kaggle által biztosított **`sampleEntry.csv`** mintájának. Ügyelj az oszlopnevekre, a sorok számára és sorrendjére, valamint az azonosítók megfelelő kezelésére.
- **Legalább egy sikeres Kaggle-beküldés kötelező.** A kapott **ROC-AUC-pontszámot** tüntesd fel a beszámolóban, és mellékelj egy képernyőképet, amelyen a beküldés és az eredmény is jól látható.

Az eredeti verseny már lezárult, ezért az utólagos beküldésekkel nem kerülsz be a 2011-es verseny hivatalos rangsorába. A Kaggle által adott pontszám ugyanakkor lehetővé teszi, hogy a végső modell teljesítményét az általa elkülönített tesztadatokon is ellenőrizd.

**A Kaggle tesztadatain kapott pontszámot ne használd a hiperparaméterek utólagos hangolására.** A modellválasztás alapja továbbra is a címkézett tanítóadatokon végzett keresztvalidáció legyen.

### 5. Az eredmények bemutatása és dokumentálása

Készíts **legfeljebb ötoldalas írásos összefoglalót vagy rövid prezentációt**, amely önmagában is érthetően bemutatja a munkádat. A beszámolóból derüljön ki:

- milyen adatokat használtál, és hogyan készítetted elő őket;
- mely modelleket vizsgáltad, hogyan hangoltad a hiperparamétereiket, és miként ellenőrizted a teljesítményüket;
- milyen validációs eredményeket kaptál, miben különböztek a modellek, és milyen következtetésekre jutottál;
- milyen ROC-AUC-pontszámot ért el a kiválasztott modell a Kaggle rendszerében, és hogyan viszonyul ez a helyi validáció eredményéhez.

A fontosabb megállapításokat támaszd alá jól olvasható ábrákkal, például ROC-görbével, a változók fontosságát bemutató diagrammal vagy a mérőszámok összehasonlításával.

A leadott program legyen **újrafuttatható**. Ahol lehetséges, rögzítsd a véletlenszám-generálás kezdőértékét (például a `random_state` paraméterrel), és add meg a futtatáshoz szükséges csomagokat, illetve egyéb feltételeket.

## A beadás módja

A beadandót egy **Google Drive-mappára mutató, megtekintési jogosultságot biztosító hivatkozással** kell leadnod Teamsben vagy Canvasben, esetleg emailben.

A megosztott mappában a következők szerepeljenek:

- a futtatható **Jupyter- vagy Colab-jegyzetfüzet** (`.ipynb`), illetve megfelelően felépített program;
- az **írásos beszámoló PDF-változata vagy a prezentáció**;
- a Kaggle rendszerébe beküldött **előrejelzési fájl** (`.csv`), valamint egy **képernyőkép a sikeres beküldésről és a kapott pontszámról**;
- egy rövid **`README.md`**, amelyből kiderül, hogyan futtatható a program, milyen csomagokra van szükség, honnan érhető el az adathalmaz, és melyik Kaggle-beküldés tartozik a végső megoldáshoz.

Az adathalmazt nem szükséges ismét feltöltened; elegendő megadnod a letöltési helyét. Beadás előtt ellenőrizd, hogy meg tudjam nyitni a megosztott mappát és az abban található valamennyi szükséges fájlt.

## Értékelési szempontok

| Értékelési terület | Súly |
|---|---:|
| Az adatok feltárása és előkészítése | 20% |
| A modellek tanítása és a hiperparaméterek hangolása | 25% |
| A stacking megvalósítása és eredményének értékelése | 10% |
| A modellek validációja, a Kaggle-eredmény, a hibák elemzése és az ábrák | 20% |
| A dokumentáció minősége, áttekinthetősége és az újrafuttathatóság | 25% |
| **Összesen** | **100%** |

Az értékelés része a **Kaggle által közölt ROC-AUC-pontszám** és annak értelmezése, de **nem kizárólag az elért pontszám** számít. Ugyanilyen fontos, hogy a tanítás és a validáció módszertanilag helyes legyen, a választott eljárásokat meg tudd indokolni, és az eredményeket megfelelően értelmezd. A Kaggle-pontszám az eredmények értékelésére szánt, 20%-os részfeladaton belül jelenik meg; az öt értékelési terület súlya változatlan.

A munka rövid, órai bemutatásáért **külön bónuszpontok** kaphatóak.

## Ajánlott források

- [Give Me Some Credit – adathalmaz és adatleírás](https://www.kaggle.com/c/GiveMeSomeCredit/data)
- [Give Me Some Credit – a Kaggle pontozási szabályai](https://www.kaggle.com/competitions/GiveMeSomeCredit/overview)
- [Scikit-learn: gyakori módszertani hibák és az adatszivárgás elkerülése](https://scikit-learn.org/stable/common_pitfalls.html)
- [Scikit-learn: keresztvalidáció](https://scikit-learn.org/stable/modules/cross_validation.html)
- [Scikit-learn: StackingClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.StackingClassifier.html)
- [Scikit-learn: osztályozási mérőszámok](https://scikit-learn.org/stable/modules/model_evaluation.html)
- [XGBoost: Python API](https://xgboost.readthedocs.io/en/latest/python/python_api.html)
- [Optuna: hiperparaméterek keresési tartományainak meghatározása](https://optuna.readthedocs.io/en/stable/tutorial/10_key_features/002_configurations.html)

