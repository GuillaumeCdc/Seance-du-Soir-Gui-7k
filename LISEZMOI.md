# Séance du soir : version avec vraies affiches

Trois fichiers : `index.html` (le jeu), `config.js` (ta clé TMDB), ce guide.

## 1. Obtenir la clé TMDB (gratuite, 5 minutes)

1. Crée un compte sur themoviedb.org et confirme ton e-mail.
2. Va dans Paramètres, puis API, et demande une clé (usage personnel, non commercial).
3. Copie la **Clé d’API** (la courte, en 32 caractères). Ne prends pas le « Jeton d’accès en lecture », il ne marche pas avec ce code.

## 2. Coller la clé

Ouvre `config.js` et colle la clé entre les guillemets :

```js
window.TMDB_KEY = "ta_clé_ici";
```

Pas besoin de toucher à `index.html`.

## 3. Mettre en ligne sur Render

1. Crée un dépôt GitHub avec les trois fichiers à la racine.
2. Sur Render : New, puis Static Site, et choisis ton dépôt.
3. Build Command : laisse vide. Publish Directory : `.` (un point).
4. Deploy. L’adresse fournie par Render est celle à partager avec tes amis.

## À savoir

- **La clé est visible** par quiconque ouvre le code de la page : c’est normal pour TMDB (clé gratuite, en lecture seule). Si tu préfères la garder discrète, mets le dépôt GitHub en privé (Render sait lire un dépôt privé). La clé reste visible dans le navigateur, mais elle ne traîne plus dans un dépôt public. Tu peux la régénérer à tout moment sur TMDB.
- **Ce qui change avec la clé** : vraies affiches partout, et pour chaque film la liste réelle des plateformes en abonnement en France (données TMDB fournies par JustWatch), à la place des badges indicatifs.
- **Limite connue** : le filtre « Je regarde sur » continue de s’appuyer sur les badges indicatifs de la base, pas sur les données TMDB. Les cartes affichées affichent la vraie dispo, mais le tri par plateforme peut en laisser passer une qui n’y est plus. Le lien « Où le voir » reste le juge de paix.
- **Sans clé**, rien ne casse : le jeu retombe sur les affiches illustrées.
- La mention TMDB demandée par leurs conditions s’affiche automatiquement en bas de page quand la clé est renseignée.
- Si les affiches n’apparaissent pas : ouvre la console du navigateur. Un message 401 signifie une clé erronée (vérifie que c’est bien la clé v3).
