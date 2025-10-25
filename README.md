📘 2. README — Mode d’emploi
----------------------------

### 🧩 Présentation

**replace\_vars\_docx** est un script Python permettant de **remplacer automatiquement des variables** dans un document Word .docx à partir d’un fichier JSON.Idéal pour générer automatiquement des thèses, rapports, lettres, contrats, etc.

### ⚙️ Installation

1.  Installe Python 3.8 ou supérieur
    
2.  pip install python-docx
    
3.  Place le script replace\_vars\_docx.py dans ton projet
    

### 📂 Structure d’exemple

`   /projet_these/  │  ├── these_modele.docx  ├── variables.json  ├── replace_vars_docx.py  └── output/      └── these_finale.docx   `

### 🧾 Exemple de variables (variables.json)

`   {    "auteur": "Marie Dubois",    "titre_these": "Étude des systèmes dynamiques complexes",    "universite": "Université de Toulouse",    "annee": "2025",    "directeur": "Pr. Laurent Bernard"  }   `

### 📄 Exemple dans Word (these\_modele.docx)

   Thèse de doctorat de [[auteur]]  Titre : [[titre_these]]  Université : [[universite]]  Année : [[annee]]  Directeur : [[directeur]]   `

### 🚀 Exécution

  python replace_vars_docx.py these_modele.docx variables.json output/these_finale.docx "[[" "]]"   `

### ✅ Résultat

  Thèse de doctorat de Marie Dubois  Titre : Étude des systèmes dynamiques complexes  Université : Université de Toulouse  Année : 2025  Directeur : Pr. Laurent Bernard   `

### 🧠 Options

ParamètreDescriptionPar défautDocument Word modèle—Fichier JSON avec les variables—Document Word généré—\[delimiteur\_gauche\]Délimiteur d’ouverture{{\[delimiteur\_droit\]Délimiteur de fermeture}}

### 💡 Bonnes pratiques

*   Utilise des délimiteurs **peu ambigus**, ex. \[\[nom\]\] plutôt que {{nom}} si tu as des accolades dans le texte.
    
*   Le script **préserve toute la mise en forme** (titres, tableaux, légendes, styles).
    
*   Les variables peuvent être utilisées dans :
    
    *   Les titres (Heading 1, 2, etc.)
        
    *   Les tableaux
        
    *   Les en-têtes et pieds de page
        

### 🧩 Exemple avancé

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   python replace_vars_docx.py rapport.docx data/variables.json rapport_final.docx "<<", ">>"   `

Variables dans le Word :

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   <> — <>  Rédigé le <>   `

### 📄 Licence

Libre d’utilisation pour tout usage personnel ou professionnel.Auteur : _Ton Nom / Ton Organisation_Version : **1.0 (2025)**

Souhaites-tu que je t’ajoute un **exemple de variables imbriquées** (comme \[\[universite.nom\]\]) avec lecture JSON profonde ?Cela permettrait de gérer des structures complexes de données (utile pour de vraies thèses ou rapports institutionnels).

##### You said:

les dependances a installer?

###### ChatGPT said:

Excellente question 👌 — tu as raison : avant d’exécuter le script, il faut s’assurer que **toutes les dépendances Python** nécessaires sont installées.Voici la liste complète, avec explication, commandes d’installation et gestion des environnements.

⚙️ **1\. Dépendances nécessaires**
----------------------------------

Le script repose principalement sur une seule librairie externe :

### 🧩 python-docx

*   📦 Nom sur PyPI : python-docx
    
*   💡 Sert à lire, modifier et enregistrer des fichiers Word (.docx)
    
*   🔗 Documentation : https://python-docx.readthedocs.io/
    

Commandes d’installation :

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   pip install python-docx   `

### 🧰 Dépendances standards (déjà incluses dans Python)

Ces modules sont intégrés dans Python, tu n’as **pas besoin de les installer** :

*   json → pour lire le fichier JSON de variables
    
*   sys → pour lire les arguments en ligne de commande
    
*   os → (optionnel si tu veux manipuler des chemins de fichiers)
    

📦 **2\. Optionnel : création d’un environnement virtuel**
----------------------------------------------------------

C’est recommandé pour éviter les conflits entre versions de librairies.

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   # Créer un environnement virtuel  python -m venv venv  # Activer l'environnement  # (Windows)  venv\Scripts\activate  # (macOS / Linux)  source venv/bin/activate  # Installer la dépendance dans cet environnement  pip install python-docx   `

📁 **3\. Fichier requirements.txt (facultatif mais pratique)**
--------------------------------------------------------------

Tu peux créer un fichier requirements.txt à la racine du projet :

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   python-docx>=0.8.11   `

Et ensuite installer tout d’un coup :

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   pip install -r requirements.txt   `

🧪 **4\. Vérification**
-----------------------

Pour vérifier que la bibliothèque est bien installée :

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   python -m pip show python-docx   `

Tu devrais voir un message du genre :

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   Name: python-docx  Version: 0.8.11  Summary: Create and update Microsoft Word .docx files.   `

✅ En résumé
-----------

DépendanceInstallationRôlepython-docxpip install python-docxLecture et modification du fichier .docx(inclus : json, sys, os)—Fonctions standard Python
