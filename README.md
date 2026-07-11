# Klasterovanje fudbalera i analiza odnosa cene i kvaliteta

## Opis projekta

Ovaj projekat predstavlja analizu podataka o profesionalnim fudbalerima primenom tehnika mašinskog učenja bez nadzora (unsupervised learning). Cilj projekta je identifikacija karakterističnih grupa igrača, kao i izdvajanje potencijalno isplativih investicija na osnovu njihovih performansi i tržišne vrednosti.

U okviru projekta izvršene su sledeće faze:

- upoznavanje sa skupom podataka i analiza njegovih karakteristika,
- čišćenje i priprema podataka,
- spajanje više tabela u jedinstven skup atributa,
- konstrukcija novih opisnih atributa za igrače,
- obrada nedostajućih vrednosti,
- kodiranje kategoričkih atributa,
- redukcija dimenzionalnosti primenom PCA,
- primena više algoritama klasterovanja:
  - K-Means
  - Gaussian Mixture Models (GMM)
  - Hijerarhijsko klasterovanje
  - Spectral Clustering
  - DBSCAN
- poređenje rezultata primenom različitih metrika kvaliteta klasterovanja,
- analiza dobijenih klastera,
- izdvajanje potencijalnih "value for money" igrača na osnovu tržišne vrednosti, minutaže i drugih statističkih pokazatelja,
- vizuelizacija rezultata klasterovanja.

---

## Struktura projekta

```
data/
    raw/            # originalni skupovi podataka
    processed/      # obrađeni skupovi podataka

notebooks/
    01_preprocessing.ipynb
    02_feature_engineering.ipynb
    03_feature_reduction.ipynb
    04_clustering.ipynb
    05_more_specific_clustering.ipynb
    06_cluster_visualization.ipynb
```

---

## Pokretanje projekta

### 1. Kloniranje repozitorijuma

```bash
git clone <url-repozitorijuma>
cd <ime-projekta>
```

---

### 2. Kreiranje virtuelnog okruženja

Linux / macOS

```bash
python3 -m venv venv
```

Windows

```bash
python -m venv venv
```

---

### 3. Aktivacija virtuelnog okruženja

Linux / macOS

```bash
source venv/bin/activate
```

Windows

```cmd
venv\Scripts\activate
```

---

### 4. Instalacija zavisnosti

```bash
pip install -r requirements.txt
```

---

### 5. Pokretanje Jupyter Notebook-a

```bash
jupyter notebook
```

ili

```bash
jupyter lab
```

Nakon pokretanja otvoriti notebook-ove redom, počevši od:

```
01_preprocessing.ipynb
```

Svi naredni notebook-ovi koriste rezultate prethodnih koraka.

---

## Korišćene biblioteke

- pandas
- numpy
- matplotlib
- scikit-learn
- scipy
- jupyter

---

## Napomena

Pre pokretanja projekta potrebno je da se originalni skup podataka nalazi u direktorijumu:

```
data/raw/
```

Obrađeni skupovi podataka i rezultati klasterovanja automatski se čuvaju u direktorijumu:

```
data/processed/
```
