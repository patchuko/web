## Blog parch.fr

Fait avec hugo.

# Pour publier et générer le site

On lance
```
./publishparch
```

Cela revient à faire un:

```
hugo
rclone sync --interactive --sftp-host 192.168.5.17 --sftp-user julienAdmin --sftp-ask-password public/ :sftp:web/
```

Après une commande `hugo`le site est regénéré dans le répertoire public.

# Pour tester le site en local

```
hugo server -D
```

# Pour ajouter un post
```
hugo new content posts/a-post.md
```

On peut aussi ajouter un _index.md pour fixer l'image de background sur la première page avec un
```
hugo new content _index.md
```

En éditant le fichier de config situé dans `/contents/_index.md`, on ajoute la dernière ligne feature_image poitant vers une image dans le répertoire `static/`:
```
+++
title = ''
date = 2024-05-27T10:05:39+02:00
draft = false
featured_image = "/marek-piwnicki-7xHmMk08mRo-unsplash.jpg"
+++
```
