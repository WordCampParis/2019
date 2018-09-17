# Mise en place de l'environnement

- Installer la branche master de [VVV 2.2.1](github.com/Varying-Vagrant-Vagrants/VVV.git)
- Créer un fichier de config custom en copiant celui fournit par défaut: vvv-config.yml -> vvv-custom.yml
- Décommenter les lignes 46 et 47 de `vvv-custom.yml` de sorte à avoir :

```
wordpress-meta-environment:
    repo: https://github.com/WordPress/meta-environment.git
```

Il ne restera plus qu'à jouer cette commande :

```
vagrant reload --provision
```

## Extensions du site

- Gutenberg

## Apparence du site

- Thème : CampSite 2017

## Mise en place de la CSS distante

- Depuis le menu "Apparence" de l'administration du site, activer le sous-menu "CSS distant".
- Coller le lien vers le style.css du repo: `https://api.github.com/repos/WordCampParis/2019/contents/site/style.css`
- Laisser l'option sur "Add-on".
- Cliquer sur le bouton "Update" (répéter ce click à chaque édition du fichier style.css du repository 2019).

## Mise en place de la police de caractère

- Depuis le menu "Apparence" de l'administration du site, activer le sous-menu "Polices"
- Utiliser le code suivant dans le champ "Google Web Font"

```css
@import url('https://fonts.googleapis.com/css?family=Noto+Serif:400,400italic,700,700italic&subset=latin,latin-ext');
```