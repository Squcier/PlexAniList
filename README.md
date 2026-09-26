# PlexAniList

<p align="center">
  <strong>Synchronise automatiquement ta progression Plex avec AniList.</strong><br>
  Une interface Web locale simple pour relier tes séries Plex à AniList et garder ta liste à jour sans saisie manuelle.
</p>

<p align="center">
  <a href="https://github.com/Squcier/PlexAniList/raw/refs/heads/main/PlexAniList.zip"><strong>⬇️ Télécharger PlexAniList</strong></a>
  ·
  <a href="#installation">Installation</a>
  ·
  <a href="#fonctionnalités">Fonctionnalités</a>
</p>

---

## 🎬 Plex + AniList, enfin synchronisés

Tu regardes tes anime sur Plex mais tu dois ensuite ouvrir AniList pour mettre à jour chaque épisode à la main ? **PlexAniList s'en charge pour toi.**

L'application surveille la progression de lecture sur Plex, identifie l'anime et la saison correspondants, puis met à jour automatiquement ta progression sur AniList.

Tout se configure depuis une **interface Web locale** accessible dans ton navigateur. Aucune donnée Plex ou AniList n'a besoin d'être hébergée sur un service tiers.

## ✨ Fonctionnalités

- **Synchronisation Plex → AniList** de la progression des épisodes.
- **Interface Web locale** claire pour gérer le logiciel.
- **Scan des bibliothèques Plex** et choix des bibliothèques à synchroniser.
- **Mapping automatique Plex ↔ AniList** avec possibilité de vérifier ou corriger les correspondances.
- **Recherche manuelle AniList** lorsqu'une série ne peut pas être reconnue automatiquement.
- **Gestion saison par saison**, avec offsets positifs ou négatifs pour les numérotations particulières.
- **Plusieurs comptes AniList** : une même saison peut mettre à jour plusieurs comptes.
- **Actions en masse** pour gérer plus rapidement une grande bibliothèque.
- **Scan et recherche automatique périodiques** configurables.
- **Seuil de progression configurable** avant de considérer un épisode comme vu.
- **Synchronisation à la pause** et complétion automatique configurables.
- **Historique de synchronisation** avec conservation des événements récents.
- **Import / export de sauvegarde** de la configuration.
- **Base de données locale SQLite** créée automatiquement.

## ⬇️ Téléchargement

### Version prête à extraire

**[Télécharger PlexAniList.zip](https://github.com/Squcier/PlexAniList/raw/refs/heads/main/PlexAniList.zip)**

Décompresse simplement l'archive dans le dossier de ton choix.

> PlexAniList est actuellement prévu principalement pour une utilisation locale sous Windows.

## 🚀 Installation

### 1. Installer Python

Installe une version récente de **Python 3** si ce n'est pas déjà fait.

Pendant l'installation sous Windows, pense à activer l'option permettant d'ajouter Python au `PATH`.

### 2. Installer les dépendances

Ouvre un terminal dans le dossier extrait puis exécute :

```bash
python -m pip install -r requirements.txt
```

### 3. Lancer PlexAniList

Sous Windows, double-clique sur :

```text
PlexAniList.vbs
```

Le logiciel démarre discrètement en arrière-plan, sans laisser de console Python ouverte.

Ouvre ensuite :

```text
http://127.0.0.1:6060
```

Tu peux également lancer manuellement l'application :

```bash
python app.py
```

## ⚙️ Configuration

Dans **Paramètres**, renseigne :

1. l'adresse de ton serveur Plex ;
2. ton token Plex ;
3. ton ou tes comptes AniList ;
4. les options de synchronisation souhaitées.

Teste les connexions depuis l'interface, puis rends-toi dans **Bibliothèques** pour choisir celles qui doivent être prises en compte.

Dans **Mapping**, scanne ensuite ta bibliothèque et vérifie les correspondances entre tes séries Plex et AniList.

Une fois le mapping terminé, PlexAniList peut gérer la progression automatiquement.

## 🧩 Mapping intelligent

Les noms et découpages de saisons entre Plex et AniList ne correspondent pas toujours parfaitement. Parce qu'apparemment numéroter des épisodes de manière cohérente aurait été trop simple.

PlexAniList permet donc de :

- rechercher automatiquement les saisons non liées ;
- choisir manuellement une entrée AniList ;
- réassigner une correspondance incorrecte ;
- ignorer certaines séries ;
- supprimer plusieurs mappings à la fois ;
- définir un **offset par saison** lorsque la numérotation Plex diffère de celle d'AniList ;
- associer une saison à **un ou plusieurs comptes AniList**.

## 🔒 Données et confidentialité

La configuration et les mappings sont conservés **localement**.

Au premier démarrage, PlexAniList crée automatiquement :

```text
PlexAniList.db
.secret_key
```

Ces fichiers contiennent des données propres à ton installation et ne doivent pas être partagés publiquement.

Tes tokens Plex et AniList restent dans ton installation locale.

## 🛠️ Technologies

PlexAniList utilise notamment :

- Python
- Flask
- SQLAlchemy / SQLite
- Waitress
- API Plex
- API AniList

## 📌 État du projet

PlexAniList est un projet en développement. Des ajustements peuvent encore être nécessaires avec certaines bibliothèques, conventions de nommage ou structures de saisons.

Si tu rencontres un problème, indique idéalement la série concernée, sa structure dans Plex et le résultat attendu côté AniList.

---

<p align="center">
  <strong>Moins de mises à jour manuelles. Plus de temps pour regarder tes anime.</strong>
</p>
