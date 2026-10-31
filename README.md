# 🕹️ Cartouche

**Une image entre, un jeu vidéo sort.**

Tu glisses une photo (ton chat, une pieuvre en plastique, un dessin de ton neveu, un coucher de soleil…), tu ajoutes si tu veux un petit bout d'histoire, et une IA te fabrique un mini-jeu web complet, jouable tout de suite. Titre, score, vies, niveaux, musique, écran de game over : tout y est.

👉 **[Essayer Cartouche](https://TON-PSEUDO.github.io/cartouche/)**

---

## ✨ Ce que ça fait

- **Ton image devient le jeu.** L'IA regarde l'image, choisit le type de jeu qui colle le mieux (plateforme, shoot'em up, casse-briques, taquin, runner…) et réutilise vraiment l'image dans le jeu.
- **Le personnage principal prend vie.** S'il y a un sujet bien visible sur la photo, il devient le héros : il est détouré, reconnu (humain, animal, pieuvre, véhicule, plante, objet…) puis animé selon sa nature. Un humain marche, un oiseau bat des ailes, une pieuvre agite ses tentacules.
- **Ton histoire compte.** Le champ de description accepte une petite histoire : l'IA s'en sert pour les personnages, le but du jeu et l'ambiance, et en tire une intro affichée au lancement.
- **Tu choisis le style, ou pas.** Laisse l'IA décider, ou impose un style parmi 16. Une fois le jeu prêt, tu peux le refaire dans un autre style.
- **Ça se joue partout.** Clavier (flèches, ZQSD ou WASD), souris, manette ou écran tactile, et tu peux mélanger en pleine partie.
- **Ça marche du premier coup (ou presque).** Chaque jeu est testé automatiquement avant de t'être livré. En cas de bug, l'IA corrige toute seule.
- **C'est joli.** Une passe graphique optionnelle repeint le jeu une fois qu'il fonctionne : décors en couches, lumières, particules, animations.
- **Tu gardes tout.** Bouton « Jouer » pour lancer le jeu dans un nouvel onglet, bouton « Télécharger le .zip » pour le garder. Le jeu téléchargé marche hors ligne, sans rien installer : double-clic sur `index.html` et c'est parti.

## 🤖 Les IA compatibles

Cartouche fonctionne avec trois IA. Il te faut **une clé API** pour au moins l'une d'elles :

| IA | Où trouver une clé | Le petit mot |
|---|---|---|
| Google Gemini | [aistudio.google.com/apikey](https://aistudio.google.com/apikey) | Palier gratuit, le plus précis pour repérer le personnage |
| Anthropic Claude | [console.anthropic.com](https://console.anthropic.com/settings/keys) | Payant à l'usage, très bon code de jeu |
| OpenAI ChatGPT | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) | Payant à l'usage |

> ⚠️ Un abonnement ChatGPT Plus ou Claude Pro **ne donne pas** accès à l'API. Il faut une clé créée sur la console du fournisseur, avec un peu de crédit dessus.

Côté modèle, les versions « Pro », « Sonnet » ou « Opus » donnent des jeux plus beaux et plus solides que les versions « Flash », « mini » ou « Haiku ». Elles sont aussi plus lentes.

## 🚀 Comment s'en servir

1. Choisis ton IA en haut de la page et colle ta clé.
2. Dépose une image JPG ou PNG dans la cartouche (ou colle-la avec Ctrl+V).
3. Si tu veux, donne un nom au jeu, écris une description ou une petite histoire, et choisis un style.
4. Clique sur **Fabriquer le jeu** et regarde la barre avancer. Selon l'IA, ça prend de quelques minutes à plus d'une demi-heure (voir plus bas).
5. Joue, télécharge, recommence dans un autre style. 🎉

**Astuce :** une image avec un sujet bien net sur un fond simple (ou un PNG déjà transparent) donne le meilleur héros animé.

## ⏱️ Pourquoi c'est parfois long ?

Fabriquer un jeu, c'est écrire plusieurs dizaines de milliers de caractères de code, et ça ne prend pas le même temps chez tout le monde.

**La durée dépend énormément de l'IA et du modèle.** Un modèle rapide (Gemini Flash, par exemple) peut boucler un jeu en quelques minutes. Un gros modèle prend son temps : avec Claude, il a déjà fallu **40 minutes** pour un seul jeu. C'est normal, ça n'est pas planté. En échange, ces gros modèles écrivent souvent des jeux plus riches et plus soignés.

**Le nombre d'étapes joue aussi.** À chaque correction automatique, et pendant la passe graphique, l'IA réécrit le jeu en entier. Un jeu qui passe le test du premier coup va donc beaucoup plus vite qu'un jeu qui demande deux corrections plus l'embellissement.

**Les messages de progression varient d'une IA à l'autre.** Certaines IA envoient leur code au fil de l'eau : le compteur de caractères défile et la barre avance en continu. D'autres réfléchissent en silence avant d'écrire la moindre ligne : la barre peut alors rester immobile un bon moment, avec très peu de messages, puis tout arriver d'un coup. Si le chronomètre tourne encore, c'est que ça travaille.

**Pour aller plus vite :**

- **Décoche la passe graphique supplémentaire.** Le temps de fabrication est à peu près divisé par deux.
- **Choisis un modèle plus léger** (Flash, mini, Haiku). Le jeu sera un peu plus simple, mais prêt bien plus tôt.
- **Laisse l'onglet ouvert** pendant la fabrication : si tu le fermes, tout est perdu. Tu peux aller faire autre chose dans un autre onglet pendant que l'IA écrit. En revanche, le test automatique a besoin que l'onglet Cartouche soit affiché, car les navigateurs mettent les animations en pause en arrière-plan. Quand le titre de l'onglet affiche ⏸, reviens dessus : le test démarre aussitôt.

## 🔒 Et mes données ?

- **Pas de serveur.** Cartouche est une simple page HTML. Ton image et ta clé partent directement de ton navigateur vers l'IA que tu as choisie, et nulle part ailleurs.
- **Ta clé reste chez toi.** Elle n'est enregistrée que si tu coches « Mémoriser », et seulement dans ton navigateur.
- **Les jeux aussi.** Ils sont fabriqués dans ton navigateur et n'existent que chez toi, jusqu'à ce que tu décides de les partager.

## 🛠️ Héberger ta propre copie

C'est un seul fichier, sans dépendance ni installation.

- **Sur ton ordi :** télécharge `index.html` et ouvre-le par un double-clic.
- **Sur GitHub Pages :** forke le dépôt, puis va dans *Settings → Pages → Deploy from a branch → `main` / `(root)`*. Une minute plus tard, c'est en ligne.

Pas besoin de droits spéciaux ni de dossier temporaire : tout se passe dans le navigateur du visiteur.

> 🙅 Ne mets **jamais** ta clé API dans le code avant de le publier. Un dépôt public, tout le monde peut le lire.

## 🎁 Partager un jeu

Le `index.html` du .zip est autonome. Tu peux l'envoyer tel quel, ou le déposer dans un autre dépôt GitHub Pages pour avoir un lien jouable. Tes amis n'ont besoin d'aucune clé : le jeu est déjà fabriqué.

## 🆘 Ça coince ?

| Le message | Ce qu'il faut faire |
|---|---|
| « … est surchargé en ce moment » | Rien de grave : Cartouche réessaie tout seul sans perdre le code déjà reçu. Si ça persiste, change de modèle puis clique sur **Reprendre la fabrication**. Rien n'est perdu. |
| « … est injoignable » | Vérifie ta connexion, puis désactive ton bloqueur de pub ou ton VPN pour cette page. |
| Bandeau rouge « aperçu » | La page tourne dans un aperçu qui bloque tout. Ouvre-la directement dans ton navigateur. |
| Le jeu ne s'ouvre pas | Ton navigateur bloque les pop-up : autorise-les pour Cartouche. |
| L'onglet du jeu est vide après rechargement | Le jeu vit dans l'onglet Cartouche. Si tu l'as fermé, le jeu est parti : utilise le .zip pour garder tes créations. |
| La manette ne répond pas | Appuie sur un bouton une fois le jeu ouvert. Les navigateurs ne signalent la manette qu'après une première pression. |

## 🧱 Sous le capot

- Un seul fichier HTML, en JavaScript pur, sans framework ni bibliothèque.
- Les jeux générés dessinent tout en Canvas 2D, avec des sons synthétisés par la Web Audio API et un support complet de la Gamepad API.
- Le détourage du personnage, le test automatique et la création du .zip sont faits maison, directement dans le navigateur.

## 📜 Licence

Cartouche est sous **licence MIT** : tu peux l'utiliser, le copier, le modifier, le partager et même le vendre, à condition de garder la mention de copyright et le texte de la licence. Le logiciel est fourni tel quel, sans garantie. Tous les détails sont dans le fichier [LICENSE](LICENSE).

Cartouche ne revendique aucun droit sur les jeux que tu fabriques. Pense simplement aux droits de l'image que tu utilises si tu comptes diffuser le jeu.

---

Imaginé par Damballah Oueddo, fabriqué avec un coup de main de Claude. Amuse-toi bien ! 👾
