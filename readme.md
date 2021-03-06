# Configurez votre GitHub

Attention, ceci n'est pas un dépôt que vous devez utiliser pour votre projet, juste un tutoriel pour vous aider à configurer vos projets.

Vous vous inscrivez sur [GitHub](https://github.com/).

Vous créez un nouveau projet `CSTwitterAnalysis`.

Configurez ensuite git sur votre machine. Pour cela, ouvrez une ligne de commande (votre console git sous windows ou votre terminal sur Linux/Mac) et exécutez :

	git config --global user.email "you@example.com"
	git config --global user.name "Your Name"

Il faut utiliser l'adresse email avec laquelle vous vous êtes inscrits sur github.

Si ce n'est pas déjà fait, vous créez une clef ssh dans votre dossier `~/.ssh` :

	ssh-keygen -t ed25519

Pas besoin de rentrer d'e-mail, il est conseillé d'indiquer une passphrase (mot de passe permettant de protéger votre clef privée). Pour le reste, ne rien écrire et appuyer sur `entrée` plusieurs fois.

Le binôme doit également créer une clef ssh de la même manière.

Ensuite vous copiez votre clef publique (qui peut être affichée avec `cat ~/.ssh/id_ed25519.pub`) et vous l'ajoutez comme clef sur votre compte github en utilisant le site web (dans `settings` puis `keys`...).

Votre binôme ajoute de la même manière sa clé sur son propre compte. Chaque membre du binôme a donc sa clef et ajoute sa clef sur son propre compte github.

En ligne de commande (sur votre console git sous windows ou votre terminal sur Linux/Mac) vous allez dans le dossier de votre projet local s'il existe.

S'il n'existe pas ou que vous voulez refaire tout depuis le début créez un nouveau dossier et faites un `git init` (en ligne de commande) en étant dedans.

Exemple :

	cd C:/mon/projet
	git init

Ensuite vous ajoutez le dépôt sur les serveurs github (remplacez "hayj" par votre username) :

	git remote add origin git@github.com:hayj/CSTwitterAnalysis.git

Si cela ne marche pas c'est que vous avez déjà un remote donc vous devez le changer avec :

	git remote set-url origin git@github.com:hayj/CSTwitterAnalysis.git

Si ce n'est pas déjà fait vous faites le premier commit (qui créé une mise à jour local) :
	
	git add .
	git commit -m "first commit"

Ensuite vous faites le premier push qui permet d'envoyer les mises à jour sur GitHub:

	git push origin master

Attention, si votre push ne fonctionne pas, vous devez ajouter l'option `f` mais cela écrasera ce qu'il y a sur GitHub par ce que vous avez en local :

	git push -f origin master

Vous invitez votre binôme dans le projet sur le site web GitHub. Vous devez également inviter votre encadrant (pour moi ce sera hayj, et Hajar c'est Hajarosy).

Votre binôme doit faire un clone sur son pc :

	git clone git@github.com:hayj/CSTwitterAnalysis.git

Si vous n'avez pas encore le projet sur pycharm, vous pouvez simplement ouvrir le dossier, puis créer des packages et module...

La création de branche est facultative, créer des branches permet de mieux travailler en binôme, de faire des merges plus facilement. Mais sinon contentez-vous des commit push pull si vous avez du mal à faire vos branches...

Chaque membre du binôme doit faire une branche.

Binome1 fait :

	git checkout -b branche1

Binome2 fait :

	git checkout -b branche2

Régulièrement, vous devez faire des `commit` et de temps en temps merger sur la branche master pour que les encadrants puissent voir le travail effectué.

Par example binome1 fait :
	
	git checkout master # pour retourner sur la branche master
	git pull # pour récupérer les dernières mise à jour de master
	git merge branche1 # pour merger master et branche1
	git push origin master # pour tout envoyer sur github
	git checkout branche1 # pour retourner sur votre branche

# Enregistrez vous sur Twitter

 * Vous vous inscrivez sur Twitter
 * puis en tant que développeur https://developer.twitter.com
 * Dans le formulaire vous expliquez que vous travaillez pour du sentiment analysis et trend analysis pour un projet en cours etc