## Utilisation

Créer un répertoire avec des fichiers .md numérotés.

* livre/001 chapitre 1.md
* livre/002 chapitre 2.md

Et gulp --src livre

Et hop un zouli livre.pdf

### Ajouter un titre de document

`DOC_TITLE="Mon titre" gulp --src livre`

### Modifier l'orientation

Paysage : `gulp --landscape --src livre`

Portrait (par défaut) : `gulp --portrait --src livre`
