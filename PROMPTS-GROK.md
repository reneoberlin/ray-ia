# PROMPTS-GROK.md

## Mission

Ce fichier définit comment créer les prompts destinés à Grok pour l’univers de Ray.

Tout prompt doit respecter RAY-CORE.md.

---

# 1. Règle principale

Quand l’utilisateur donne une idée courte, il ne faut pas lui demander de répéter toutes les caractéristiques de Ray.

Le système doit automatiquement reprendre les règles de RAY-CORE.md.

Exemple :

Utilisateur :
"Ray marche dans Paris sous la pluie."

Le système doit automatiquement compléter :
- apparence de Ray
- âge apparent
- fidélité du visage
- vêtements
- époque
- décor
- lumière
- ambiance
- cadrage
- interdits

---

# 2. Deux types de prompts Grok

## A. Prompt pour créer une image

Le prompt doit préciser :
1. sujet principal
2. apparence de Ray
3. vêtements
4. époque
5. décor
6. action
7. lumière
8. cadrage
9. ambiance
10. rendu
11. interdits

---

## B. Prompt pour animer une image

Quand une image existe déjà, Grok ne doit pas recréer la scène.

Il doit :
- conserver strictement les visages
- conserver les vêtements
- conserver le décor
- conserver les proportions
- conserver la lumière
- conserver la composition générale

Il doit seulement ajouter les mouvements demandés.

---

# 3. Règles pour l’animation

Les mouvements doivent être naturels et subtils.

Exemples :
- Ray marche lentement
- Ray tourne légèrement la tête
- Ray regarde une personne
- Ray avance de quelques pas
- Ray ajuste son chapeau
- Ray respire naturellement
- les vêtements bougent légèrement
- les cheveux réagissent doucement au vent
- les personnages bougent au rythme de la musique
- la caméra effectue un travelling lent
- léger zoom cinématographique
- panoramique lent

---

# 4. Interdits vidéo

Ne jamais :
- modifier le visage de Ray
- vieillir Ray
- changer sa coiffure
- modifier sa moustache
- changer ses vêtements sans demande
- changer le décor
- ajouter des personnages sans demande
- modifier la morphologie
- faire des mouvements brusques
- déformer les mains
- faire bouger les lèvres si aucun dialogue n’est demandé
- transformer l’image en style moderne

---

# 5. Caméra

Privilégier :
- travelling lent
- panoramique doux
- léger zoom
- caméra stable
- mouvement cinématographique fluide

Éviter :
- caméra nerveuse
- zoom brutal
- rotation artificielle
- effet clip moderne non demandé

---

# 6. Visages

Priorité absolue :
le visage de Ray et des autres personnages de référence doit rester identique.

Formulation recommandée :

"Preserve the exact facial identity from the reference image. Do not alter, age, beautify, modernize or reinterpret the face."

Pour Ray ajouter :

"Ray must remain approximately 42–45 years old in appearance. Do not make him older."

---

# 7. Prompt image type

Structure :

"Create a cinematic retro scene featuring Ray.

Ray must preserve the exact facial identity from the reference image, without deformation or aging. He appears approximately 42–45 years old, with a very thin discreet moustache, natural facial proportions and realistic features.

[Décrire ici la tenue.]

[Décrire ici le décor.]

[Décrire ici l’action.]

The scene takes place in [année ou époque].

Use authentic period details, realistic proportions, harmonious lighting and a classic cinematic atmosphere.

Camera: [cadrage].

Lighting: [lumière].

Visual style: realistic vintage cinema, elegant, subtle film texture, historically coherent.

Do not modernize the scene. Do not age Ray. Do not alter his face, body proportions or identity."

---

# 8. Prompt animation type

Structure :

"Animate the provided image while preserving the original composition.

Do not recreate or redesign the characters.

Preserve exactly:
- facial identity
- age
- hairstyle
- clothing
- body proportions
- background
- lighting
- visual style

Action:
[décrire uniquement les mouvements]

Ray must remain visually identical to the reference image and approximately 42–45 years old in appearance.

Camera movement:
[décrire mouvement caméra]

Movements must be natural, subtle, realistic and cinematic.

Do not change faces, clothing, environment or proportions."

---

# 9. Si plusieurs personnages sont présents

Pour chaque personnage :
- respecter son visage de référence
- respecter son âge apparent
- respecter sa morphologie
- respecter sa tenue
- ne pas fusionner les visages
- ne pas remplacer un personnage par un autre

Ray doit rester parfaitement identifiable.

---

# 10. Si une photo de référence est fournie

La photo devient la priorité visuelle.

Le prompt doit explicitement dire :
"Use the provided reference image as the strict identity reference."

L’image ne doit pas être seulement "inspirée" de la référence.

Elle doit conserver l’identité visuelle du personnage.

---

# 11. Réponse attendue

Quand l’utilisateur demande un prompt Grok, fournir directement :

PROMPT GROK — IMAGE

ou

PROMPT GROK — ANIMATION

Puis le prompt prêt à copier.

Éviter les longues explications sauf si elles sont demandées.

---

# 12. Règle finale

Une idée courte de l’utilisateur doit suffire.

Le système doit compléter automatiquement les informations manquantes grâce à :
- RAY-CORE.md
- les fichiers personnages
- les fichiers de continuité
- les références visuelles disponibles