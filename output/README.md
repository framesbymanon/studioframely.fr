# Studio Framely — Site

## Structure

```
index.html                       ← la page (propre, plus de blob 21 Mo)
assets/
  images/
    hero-background.jpg
    portfolio-1.jpg
    portfolio-2.jpg
    portfolio-3.jpg
  video/
    portfolio-reel.mp4
  icons/
    logo-header.svg
    logo-footer.svg
  js/
    dc-runtime.js                ← moteur de rendu (ne pas modifier)
```

## Ce qui a changé par rapport à l'export Claude Design

- Le fichier original (21,6 Mo) intégrait 738 fichiers de police en base64
  directement dans la page. Ils ont été retirés et remplacés par un lien
  Google Fonts classique (mêmes polices : Bodoni Moda, Cormorant Garamond,
  DM Serif Display, Gilda Display, Gothic A1, Italiana, Marcellus,
  Playfair Display, Prata, Space Mono).
- Les images, la vidéo et les logos sont maintenant de vrais fichiers dans
  `assets/`, plus des blobs encodés dans le HTML.
- Résultat : dossier complet à 9,4 Mo (contre 21,6 Mo), et un `index.html`
  lisible de 28 Ko au lieu de 21 Mo.

## Pousser sur GitHub

Dans un terminal, à l'intérieur de ce dossier :

```bash
git init
git add .
git commit -m "Site Studio Framely"
git branch -M main
git remote add origin https://github.com/TON-USERNAME/TON-REPO.git
git push -u origin main
```

(Crée d'abord le repo vide sur github.com — bouton "New" — puis copie l'URL
qu'il te donne pour remplacer celle ci-dessus.)

## Mettre le site en ligne

Une fois sur GitHub, connecte le repo à Vercel (vercel.com → "Import Project"
→ sélectionner le repo) : chaque `git push` redéploiera automatiquement.
Comme c'est un site statique (pas de framework), Vercel le détecte et le sert
tel quel, sans configuration.

## Si tu remodifies le design dans Claude Design

Ré-exporte en "Standalone HTML" et redonne-moi le nouveau fichier — je
referai le même nettoyage (extraction des assets, retrait des polices
embarquées) pour garder le dossier léger.
