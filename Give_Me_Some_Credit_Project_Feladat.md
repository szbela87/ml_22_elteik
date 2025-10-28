# **1. Projektfeladat: Hitelkockázat előrejelzése**

## **Feladatleírás**

A bankok kulcsszerepet játszanak a piacgazdaságban: ők döntik el, ki juthat finanszírozáshoz és milyen feltételekkel.  
A pénzügyi rendszer stabilitásához elengedhetetlen, hogy az egyének és vállalatok szükség esetén hitelt vehessenek fel.  
Ebben központi szerepet tölt be a **hitelkockázat-előrejelzés**, amely segít megítélni, hogy egy hiteligénylő mekkora valószínűséggel kerülhet pénzügyi nehézségekbe, és milyen eséllyel fogja visszafizetni a kölcsönét.

A projekt során a feladatod, hogy egy valós adathalmazon, mégpedig a Kaggle-en elérhető *“Give Me Some Credit”* dataseten dolgozz, és készíts egy modellt, amely a rendelkezésre álló adatok alapján előrejelzi, ha egy hitelfelvevő a következő két évben anyagi nehézségekkel szembesülhet.  
Az adathalmaz elérhető [itt](https://www.kaggle.com/c/GiveMeSomeCredit).

---

## **Cél**

A célod, hogy olyan modellt hozz létre, amely segíthet a hitelfelvevőknek tudatosabb pénzügyi döntéseket hozni, és időben felismerni a kockázatokat.  
Ehhez 250 000 korábbi hiteligénylő demográfiai és pénzügyi adatait használhatod fel.

---

## **Feladatok részletesen**

Az egyes alpontoknál érdemes tanulmányozni a Kaggle oldalon a Code fülön elérhető megoldásokat. A felhasznált anyagokat hivatkozni szükséges (linkkel elegendő). Ugyanígy kérem megjelölni a beadott megoldásban,
hogy mely részhez használtál generatív modellt. Ez önbevallás alapon működik, semmilyen negatív következményekkel nem jár, hiszen eleve ezen modellek használata ajánlott a megoldások elkészítéséhez, finomításához.

### 1. **Adatfeldolgozás és előkészítés**
- Tisztítsd meg az adathalmazt: kezeld a hiányzó értékeket, és végezd el a szükséges standardizálást vagy normalizálást.  
- Vizsgáld meg az egyes változók eloszlását, és kezeld a kiugró (outlier) értékeket, hogy ne torzítsák a modell teljesítményét.

### 2. **Modellek fejlesztése**
- Taníts be legalább három különböző gépi tanulási modellt, például:
  - **Véletlen erdő (Random Forest)**  
  - **SVM (Support Vector Machine)**  
  - **Legalább egy boosting algoritmus** is legyen a módszerek között, például XGBoost vagy LightGBM.  
- Optimalizáld a modellek hiperparamétereit keresztvalidációval. Például *grid search*, *random search*, *Optuna*, vagy *Hyperopt* használatával.

### 3. **Stacking alkalmazása**
- Hozz létre egy **ensemble modellt** stacking technikával, amely az egyes modellek előrejelzéseit kombinálja.  
- Hasonlítsd össze a stacking modell teljesítményét az önálló modellekével, és elemezd, hogy az egyes modellek együttműködése javítja-e az eredményt.

### 4. **Modellek értékelése és elemzése**
- Értékeld a modellek teljesítményét a következő mérőszámok alapján:
  - Kiegyensúlyozott Pontosság (*balanced_accuracy*)  
  - Érzékenység (*recall*)  
  - Precizitás (*precision*)  
  - F1-mutató  
  - AUC–ROC  
- Végezd el a következő hibaanalízist: vizsgáld meg, mely ügyféltípusok esetén teljesítenek legrosszabbul a modellek, és milyen típusú esetekben hibáznak leginkább. Készíts rövid szöveges indoklást is.
- Állíts fel egy sorrendet a fenti metrikák között aszerint, hogy a feladatnak szempontjából - véleményed szerint - mely metrika felel meg leginkább. Készíts rövid szöveges indoklást is.

### 5. **Dokumentáció és prezentáció**
- Készíts egy **legfeljebb 5 oldalas beszámolót**, vagy **prezentációt** amelyben bemutatod:
  - az adatfeldolgozás lépéseit,  
  - a modellezési folyamatot,  
  - az elért eredményeket és azok összehasonlítását.  
- Vizualizáld az eredményeidet: készíts például ROC-görbéket, *feature importance* ábrákat, vagy a teljesítménymutatók összehasonlító diagramjait.
- A dokumentáció/prezentáció bemutatása opcionális, plusz pont szerezhető vele.

---

## **Értékelési szempontok**

Az értékelés során az alábbiakat vesszük figyelembe:

- **Az adatfeldolgozás és előkészítés minősége**  
- **A modellek fejlesztésének és optimalizálásának színvonala**  
- **A stacking modell megvalósítása és teljesítménye**  
- **Az eredmények vizualizációja és értelmezése**  
- **A dokumentáció/prezentáció minősége**  
- **Bónuszpont: Kaggle – Late submission**
