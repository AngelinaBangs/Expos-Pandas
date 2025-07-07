Cet exposé a été réalisé par Oumar KOULIBALY et Angelina M'Balombe BANGOURA.

# Exposé-Pandas
 # Qu’est-ce que Pandas ?

✅ Librairie Python pour la manipulation de données.<br>
✅ Permet de travailler avec des tableaux (type Excel).<br>
✅ Très utilisée en data science et analyse de données.<br>

# Pourquoi utiliser Pandas?

✅ Manipulation facile de données (manipulation, transformation, exploration)<br>
✅ Gestion de grands volumes de données<br>
✅ Fusion, tri, filtrage, regroupement de données<br>
✅ Lecture et écriture des différents formats Excel, CSV, SQL, etc.<br>

# Cas d'utilisation
Pour pouvoir manipuler les données, il faudrait tout d’abord importer la librairie pandas. La syntaxe est la suivante:

                   Import pandas as pd
.
# 1. Chargement et exportation de données

# Lire des fichiers :
pd.read_csv('fichier.csv')<br>
pd.read_excel('fichier.xlsx')<br>
pd.read_json('fichier.json')<br>
pd.read_sql('requete SQL', connexion)<br>
pd.read_parquet('fichier.parquet')<br>

# Télécharger des fichiers :

df.to_csv('fichier.csv')<br>
df.to_excel('fichier.xlsx')<br>
df.to_json('fichier.json')<br>
df.to_sql('nom_table', connexion)<br>
df.to_parquet('fichier.parquet')<br>

# 2. Exploration et inspection des données

df.head(n)               # Affiche les premières lignes<br>
df.tail(n)               # Affiche les dernières lignes<br>
df.info()                # Infos sur le DataFrame<br>
df.describe()            # Statistiques descriptives<br>
df.shape                 # (n_lignes, n_colonnes)<br>
df.columns               # Liste des colonnes<br>
df.index                 # Index du DataFrame<br>
df.dtypes                # Types de données des colonnes<br>
df.memory_usage()        # Utilisation mémoire<br>

# 3. Sélection et filtrage

df['colonne']            # Accès à une colonne<br>
df[['col1', 'col2']]     # Accès à plusieurs colonnes<br>
df.loc[ligne, colonne]   # Accès par étiquette<br>
df.iloc[i, j]            # Accès par position<br>
df[df['col'] > 5]        # Filtrage conditionnel<br>
df.query('col > 5')      # Filtrage avec query<br>

# 4. Nettoyage et préparation des données

df.dropna()                      # Supprime les lignes avec NaN<br>
df.fillna(valeur)               # Remplace les NaN<br>
df.isnull()                     # Détection des NaN<br>
df.duplicated()                 # Détection des doublons<br>
df.drop_duplicates()            # Supprime les doublons<br>
df.replace(val1, val2)          # Remplace des valeurs<br>
df.rename(columns={'a':'b'})    # Renomme les colonnes<br>
df.astype({'col': type})        # Conversion de types<br>
df.apply(fonction)              # Applique une fonction<br>
df.map(fonction)                # Sur une série<br>

# 5. Manipulation de colonnes

df['nouvelle'] = df['col1'] + df['col2']   # Création de colonne<br>
df.drop('colonne', axis=1)                 # Supprime une colonne<br>
df.insert(0, 'col', valeurs)               # Insère une colonne<br>
df.rename(columns={'a': 'b'})              # Renommer colonne<br>

# 6. Opérations sur les données

df.sum()                      # Somme par colonne <br>
df.mean()                     # Moyenne<br>
df.median()<br>
df.std()                      # Écart-type<br>
df.min(), df.max()<br>
df.cumsum(), df.cumprod()<br>

# 7. Groupement et agrégation

df.groupby('colonne')                      # Groupement<br>
df.groupby('col').agg({'col2':'sum'})      # Agrégation multiple<br>
df.pivot_table(index='a', columns='b', values='c', aggfunc='sum')  # Tableau croisé<br>

# 8. Fusion, jointures et concaténation

pd.concat([df1, df2], axis=0)              # Concaténation verticale<br>
pd.merge(df1, df2, on='colonne')           # Jointure SQL<br>
df1.join(df2, how='left')                  # Join sur index<br>

# 9. Tri et réindexation

df.sort_values(by='colonne')              # Tri par valeur<br>
df.sort_index()                           # Tri par index<br>
df.reset_index()                          # Réinitialise l’index<br>
df.set_index('colonne')                   # Définit une colonne comme index<br>

# 10. Dates et temps

pd.to_datetime(df['date'])               # Conversion en datetime<br>
df['date'].dt.year, .dt.month, .dt.day   # Extraction des composantes<br>
df['date'].dt.weekday                    # Jour de la semaine<br>
df.set_index('date')                     # Utilisation comme index<br>

# Cas Pratique
Chargement du Data Set Voiture pour la manipulation des fonctions citées ci-haut
-  Filtrer les données par condition
- Calculer des moyennes ou des totaux
- Exporter le résultat etc...

# Conclusion
Pandas simplifie la manipulation de données
Utile pour les rapports et l’automatisation
Indispensable pour les data analysts et développeurs







