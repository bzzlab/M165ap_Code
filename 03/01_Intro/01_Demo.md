### Download-Links
* MongoDB Tools Download:
https://www.mongodb.com/try/download/database-tools
* Repo Sample-MongoDB:
https://github.com/huynhsamha/quick-mongo-atlas-datasets


#### Installation
1. Download des MongoDB-Tools als Zip-File 
(https://www.mongodb.com/try/download/database-tools/releases/archive)
2. Zip-File entpacken im Zielverzeichnis c:\Program Files\MongoDB\Server\
3. Verzeichnis umbenennen auf 'tools'
4. Kurzer Test im Quellverzeichnis
````
cd '/c/Program Files/MongoDB/Server/tools/bin'
mongorestore --version
````
5. Pfad im Home-Directory mit .bash_profile setzen
```
# Wechsel ins Home-Directory -> '~' Tilde-Zeichen erscheint
cd 

# Print working dirctory 
pwd

# leeres .bash_profile erstellen mit touch
touch .bash_profile

# .bash_profile editieren
nano .bash_profile

# Einfügen der Zeilen unten ...
## M165
export MONGODB='/c/Program Files/MongoDB/Server'
export PATH=$MONGODB/tools/bin:$PATH

# mit CTRL-x und yes Speicherung bestätigen

# .bash_profile nur einmalig ausführen
source .bash_profile

# alle Pfade ausgeben und Kontrolle, ob MongoDB-Pfad gesetzt ist
echo $PATH
```
6. Test: mongorestore --version