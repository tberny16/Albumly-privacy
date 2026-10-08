# Pages publiques d'Albumly

Pages statiques de l'application Android **Albumly**, éditée par Berny Labs. Le code source de
l'application vit ailleurs et reste privé. Le site n'utilise aucun script, cookie, outil d'analyse,
police distante ni formulaire de collecte.

## Pages

- `accueil.html` : présentation, fonctionnalités et contact.
- `index.html` : politique de confidentialité, à son adresse historique.
- `conditions.html` : conditions d'utilisation proposées, à relire avant publication.
- `styles.css` : styles responsive et modes clair/sombre ; `icon.png` : logo existant.

## Publication

Servi par GitHub Pages depuis la branche `main`, à la racine :
*Settings → Pages → Source : Deploy from a branch → `main` / `(root)`*.

URL publique : <https://tberny16.github.io/Albumly-privacy/>

Après publication des nouvelles pages, renseigner dans Google Auth Platform → Branding :

| Champ | Valeur |
|---|---|
| Page d'accueil | `https://tberny16.github.io/Albumly-privacy/accueil.html` |
| Politique de confidentialité | `https://tberny16.github.io/Albumly-privacy/` |
| Conditions d'utilisation | `https://tberny16.github.io/Albumly-privacy/conditions.html` |
| Domaine autorisé | `tberny16.github.io`, sous réserve de validation par Google |

Ces URL ne sont utilisables qu'une fois les fichiers publiés et accessibles sans connexion.
Une préparation locale ne vaut ni déploiement GitHub Pages, ni validation juridique ou OAuth.

C'est cette URL qui est déclarée dans la fiche Google Play et dans le formulaire Data Safety. Le
chemin respecte la casse du nom du dépôt : `albumly-privacy` en minuscules renvoie une 404.

## Mise à jour

Le texte de référence est `docs/PRIVACY_POLICY.md` dans le dépôt de l'application. Toute
modification doit être reportée ici **et** la date de dernière mise à jour changée dans les deux
fichiers, faute de quoi les deux versions divergent.

Google Play vérifie que le nom de l'éditeur et l'adresse de contact affichés ici correspondent à
ceux de la fiche.

## Vérification de propriété pour OAuth

Utiliser le compte Google propriétaire ou éditeur du projet OAuth dans
[Google Search Console](https://search.google.com/search-console/).
Ajouter une propriété de type « Préfixe de l'URL » pour le site accessible que vous contrôlez,
puis suivre la méthode de validation proposée par Google (balise HTML ou fichier).
Ne pas inventer de valeur `google-site-verification` : conserver la valeur fournie par Google.

Une propriété couvrant seulement `/Albumly-privacy/` ne prouve pas à elle seule le contrôle
de toute la racine `https://tberny16.github.io/`. Si Google exige la validation de cette racine,
le jeton doit être servi par le site racine correspondant ou par un domaine que vous contrôlez.
Ne jamais déclarer la propriété de `github.io` ou `github.com`.

La validation Search Console, la publication du branding et le passage de l'audience OAuth
en production sont des étapes distinctes. La validation des scopes peut aussi être nécessaire.

Références : [Branding](https://support.google.com/cloud/answer/15549049),
[Search Console](https://support.google.com/webmasters/answer/9008080?hl=fr).
