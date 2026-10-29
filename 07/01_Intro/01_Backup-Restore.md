## Backup und Restore 
For a demonstration see https://youtu.be/1saxBK0ibIg (the first 2.08 minutes)

1. Backup/Dump (Datensicherung)
```mongodump --host localhost --port 27017  --db mflix --out .```
2. Restore (Wiederherstellen)
```mongorestore --host localhost --port 27017 --db mflix --dir ./mflix```
