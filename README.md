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
