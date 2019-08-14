# emprisonnement
Script Bash pour gérer (créer, rentrer et supprimer) des 'prisons' (chroot). 

# [0] Information importante 

Sans précision sur le mode verbeux ou non, par défaut, toutes les opérations seront acceptées sans demande de confirmation. 

# [1] Cas d'usage 

'emprisonnement' se lance comme un script Bash classique, avec les arguments potentiels suivants : 

[-a 'action'] [-d 'dossier_cible'] [-c 'commandes_cibles'] [-v]

... où 'action' est l'action à mener 
- 'aider' (par défaut), 
- 'automatiser', 
- 'creer', 
- 'supprimer', 
- 'rentrer' [-s 'commande'], 
- 'credit' 

... où 'commandes_cibles' est la liste des commandes supplémentaires à rendre disponibles ('bash env ls cat more groups' par défaut) 

... où 'dossier_cible' est le dossier d'emprisonnement 

... où l'argument '-v' est le mode verbeux (mode 'log') 

... où 'commande' peut être une commande Bash ou un script à emprisonner 

# [2] Intérêt 

Ce programme produira une prison dédiée à un environnement contrôlé. En dehors des actions d'aide et d'affichage du crédit, les droits 'root' sont nécessaires. 

# [3] Crédit, version et licence 

- version 0.0.1 (fonctionnel) 
- par Julien Garderon, août 2019 
- GNU GPL 3+ (monde) ou CeCILL 2+ (France) 

# [4] Exemples 

(créer la prison) 

./emprisonner -a creer -d ./prison 

(supprimer la prison) 

./emprisonner -a supprimer -d ./prison 

(rentrer dans la prison) 

./emprisonner -a rentrer -d ./prison 


