---
layout: post
title:  "Mettre en forme en sauvegardant avec VS Code et HTML"
date:   2021-11-01 01:00:00 +0200
categories: vs-code formater prettier sauvegarder
---

# Introduction

Bonjour, dans cet article je vais essayer de vous expliquer comment mettre en forme (formater) votre code HTML à l'aide de l'éditeur de texte VS Code automatiquement en sauvegardant votre document ".html" avec les touches "Ctrl + s".

# Installation et configuration de l'extension Prettier

Pour configurez VS Code, suivez les étapes ci-dessous:

- Lancez VS Code et cliquez sur l'onglet "Extensions" du menu de gauche.
- Dans le champs de recherche entrez : "Prettier"
- Installer l'extension qui se nomme  "Prettier - Code formatter" (un reload de VS Code est peut-être nécessaire)
- Rendez-vous dans les paramètres de l'extension ( cliquez sur le bouton engrenage à droite des boutons d'installations et d'activation de l'extension, puis cliquez sur "paramètres d'extension")
- Une fois dans les paramètres, faites un "Ctrl + f" et tappez "On save" dans le champs de recherche
- Cliquez, dans la rubrique "Editor: Code Actions On Save", sur le lien "Modifier dans settings.json", vous aurez accès au fichier de configuration de VS Code
- Ajouter ces lignes au fichier de configuration : 
```json
"[html]":{
        "editor.formatOnSave": true,
    }
```

- Ouvrez un fichier ".html" ou créez en un pour tester si vous n'en avez pas
- Mettez y du code non formaté dedans, par exemple : 

```html
<!-- Menu de navigation du site --><ul class="navbar"><li><a href="index.html">Home page</a><li><a href="reflexions.html">Réflexions</a><li><a href="ville.html">Ma ville</a><li><a href="liens.html">Liens</a></ul><!-- Contenu principal --><h1>Ma première page avec du style</h1><p>Bienvenue sur ma page avec du style! <p>Il lui manque des images, mais au moins, elle a du style. Et elle a desliens, même s'ils ne mènent nulle part...&hellip;<p>Je devrais étayer, mais je ne sais comment encore.<!-- Signer et dater la page, c'est une question de politesse! --><address>Fait le 5 avril 2004<br>par moi.</address>
```

- Faites un clic droit dans le document ".html" ou vous avez ajouté le code ci-dessus, et cliquez sur : "Mettre en forme le document avec ..."
- Choisissez l'extension "Prettier - Code formatter"

Voila, normalement vous devez avoir un code formaté comme dans l'exemple ci-dessous : 


```html
		<!-- Menu de navigation du site -->
		<ul class="navbar">
			<li><a href="index.html">Home page</a></li>
			<li><a href="reflexions.html">Réflexions</a></li>
			<li><a href="ville.html">Ma ville</a></li>
			<li><a href="liens.html">Liens</a></li>
		</ul>
		<!-- Contenu principal -->
		<h1>Ma première page avec du style</h1>
		<p>Bienvenue sur ma page avec du style!</p>
		<p>
			Il lui manque des images, mais au moins, elle a du style. Et elle a
			desliens, même s'ils ne mènent nulle part...&hellip;
		</p>
		<p>
			Je devrais étayer, mais je ne sais comment encore.<!-- Signer et dater la page, c'est une question de politesse! -->
		</p>
		<address>Fait le 5 avril 2004<br />par moi.</address>
```

Si maintenant, vous faites un "Ctrl + s", votre code HTML se formatera automatiquement.

N'hésitez pas à me laisser un petit commentaire si ça ne fonctionne pas ou que vous bloquez quelque part, merci d'avance !
