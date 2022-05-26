---
title: Utiliser du code JavaScript personnalisé dans une landing page
description: Découvrez comment concevoir le contenu dʼune page de destination dans Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 7%

---

# Utiliser du code JavaScript personnalisé dans une landing page {#lp-custom-js}

Vous pouvez définir le contenu de votre landing page à l&#39;aide d&#39;un code JavaScript personnalisé. Par exemple, si vous devez effectuer un style avancé ou si vous souhaitez ajouter des comportements personnalisés à vos landing pages, vous pouvez créer vos propres contrôles et les exécuter dans [!DNL Journey Optimizer].

## Insérer du code JavaScript dans une landing page

Pour insérer du code JavaScript personnalisé dans le contenu d’une landing page, vous pouvez effectuer l’une des opérations suivantes :

* Importez le contenu du HTML existant lorsque vous commencez à créer votre contenu, puis sélectionnez le fichier contenant votre code JavaScript personnalisé. Découvrez comment importer du contenu [dans cette section](../design/existing-content.md).

* Concevez votre landing page à partir de zéro ou d&#39;un modèle enregistré. Faites glisser et déposez le **[!UICONTROL HTML]** composant de contenu dans la zone de travail et affichez le code source pour ajouter votre JavaScript dans le composant. Découvrez comment utiliser le composant HTML dans [cette section](../design/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* Entrez ou collez du code JavaScript directement dans le concepteur de contenu. Découvrez comment coder votre propre contenu [dans cette section](../design/code-content.md).

>[!NOTE]
>
>Actuellement, vous ne pouvez pas afficher JavaScript en action lorsque [aperçu de la landing page](create-lp.md#test-landing-page).

Pour que la landing page s&#39;affiche correctement, utilisez la syntaxe suivante, comme décrit dans les sections ci-dessous.

## Initialisation du code

Pour initialiser votre code JavaScript, vous devez utiliser la variable `lpRuntimeReady` . Cet événement sera déclenché après l’initialisation réussie de la bibliothèque. Le rappel est exécuté avec la fonction `lpRuntime` pour exposer la méthode et les crochets de la bibliothèque.

`LpRuntime` signifie &quot;Landing page Runtime&quot;. Cet objet est l’identifiant de bibliothèque principal. Il expose les hooks, les méthodes d’envoi de formulaire et d’autres méthodes d’utilitaire pouvant être utilisées dans du code JavaScript personnalisé.

**Exemple :**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## Les points d&#39;extension

Les points d’extension permettent de joindre une méthode pendant le cycle de vie de l’envoi du formulaire. Par exemple, vous pouvez utiliser des points d’extension pour effectuer une validation de formulaire avant que le formulaire ne soit réellement envoyé.

Voici les hooks que vous pouvez utiliser :

| Nom | Description |
|--- |--- |
| addBeforeSubmitHook | crochet personnalisé à appeler avant envoi du formulaire. Renvoie true pour poursuivre l’envoi, sinon renvoie false pour bloquer l’envoi. |
| addBeforeSubmitHook | crochet personnalisé à appeler lors de l’échec de l’envoi du formulaire. |
| addOnSuccessHook | crochet personnalisé à appeler lors de l’envoi réussi du formulaire. |

**Exemple :**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## Envoi de formulaire personnalisé

Les méthodes répertoriées ci-dessous sont utilisées pour effectuer des envois de formulaire personnalisés.

>[!NOTE]
>
>Comme l’envoi du formulaire est géré par JavaScript personnalisé, l’envoi par défaut doit être désactivé explicitement en définissant une variable globale. `disableDefaultFormSubmission` to `true`.

| Nom | Description |
|--- |--- |
| submitForm | Cette méthode envoie le formulaire et gère le flux de post-envoi. |
| submitFormPartial | Cette méthode envoie également le formulaire, mais ignore le flux de post-envoi. Par exemple, si vous avez configuré la redirection vers la page de succès après l’envoi réussi, cette redirection ne se produira pas en cas d’envoi partiel du formulaire. |

**Exemples :**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## Fonction Utilitaire

| Nom | Description |
|--- |--- |
| getFormData | Cette méthode peut être utilisée pour obtenir la variable `formData` sous la forme d’un objet JSON. Cet objet peut être transmis à `submitForm` pour l’envoi du formulaire. |

**Exemple :**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## Cas dʼutilisation

### Cas d’utilisation 1 : Ajout de la validation avant l’envoi du formulaire

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### Cas d’utilisation 2 : Envoi partiel du formulaire

Par exemple, vous disposez d’un formulaire avec plusieurs cases à cocher sur la page. Lorsque vous cochez une case, vous souhaitez que ces données soient enregistrées dans le serveur principal sans attendre que l’utilisateur clique sur le bouton d’envoi.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### Cas d’utilisation 3 : Balises d’analyse personnalisées

Avec JavaScript, vous pouvez ajouter des écouteurs de champs de saisie et joindre un déclencheur d’appel Analytics personnalisé.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### Cas d’utilisation 4 : Formulaire dynamique

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
