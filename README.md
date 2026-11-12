# Cap sur ma transition

Ce dépôt contient les ressources nécessaires pour implanter le processus **Cap sur ma transition** dans un environnement Microsoft 365.

La solution repose sur trois composantes :

1. un formulaire **Microsoft Forms**;
2. une liste **Microsoft Lists / SharePoint** pour compiler les données;
3. une solution **Power Automate** pour automatiser le traitement.

## Ressources requises

Avant de commencer, assurez-vous de disposer des éléments suivants dans ce dépôt :

- le fichier CSV servant à créer la liste;
- le fichier de solution Power Automate;
- les vidéos explicatives, accessibles en streaming depuis OneDrive;
- les autorisations nécessaires pour créer un formulaire, une liste SharePoint et importer une solution Power Automate.

# Procédure d’implantation

## 1. Dupliquer le formulaire Microsoft Forms

Utilisez le modèle suivant :

[Dupliquer le formulaire Cap sur ma transition](https://forms.cloud.microsoft/Pages/ShareFormPage.aspx?id=ROmSjqz7r0qDi2rOzIAlr0Cjq5h6BrpDn0c58ocAUSZUMzhKTjRPNDBDR1ZaVjBWWDRCTTQyNzRCOC4u&sharetoken=92ry78ZMckimYGeAX84K)

1. Ouvrez le lien.
2. Sélectionnez **Dupliquer** afin de créer une copie du formulaire dans votre environnement Microsoft 365.
3. Ajustez les questions **12, 13 et 14** selon votre contexte.
4. Vérifiez l’embranchement afin que chaque élève ne voie que les enseignants de son édifice.
5. Inscrivez le nom des responsables sous forme d’**adresse courriel**.

### Repérer l’identifiant du formulaire

Dans l’adresse URL de votre copie du formulaire, repérez l’identifiant du formulaire et conservez-le. Cet identifiant sera nécessaire lors de la configuration de la solution Power Automate.

> 🎥 **Vidéo explicative**  
> [Dupliquer et adapter le formulaire](URL_VIDEO_FORMS)

## 2. Créer la liste SharePoint

1. Ouvrez **Microsoft Lists**.
2. Créez une nouvelle liste à partir d’un fichier CSV.
3. Téléversez le fichier CSV fourni dans ce dépôt.
4. Au moment de nommer la liste, utilisez l’option **Créer dans** pour l’enregistrer dans un site SharePoint, et non dans **Mes listes**.
5. Une fois la liste créée, repérez et conservez son identifiant.

> 🎥 **Vidéo explicative**  
> [Créer la liste à partir du fichier CSV](https://o365csdgs-my.sharepoint.com/:v:/g/personal/stephane_lavoie_cssdgs_gouv_qc_ca/IQCc9jbiNZWnTI7yyBzmnQX2AdNeaU8X9tmqf1i3-IKPRRc?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=GWzeFZ)

## 3. Importer la solution Power Automate

1. Ouvrez **Power Automate**.
2. Dans le menu de gauche, sélectionnez **Solutions**.
3. Sélectionnez **Importer une solution**.
4. Chargez le fichier de solution fourni dans ce dépôt.
5. Terminez l’importation en configurant les connexions demandées.

> 🎥 **Vidéo explicative**  
> [Importer la solution Power Automate](URL_VIDEO_IMPORT)

## 4. Configurer les variables

Après l’importation, ajustez les trois variables de la solution :

| Variable | Valeur à fournir |
|---|---|
| URL du SharePoint | Adresse du site SharePoint qui contient la liste |
| ID de la liste | Identifiant de la liste créée à partir du fichier CSV |
| ID du formulaire | Identifiant de la copie du formulaire Microsoft Forms |

Vérifiez également que les connexions Microsoft Forms et SharePoint utilisent des comptes autorisés à accéder aux ressources correspondantes.

> 🎥 **Vidéo explicative**  
> [Configurer les variables et les connexions](URL_VIDEO_CONFIGURATION)

## 5. Activer et tester le flux

1. Activez le flux Power Automate.
2. Soumettez une réponse de test dans votre copie du formulaire.
3. Consultez l’historique d’exécution du flux.
4. Confirmez que les données ont été ajoutées dans la liste SharePoint.
5. Vérifiez l’embranchement des édifices et les adresses courriel des responsables.

### Liste de vérification

- [ ] Le formulaire a été dupliqué dans le bon environnement.
- [ ] Les questions 12, 13 et 14 ont été adaptées.
- [ ] L’embranchement affiche les bons enseignants pour chaque édifice.
- [ ] Les responsables sont inscrits sous forme d’adresses courriel.
- [ ] La liste a été créée dans le bon site SharePoint.
- [ ] L’URL SharePoint est exacte.
- [ ] L’ID de la liste est exact.
- [ ] L’ID du formulaire est exact.
- [ ] Le flux est activé.
- [ ] Une soumission complète a été testée.
- [ ] Les données apparaissent correctement dans la liste.

> 🎥 **Vidéo explicative**  
> [Tester et valider le processus](URL_VIDEO_TEST)

## Vidéos explicatives

Les vidéos sont hébergées dans OneDrive et s’ouvrent en streaming. Les liens doivent être configurés avec une autorisation de partage adaptée au public visé.

| Étape | Vidéo |
|---|---|
| Formulaire | [Dupliquer et adapter le formulaire](URL_VIDEO_FORMS) |
| Microsoft Lists | [Créer la liste à partir du CSV](URL_VIDEO_LIST) |
| Power Automate | [Importer la solution](URL_VIDEO_IMPORT) |
| Configuration | [Configurer les variables](URL_VIDEO_CONFIGURATION) |
| Validation | [Tester le processus](URL_VIDEO_TEST) |

> **Important :** un lien OneDrive réservé aux membres du CSSDGS ne sera pas accessible aux personnes externes. Vérifiez les paramètres de partage avant de diffuser ce dépôt.

## Dépannage rapide

### Le flux ne trouve pas le formulaire

Vérifiez que la variable **ID du formulaire** contient l’identifiant de la copie et non celui du formulaire modèle.

### Le flux ne trouve pas la liste

Vérifiez l’URL du site SharePoint et l’identifiant de la liste. Assurez-vous également que la liste a été créée dans un site SharePoint plutôt que dans **Mes listes**.

### Le mauvais responsable est proposé

Vérifiez les questions 12, 13 et 14, les embranchements du formulaire et le format des adresses courriel.

### Le flux ne se déclenche pas

Confirmez que le flux est activé, que les connexions sont valides et qu’une nouvelle réponse a été soumise après son activation.
