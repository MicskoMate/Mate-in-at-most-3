# Python_chess_puzzle_solver:
## Projekt neve: Mate_in_at_most_3
## Projektet készítette:
Micskó Máté és Szabó Máté
## Futtatáshoz szükséges:
-Python

-chess library (pip install chess)
## Feladat leírása:
A projekt célja egy olyan sakkfeladvány megoldó elkészítése volt, amely képes befogadni, illetve feldolgozni és megoldani a legfeljebb 3 lépéses matt feladványokat. Maga a solver egy Jupyter-notebook, amiben az első néhány cella különböző segédfüggvényeket tartalmaz, amik beleépülnek egy nagy solver függvénybe. A notebookban kommentek formájában részletes leírás található egyes függvények és változók funkciójáról, szerepéről, valamint próbáltunk olyan neveket adni ezeknek, amik segítik a könnyű megértést.
## Használati útmutató:
Mielőtt használni akarja a solvert bizonyosodjon meg róla, hogy minden cellát lefuttat, különben a solver a függényeket nem fogja tudni majd használni. Ezek lefuttatása után a követekező módon tudja egy adott sakkfeladványra (amely legfeljebb 3 lépésből matt) a megoldást megkapni: Nyisson egy új cellát és az alábbi kódot másolja be, valamint döntse el, hogy a lépéseket mely kritériumok szerint szeretné pontozni (4 db bool argumentum). Ezek után a feladvány fen kódját a kettőspontok közé másolja be és futtassa. Az output egy olyan lista, aminek az első eleme a megoldás első lépése, a második pedig egy lista, amiben listákban fel van sorolva az összes lehetséges kimenetel, attól függően, hogy az ellenfél mit lép. A nootebook legvégén van egy függvény, ami a solver outputját kiprinteli a táblás állással. A kommentbe rakott %%time csupán érdekességként van ott, ki lehet venni a kommentből, hogy megnézzük a különböző hívásokra mennyi időbe telik a feladat megoldása (például a brute force sokkal lassabb, mint egy okosabb megközelítés). A példaként megadott kódra például az alatta található lépéssorozatot fogja kiadni a solver (a notebookban további példák is találhatók):
```python
#%%time
board = chess.Board("r1b1kb1r/pppp1ppp/5q2/4n3/3KP3/2N3PN/PPP4P/R1BQ1B1R b kq - 0 1")
display(board)
puzzle_solver("r1b1kb1r/pppp1ppp/5q2/4n3/3KP3/2N3PN/PPP4P/R1BQ1B1R b kq - 0 1", True, True, True, True)
```
   ```python
 [Move.from_uci('f8c5'),
 [[Move.from_uci('d4c5'),
   Move.from_uci('f6b6'),
   Move.from_uci('c5d5'),
   Move.from_uci('b6d6')]]]
```
## Teszteléshez további linkek:
-mate in 2: https://wtharvey.com/m8n2.txt

-mate in 3: https://wtharvey.com/m8n3.txt"
