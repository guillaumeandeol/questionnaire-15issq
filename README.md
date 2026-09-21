# Questionnaire 15iSSQ

Version électronique du questionnaire d'habiletés auditives **15iSSQ**
(version française abrégée du *Speech, Spatial and Qualities of Hearing scale*).

**Adresse publique : https://guillaumeandeol.github.io/questionnaire-15issq/**

C'est l'adresse à communiquer aux collègues et aux participants. Le QR code
correspondant est fourni dans ce dossier : `QR_15iSSQ_github.svg` pour
l'impression, `QR_15iSSQ_github.png` pour l'écran.

Application autonome : un seul fichier HTML, aucune dépendance, aucun serveur.
Tout le calcul (scores par partie, comparaison aux normes normo-entendants,
écarts en écarts-types) se fait dans le navigateur.

## Confidentialité

L'application ne transmet **aucune donnée** : rien n'est envoyé ni enregistré
sur un serveur. Les réponses restent dans le navigateur du participant et
disparaissent à la fermeture de la page.

## Déroulé

1. Écran d'accueil : consignes, identifiant libre et date.
2. Les 16 items, chacun avec un curseur de 0 à 10 et une case
   « Non applicable » qui exclut l'item du calcul.
   L'item 16 (effort d'écoute) utilise une échelle inversée.
3. Page de résultats : score global, scores par partie (audition de la parole,
   audition spatiale, qualité d'audition) et détail par question.

## Lecture des résultats

Chaque score est comparé à la moyenne des normo-entendants (normes Moulin
et al. 2015) et l'écart est exprimé en écarts-types (ET) :

| Statut | Écart à la norme |
|---|---|
| Dans la norme | ≥ −1 ET |
| Limite | −1 à −2 ET |
| Sous la norme | < −2 ET |

La colonne **Visuel** place le score sur une jauge graduée en écarts-types
(de −4 à +1,5 ET) : trait foncé sur la moyenne des normo-entendants, traits
fins sur les bornes −1 ET et −2 ET, zones colorées pour les intervalles
correspondants, pastille pour le score. L'axe étant le même sur toutes les
lignes, les jauges se comparent directement entre sous-échelles et entre
items — ce qui ne serait pas le cas sur une échelle 0-10, les écarts-types
différant d'une sous-échelle à l'autre. Une pastille en pointillé signale un
score situé hors de l'axe.

### Profil radar

Le bouton **Afficher le profil radar** trace les 15 items du score global sur
un graphe en toile d'araignée (l'item 16, effort d'écoute, en est exclu
puisqu'il n'entre pas dans le score). Le rayon est gradué en écarts-types,
comme les jauges : la norme est donc un cercle parfait et les bornes −1 ET et
−2 ET deux cercles concentriques — ce qui ne serait pas le cas avec des scores
bruts, les normes variant de 7,5 à 9,5 selon l'item.

Les trois sous-échelles occupent chacune un tiers du disque et sont
matérialisées par un secteur teinté, des séparateurs radiaux, un arc extérieur
coloré et le nom de la sous-échelle : parole en bleu (items 1-5), spatiale en
violet (6-10), qualité en vert (11-15). Un item déclaré non applicable apparaît
en gris, le profil ne passant pas par ce point.

L'ordre des axes est celui du questionnaire. **Il ne doit pas être modifié** :
sur un radar, changer l'ordre des axes change la silhouette du profil et son
aire, donc l'impression qu'il donne. Le radar reste un complément au tableau,
où se lisent les valeurs exactes.

Deux boutons l'accompagnent :

- **Télécharger l'image (PNG)** — exporte le graphe en 1120 × 1236 px, avec
  l'identifiant et la date, pour un compte rendu ou une diapositive.
- **Comparer à une passation** — superpose en pointillé un profil antérieur.
  Chaque passation fournit un *code de profil* (`15iSSQ|ID|date|scores`) à
  conserver ; le recoller ici suffit à afficher les deux profils ensemble.
  Rien n'est stocké par l'application : le code est la seule trace, et c'est
  vous qui le gardez.

Cet outil est une aide : il ne remplace pas un bilan audiologique complet.

## Hébergement

Le site est publié par **GitHub Pages** depuis la branche `main`, dossier
`/ (root)` (réglage dans *Settings → Pages*). Aucun fichier de configuration
n'est nécessaire : GitHub sert directement `index.html`.

## Mise à jour

Remplacez `index.html` et validez (commit) : le site se republie
automatiquement en une ou deux minutes. Le plus simple depuis le navigateur :
**Add file → Upload files**, puis glissez le nouveau fichier — GitHub le
reconnaît comme une mise à jour.

En ligne de commande :

```bash
git clone https://github.com/guillaumeandeol/questionnaire-15issq.git
cd questionnaire-15issq
# remplacer index.html par la nouvelle version
git commit -am "Mise à jour du questionnaire"
git push
```

Si une ancienne version s'affiche encore chez un collègue, c'est le cache du
navigateur : Ctrl+Maj+R (Cmd+Maj+R sur Mac) force le rechargement.

## Impression / archivage

Le bouton **Imprimer / PDF** de la page de résultats produit un compte rendu
imprimable ou enregistrable en PDF, jauges comprises.

## Références

Items et normes : Moulin et al. 2015 & 2019 (PAM / CRNL), validation française
du SSQ.
