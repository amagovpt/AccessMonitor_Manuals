![image](lib/images/logo/fcul_logo.png)

![image](lib/images/logo/FCiencias_ID.png)

  

  

31 of January of 2019

Faculdade de Ciências da Universidade de Lisboa

# Introduction

This manual explains how to translate the suite of applications to
another languages.

# Requirements

  - Knowledge about a JSON structure

  - The application source code

# How to translate

To have all the translations working correctly two major steps are
required. Repeat these two steps for each application.

## Step 1: Create a new language file

1.  Go to the application’s root folder

2.  Go to the folder **src/assets/i18n/** (figure
    [\[fig:i18n\_folder\]](#fig:i18n_folder) shows an example for the
    AMP application). The **English.json** and **Portuguese.json** files
    must exist in that folder.

3.  Create a new JSON file. Name it the new language in English (ex.:
    **Spanish.json**). The first letter of the name must be uppercase.

4.  Copy all the contents of the **English.json** file to the new file

5.  Translate all the English sentences to the new language, except in
    the “LANGUAGES” substructure

6.  Inside the file find the “LANGUAGES” substructure (figure
    [\[fig:languages\_substructure\]](#fig:languages_substructure))
    
    1.  Add your language to the substructure. The key is the name of
        the language in English. The value is the name of the language
        in the language (ex.: “Spanish”: “Español”)
    
    2.  Repeat the previous step for all language files

![Language files location
example](lib/images/translate/i18n_folder.png)

<span id="fig:i18n_folder" label="fig:i18n_folder">\[fig:i18n\_folder\]</span>

![JSON file, “LANGUAGES”
substructure](lib/images/translate/languages_substructure.png)

<span id="fig:languages_substructure" label="fig:languages_substructure">\[fig:languages\_substructure\]</span>

## Step 2: Add the new language to the code

1.  Go to the application’s root folder

2.  Go to the folder **src/app/**

3.  Open the **app.component.ts** file

4.  Find the languages structures (figure
    [\[fig:code\_lang\_structures\]](#fig:code_lang_structures))

5.  Add the language to the **langs** structure (ex.: “es”: “Spanish”)

6.  Add the language code to the **langCodes** structure (ex.:
    “Spanish”: “es”)

7.  Change the default language and backup language in case of missing
    translations (figure
    [\[fig:code\_default\_lang\]](#fig:code_default_lang))
    
    1.  In line 43 and 49 change the language **Portuguese** to the
        desired default language

8.  Go to the folder **src/** inside the application’s root folder

9.  Open the **index.html** file

10. Change the attribute **lang** from the **html** tag to the desired
    lang code, figure
    [\[fig:html\_code\_default\_lang\]](#fig:html_code_default_lang),
    line 2

![Languages structures in the
code](lib/images/translate/code_lang_strcuture.png)

<span id="fig:code_lang_structures" label="fig:code_lang_structures">\[fig:code\_lang\_structures\]</span>

![Definition of the default language in the
code](lib/images/translate/code_default_lang.png)

<span id="fig:code_default_lang" label="fig:code_default_lang">\[fig:code\_default\_lang\]</span>

![Definition of the default language in the **index.html**
file](lib/images/translate/index_html_lang.png)

<span id="fig:html_code_default_lang" label="fig:html_code_default_lang">\[fig:html\_code\_default\_lang\]</span>

# Testing

Launch the application, and open it in the browser, go to the footer of
the page and try to change the page language in the selection box at the
right. If the translations don’t show up correctly, just clean up the
browser cache.
