# NGINX szerver Vagrant boxban

## Leírás
Ez a repository az SZTE-n hirdetett Felhő és DevOps alapok kurzus gyakorlátnak teljesítéséhez szükséges beadandó feladatot tartalmazza.

### A Vagrantfile-ról
A `Vagrantfile` a következő beállításokat végzi el:
  - egy `ubuntu/bionic` Vagrant boxot fog elindítani,
  - beállítja a megfelelő hypervisort (ebben az esteben VirtualBox), és konfigurálja azt
  - létrehoz egy privát hálózatot a VM-nek,
  - amelynek a `192.168.33.10`-es privát IP címet osztja ki
  - futtat egy `apt-get update`-et, és
  - feltelepíti az NGINX-et
  - majd a `./html` mappát besynceli a `/var/www/html`-be

## Indítás
`vagrant up`

## Elérés
Az nginx szerver elérhető a [192.168.33.10](http://192.168.33.10) IP címen.