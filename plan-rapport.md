# Introduction présentation de Cranelift
- Compilateur JIT pour Webassembly (et éventuellement Rust).
- Rappeler les buts du projet : contribuer à un vrai compilateur, apprendre un nouveau langage impliquant de nouveaux concepts, participer à un projet open source.

# Les tâches effectuées
- Rappel du cahier des charges :
	- Résoudre des bugs pour s'échauffer.
	- Écrire des passes d'optimisation.
- Ce qui a été fait :
	- Résolution d'un bug, intégration d'une PR.
	- Passes d'optimisation non faite pour travailler sur un nouvel allocateur de registre :
		- Parler de l'état actuel de l'allocation de registres ? Quelles sont les particularitées de cet allocateur ?
		- Remplacement Set par BitSet pour de meilleures performances.
			- Premiers essais d'un BitSet générique avec spécialisation pour Registre, pourquoi ça a pas marché.
			- Changement de méthode, écriture d'une spécialisation pour les registres (RegSet).
			- Écriture de tests unitaires qui effectuent un grand nombre d'opération sur les RegSet.
			- Techniques pour trouver des bugs :
				- Coverage.
				- Avec un debugger.
				- ce qu'on aurait pu mieux faire : TDD etc.
			- Comment s'occuper d'un bug quand on en a trouvé un.
			- Optimisation (profiling, callgrind).
			- Ce qu'on aurait pu mieux faire ?
# Contribution à un projet open source
- Organisation de Mozilla :
	- Outils : Riot/Matrix, Git, Github.
	- Travail en "remote".
- Notre organisation :
	- Fréquence réunions.
	- Répartition travail, fonctionnement de nos dépots).
	- Ce qu'on pourrait mieux faire
		- alterner quand on travaille sur des tâches différentes.
- Processus d'ajout d'une fonctionnalité :
	- Les issues.
	- Pull request.
	- Revue de code.
- Git : 
	- Travailler sans faire de merge conflict.
		- Utilité : facilite bisect ?
	- Quelques commandes qu'on a appris rebase, squash, bisect, cherry-pick.
- Bonnes pratiques :
	- Pour faciliter la revue de code.
	- Pour la "maintenance du projet".
		- la façon de faire un commit (message du commit).
# Apprentissage du langage Rust
- Secteur et contexte du langage (concurrents, rapide historique), particularités du langage (borrow checker, lifetimes, langage non orienté objet).
- Avantages (à développer ?) :
	- Empêche les erreurs type double-free, use after free etc.
	- Mécanisme de gestion de la mémoire similaire au RAII en C++ donc pas de garbage collector).
- Environnement et outils utiles au projet (cargo, fmt, clippy).
- Difficultés rencontrées ?

