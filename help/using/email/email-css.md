---
solution: Journey Optimizer
product: journey optimizer
title: Ajout d’une page CSS personnalisée au contenu de votre e-mail
description: Découvrez comment ajouter du code CSS personnalisé au contenu de votre e-mail directement dans le Designer d’e-mail de Journey Optimizer.
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, éditeur, résumé, e-mail
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# Ajouter des métadonnées au contenu de votre e-mail {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Ajouter un CSS personnalisé"
>abstract="xxx."

Lors de la conception de vos e-mails, vous pouvez ajouter votre propre CSS personnalisé directement dans le [!DNL Journey Optimizer] [Designer d’e-mail](get-started-email-design.md).

Ce qui est attendu dans la zone de texte Ajouter un CSS personnalisé est une chaîne CSS valide.

![](assets/email-body-css.png)

Conditions de disponibilité

La fonction Ajouter un CSS personnalisé n’est disponible que lorsqu’un contenu est défini dans l’éditeur. Pour voir la section Ajouter un CSS personnalisé , l’utilisateur doit ajouter du contenu dans l’éditeur. Si l’utilisateur supprime tout son contenu, la section disparaît et le code CSS personnalisé n’est pas appliqué. Si l’utilisateur ajoute à nouveau du contenu, la section est disponible et le code CSS personnalisé est appliqué.

**Exemples d’entrées CSS non valides**

Une page CSS non valide ne peut pas être enregistrée et si la page CSS n’est pas valide, un toast rouge s’affiche pour indiquer que la page CSS n’a pas pu être enregistrée.

`<style>` n’est pas accepté


```
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```


Accolade manquante non valide

```
body {
 background: red; 
```
