# Answers

Nom : Delloye
Prénom : Georges

# 1.
Qu'est-ce qu'une instance EC2 ?

Elastic Compute Cloud (EC2) est un service proposé par AWS permettant à des tiers de louer des serveurs sur lesquels exécuter leurs propres applications web.

EC2 permet un déploiement extensible des applications en fournissant une interface web par laquelle un client peut créer des machines virtuelles sur lesquelles le client peut charger n'importe quel logiciel de son choix. Un client peut créer, lancer, et arrêter des instances de serveurs en fonction de ses besoins, et payer en fonction du temps d'usage des serveurs, d'où le terme d'« Élastique ». Un client peut mettre en place des instances de serveurs isolées physiquement (qui ne s'exécutent pas sur le même serveur physique) les unes des autres, de telle façon qu'en cas de panne, il soit possible de restaurer les instances défaillantes et d'assurer la continuité du service.

# 2.
Qu'est-ce qu'un VPC ?

Un Virtual Private Cloud (VPC) est un groupe de ressources informatiques configurables à la demande dans un environnement de cloud public, qui fournit un certain niveau d'isolement entre les différentes organisations qui utilisent ces ressources. L'isolation entre le VPC et les autres utilisateurs du cloud est habituellement obtenue par l'utilisation d'un sous-réseau IP et d'un mécanisme de communication virtuel (VLAN) pour chaque utilisateur.

Dans un VPC, le mécanisme décrit ci-dessus pour fournir une isolation dans le cloud, est complété par un service de VPN (pour chaque utilisateur) qui garantit la sécurité de l'accès des utilisateurs à distance aux ressources, grâce à un système d'authentification et de cryptographie.

Les VPC sont couramment utilisés dans le contexte de IaaS.

# 3.
A quoi sert un NSG ?

Les Network Security Groups permettent de définir des règles qui contrôlent les types de trafic autorisés entre les sous-réseaux virtuels d'un réseau virtuel, et même entre des machines virtuelles spécifiques. C'est très utile si on souhaite contrôler le flux d'un trafic entre les sous-réseaux virtuels.

# 4.
Quelles sont les 5 propriétés désirables du cloud ?

 - Accès aux services par l’utilisateur à la demande.
La mise en œuvre des systèmes est entièrement automatisée et c’est l’utilisateur, au moyen d’une console de commande, qui met en place et gère la configuration à distance.

 - Accès réseau large bande.
Ces centres de traitement sont généralement raccordés directement sur le backbone Internet pour bénéficier d’une excellente connectivité. Les grands fournisseurs répartissent les centres de traitement sur la planète pour fournir un accès aux systèmes en moins de 50 ms de n’importe quel endroit.

 - Réservoir de ressources (non localisées).
La plupart de ces centres comportent des dizaines de milliers de serveurs et de moyens de stockage pour permettre des montées en charge rapides. Il est souvent possible de choisir une zone géographique pour mettre les données “près” des utilisateurs.

 - Redimensionnement rapide (élasticité).
La mise en ligne d’une nouvelle instance d’un serveur est réalisée en quelques minutes, l’arrêt et le redémarrage en quelques secondes. Toutes ces opérations peuvent s’effectuer automatiquement par des scripts. Ces mécanismes de gestion permettent de bénéficier pleinement de la facturation à l’usage en adaptant la puissance de calcul au trafic instantané.

 - Facturation à l’usage.
Il n’y a généralement pas de coût de mise en service (c’est l’utilisateur qui réalise les opérations). La facturation est calculée en fonction de la durée et de la quantité de ressources utilisées. Une unité de traitement stoppée n’est pas facturée.

# 5.
Qu'est-ce que l'A/B Testing ?

L'A/B Testing (parfois appelés tests partagés) compare deux versions d'une page Web pour voir celle qui fonctionne le mieux. On compare deux pages Web en montrant les deux variantes (A et B) à des visiteurs similaires en même temps. Celle qui donne le meilleur taux de satisfaction gagne. Cela permet d'effectuer des choix grâce aux retours client. C'est très souvent utilisé dans les grandes entreprises comme Facebook, qui montre ainsi de version de l'application.

# 6.
Comment programmer le cloud ?

-----

# 7.
Quelle est la technique pour faire un déploiement sans interruption de service ?

Pour faire un déploiement sans interruption de service, on peut utiliser la méthode du blue/green. Cette méthode consiste à avoir deux environnements de production : un premier (blue) qu'utilisent les utilisateurs, et un second (green) dans la même version que le premier. On développe les nouvelles fonctionnalités, on les déplois sur l'environnement non-utilisé (le green), et une fois que cela est fait on fait passer le trafic d'utilisateur sur l'environnement nouvellement déployer. Lorsqu'il faudra faire un nouveau déploiement, on fera alors l'inverse en déployant les nouvelles fonctionnalités sur l'environnement non-utilisé (blue), et en faisant ensuite repasser le trafic sur cet environnement.

# 8.
Qu'est-ce que le Canary release ?

C'est le principe de prendre une petite portion des utilisateurs pour une nouvelle release. Ces utilisateurs seront les premiers à l'utiliser (et donc la tester). Si tout va bien, tant mieux et la release sera déployer à tous les autres utilisateurs. Si cela va mal, seul un petit groupe aura été impacté. D'où le principe de Canary release, le petit groupe étant le canari que prenaient les mineurs et qui piaillait lorsqu'il y avait du gaz dans l'air, prévenant ainsi les coups de grizou.

# 9.
Comment changer de taille de machine virtuelle ?

Pour changer la taille des machines virtuelles, il faut changer la taille des disques de ces machines, mais aussi des partitions !

En pratique on peut utiliser : cd "C:\Program Files\Oracle\VirtualBox"
VBoxManage modifyhd "C:\Users\...\Windows10pro.vdi" --resize 81920   qui va modifier la taille de l'image disque pour qu'elle soit de 81920 Mo (80Go). Ensuite il faut augmenter la taille des partitions. Il suffit d’ouvrir le gestionnaire de disque (Win+R puis diskmgmt.msc). Ensuite, sur la partition, il faut faire un clique droit puis "Étendre le volume". Valider, et la partition devrait maintenant occuper l’espace nouvellement alloué.

# 10.
Qu'est-ce que le Blue/Green deployment ?

Voir question #7
