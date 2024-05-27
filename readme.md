## Blog parch.fr

Fait avec hugo.

# Pour publier et générer le site

On lance
```./publishparch````

Cela revient à faire un:
````
hugo
rclone sync --interactive --sftp-host 192.168.5.17 --sftp-user julienAdmin --sftp-ask-password public/ :sftp:web/
```

