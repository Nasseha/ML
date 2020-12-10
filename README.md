# Big data sous python - Digit Recognizer
Ariinui TERIITEHAU et Nasseha SAID-SALIM.  
Notre projet se trouve dans le fichier zip à télécharger digit.recognizer.zip 
https://www.kaggle.com/c/digit-recognizer 




Vagrant file 

# Big Data sous python 
Vérifier le vagrant file si les paramètres sont adaptés à la machine 

Utiliser le notebook dans le cas ou ca fonctionne pas le rendu_python.py

Ne pas oublier de changer les path dans le codage "Rapport_final.ipynb" ! 


## Python avec VirtualBox+Vagrant

Pour éviter tout problème d'installation sur votre machine, nous avons mis en place des machines virtuelles Vagrant.
Vagrant permet d'avoir une machine de petite taille (< 800 Mb) et un environnement préconfiguré. Les instructions sont les suivantes :

- Installer VirtualBox : https://www.virtualbox.org/
- Installer Vagrant : https://www.vagrantup.com/

- ouvrez un utilitaire de commande, aussi connu sous le nom de 'terminal', pointant dans ce dossier (voir les instructions de votre système d'exploitation sur internet), puis tapez les commandes suivantes :

Il y a déjà un Vagrantfile pré-remplie dans le fichier 
```
$ vagrant init nasseha_ariinui_big_data
$ vagrant up 
$ vagrant ssh
```

- Vous devriez être maintenant dans la machine virtuelle, rien d'autre ne va s'ouvrir, l'interface n'est pas graphique. Si cela a marché, vous devriez voir maintenant dans le terminal les lignes suivantes:
```
Welcome to Ubuntu 20.04.1 LTS (GNU/Linux 5.4.0-51-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Wed Oct 28 11:10:43 UTC 2020

  System load:  0.27              Processes:               119
  Usage of /:   4.7% of 38.71GB   Users logged in:         0
  Memory usage: 17%               IPv4 address for enp0s3: 10.0.2.15
  Swap usage:   0%

  8 updates can be installed immediately.
  8 of these updates are security updates.
  To see these additional updates run: apt list --upgradable

  Last login: Wed Oct 28 10:36:09 2020 from 10.0.2.2
  vagrant@ubuntu-focal:~$
```

Il faut maintenant amener le système Vagrant dans le dossier de travail partagé entre votre machine physique et la machine virtuelle, en tapant dans le terminal:
```
vagrant@ubuntu-focal:~$ cd /vagrant
```

installer les package et python dans le virtual box
$ sudo apt-get update
$ sudo apt-get install python3-virtualenv virtualenv python python3
$ sudo apt-get install gcc g++ python3-dev

$ virtualenv --python=python3 venv
$ . venv/bin/activate                   # N'oubliez pas le "." au début.
$ pip install -r requirements.txt

Vous pouvez donc faire tourner votre code Python en tapant :
```
vagrant@ubuntu-focal:~$ python3 rendu_python.py
```




