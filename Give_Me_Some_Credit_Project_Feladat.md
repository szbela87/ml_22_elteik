
# Projektfeladat: Hitelkockázat előrejelzése a "Give Me Some Credit" Kaggle adathalmaz alapján

## Feladatleírás
A bankok kulcsszerepet játszanak a piacgazdaságok működésében, mivel ők döntik el, ki férhet hozzá finanszírozáshoz, és milyen feltételekkel. 
A pénzügyi piacok és a társadalom stabil működéséhez elengedhetetlen, hogy az egyének és a vállalatok hitelhez juthassanak, amikor szükségük van rá. 
Ennek egyik fő eszköze a **hitelkockázat-előrejelzés**, amely a bankok számára lehetővé teszi annak meghatározását, hogy egy adott hiteligénylő 
milyen valószínűséggel kerül anyagi nehézségekbe, és ezáltal milyen eséllyel fizeti vissza a kölcsönét.

A projekt során a hallgatóknak az iparágban használt hitelkockázati modellek fejlesztésében és finomításában kell versenyezniük. 
Cél egy olyan algoritmus létrehozása, amely a rendelkezésre álló adatok alapján minél pontosabban meg tudja jósolni, hogy egy hitelfelvevő 
mekkora eséllyel kerül pénzügyi nehézségekbe a következő két év során. Az adathalmaz linkje [itt](https://www.kaggle.com/c/GiveMeSomeCredit) található.

## Projekt célja
Az elkészítendő modell segítséget nyújthat a hitelfelvevők számára, hogy a legjobb pénzügyi döntéseket hozhassák meg, és előre láthassák 
esetleges pénzügyi kockázataikat. Ehhez a modellhez a hallgatók 250,000 korábbi hiteligénylő adatait használhatják fel, amely tartalmazza az 
egyes hitelfelvevők demográfiai és pénzügyi adatait.

## Részletes feladatok

1. **Adatfeldolgozás és előkészítés:**
   - Az adathalmaz megtisztítása: kezelje a hiányzó adatokat, és végezze el a szükséges adatstandardizálást vagy normalizálást.
   - Vizsgálja meg a változókat, és szükség esetén kezelje az outliereket, hogy azok ne torzítsák a modell eredményeit.

2. **Modellek fejlesztése:**
   - Tanítsa be az alábbi gépi tanulási modelleket: véletlen erdő (Random Forest), SVM (Support Vector Machine), valamint legalább egy boosting algoritmus (például XGBoost vagy LightGBM).
   - Optimalizálja a modellek hiperparamétereit keresztvalidáció segítségével (pl. grid search vagy random search módszerekkel, vagy hyperopt, esetleg optuna könyvtárakkal).

3. **Stacking alkalmazása:**
   - Készítsen egy ensemble modellt, amely az egyes modellek együttes teljesítményére épít stacking technika alkalmazásával.
   - Hasonlítsa össze a modell teljesítményét az önálló modellek teljesítményével, hogy megállapítható legyen az egyes algoritmusok közti együttműködés hatása.

4. **Modellek értékelése és elemzése:**
   - A modell teljesítményét a következő mérőszámok alapján értékelje: pontosság (accuracy), érzékenység (recall), pontosság (precision), F1-mutató és AUC-ROC mutató.
   - Végezzen hibaanalízist, és elemezze, hogy a modellek mely ügyféltípusoknál teljesítenek a legrosszabbul, illetve hogy milyen típusú esetekben hibáznak leginkább.

5. **Dokumentáció és prezentáció:**
   - Készítsen rövid (<=5 oldal) dokumentációt a projekt során elvégzett lépésekről, beleértve az adatfeldolgozást, a modellezést és az eredmények összehasonlítását.
   - Az eredményeket vizualizálja (pl. ROC-görbék, feature importance ábrák), és mutassa be a teljesítménymutatók összehasonlító diagramjait.

## Értékelési szempontok
Az értékelés során figyelembe vett szempontok:
- **Adatfeldolgozás és előkészítés minősége**
- **Modellek fejlesztése és optimalizálása**
- **Stacking modell megvalósítása és teljesítménye**
- **Eredmények vizualizációja és a teljesítménymutatók elemzése**
- **Dokumentáció és a bemutató minősége**

