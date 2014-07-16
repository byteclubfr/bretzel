## Utilisation

Créer un répertoire avec des fichiers .md numérotés.

* livre/001 chapitre 1.md
* livre/002 chapitre 2.md

Et gulp --src livre

Et hop un zouli livre.pdf

### Ajouter un titre de document

`DOC_TITLE="Mon titre" gulp --src livre`

### Options

* **Modifier l'orientation**
  * Paysage : `--orientation=landscape`
  * Portrait (par défaut) : `--orientation=portrait`
* **Désactiver le chapitrage automatique**
  * `--no-auto-h1`
  * Note : il faudra alors ajouter des titres H1 dans chaque slide

### Markdown

* Il s'agit du `Github Flavored Markdown` avec coloration syntaxique
* Possibilité de forcer un page-break en ajoutant `…/…` ou `.../...` dans le document
