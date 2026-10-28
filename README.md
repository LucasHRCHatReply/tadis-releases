# Tadis pour macOS

Tadis (« t'as dit ») transcrit un fichier audio ou vidéo en texte, sur le Mac, sans compte et sans rien envoyer :
vocal WhatsApp, mémo, réunion, vidéo. On dépose le fichier, le texte sort, on le copie ou on l'exporte (texte,
sous-titres SRT ou VTT, Markdown horodaté). Les passages douteux (boucle, phrase inventée, passage parti dans une autre
langue) sont marqués, jamais effacés en silence.

Deux moteurs, tous deux locaux : Parakeet v3 (NVIDIA, téléchargé une fois, ~470 Mo) par défaut, et le moteur de dictée
de macOS en second avis.

Ce dépôt ne contient que les versions à installer. Le code source n'est pas public. Version de démonstration : à
essayer, pas encore à confier un travail important.

## Ce qu'il faut

- un Mac à puce Apple (M1 ou plus récent) ;
- macOS 26 ou plus.

## Installer

Dans Terminal (Cmd + Espace, « Terminal »), une seule commande, qui installe aussi les mises à jour :

```
curl -fsSL https://raw.githubusercontent.com/LucasHRCHatReply/tadis-releases/main/installer.sh | zsh
```

Le script télécharge la dernière version, vérifie l'empreinte SHA-256 du zip, l'identifiant de l'app et sa signature
(équipe Apple `JT9FY7PP7K`, `codesign --verify --deep --strict`), copie l'app dans ~/Applications, puis l'ouvre.
