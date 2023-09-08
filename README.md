# lab_ansible

## Ojectif:

Adaptez votre playbook afin qu'il s'adapte à l'Amazon Machine Image, ET aux machines virtuelles déployées par ce vagrantfile.

## Faites attention

Récupérez le "fact" vous donnant l'OS sur lequel le système est déployé.

Il faudra stocker cette information dans une variable et une condition.

le gestionnaire de paquets utilisé va être différent pour un système basé sur debian.

Les chemins de configuration vont être différents pour le serveur apache.

## Utilisation

Le vagrantfile utilise virtualbox comme provider. Si vous avez un souci avec son utilisation n'hésitez pas à me solliciter.

Pour se connecter aux machines:

    Controller: vagrant ssh controller
    Managed node 1: vagrant ssh m1
    Managed node 2: vagrant ssh m2


`git clone https://github.com/Mossbaddi/lab_ansible`

`cd lab_ansible`

`vagrant up`


Pour stopper les machines: `vagrant halt`

Pour DETRUIRE LES MACHINES: `vagrant destroy`

N'hésitez pas à relancer plusieurs fois le up, et utilisez vagrant status pour connaitre l'état de machine. Vous pourrez le voir sur l'interface de virtualbox également. Il peut arriver que le boot des trois machines du premier coup pose problème, sur mon poste également donc je vous le fais savoir.


### Side note:

En faisant ce TP bonus, vous apprendrez beaucoup sur ansible et aurez déjà une idée de ce à quoi peut ressembler un playbook avancé! N'hésitez surtout pas à bien consulter la documentation et vous documenter sur les modules disponibles, les fonctionnalités d'ansible. Comme d'habitude, plusieurs routes mènent à Rome, et il y en a toujours une qui est mieux pavée que les autres. 

### TEST VAGRANT PERSO
ligne de commande : 
cd ~/.ssh
ssh-keygen -t rsa #genere cle rsa 
ssh-copy-id -i id_rsa vagrant@managed1 # mdp : vagrant

