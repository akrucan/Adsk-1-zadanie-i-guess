# Zadanie 1
## Kroki instalacji

1. Stworzenie maszyny wirtualnej na platformie AWS
2. Połączenie z sokrates.edu.jkan.pl
3. Stworzenie pliku hosts.ini zawierających ip wirtulanych maszyn
4. Stworzenie folderu *files* zawierającego potrzebne pliki konfiguracyjne (*Mariadb.repo, wp-config.php, blog-vhost.conf, lb.conf*)
5. Stworzenie pliku *setup_wp.yml* 
```
Plik setup.yml zawiera:
- zadeklarowanie hostów
- instalację EPEL
- instalację repozytorium php (remi)
- instalację bibliotek php 
- skopiowanie configu Mariadb z pliku files/Mariadb.repo
- instalację Mariadb
- instalację MySQL
- instalację MySQL-python
- stworzenie bazy danych pod aplikację WordPress
- zadeklarowanie permisji dostępów użytkowników WordPress
- instalację WordPress
- zaciągnięcie configu vhostów z pliku files/blog-vhost.conf
- zaciągnięcie configu WordPress z pliku files/wp-config.php
```

## Wykonanie pliku setup_wp.yml
```
ansible-playbook setup_wp.yml -i hosts.ini -e DB_PW='(hasło)'

```
![](ez.png)