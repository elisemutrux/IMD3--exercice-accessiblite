# Exercice accessibilité

Rendez vous sur la page `index.html`. Celle-ci a été conçu par quelqu'un qui ne connait rien aux normes d'accessibilité. A vous de faire en sorte d'améliorer ce formulaire !

Les formulaires sont parmi les éléments des sites internets les moins accessibles. Parmi les erreurs courantes:

- Absence de labels associés aux champs de formulaire
- Manque d’indications pour les champs obligatoires
- Absence de navigation clavier
- Contrastes insuffisants
- Placeholders utilisés à la place des labels

## Installation

```
npm install
npm run dev
```

## Etape 1

Utilisez l'extension chrome "Wave" pour déterminer les points d'amélioration. Modifiez le code HTML et / ou SCSS afin de régler les problèmes.

Pensez

- à utiliser des balises sémantiques lorsque c'est possible
- à utiliser les (bons) attributs, notamment pour les éléments `<input>`
- au contraste des couleurs
- à la taille du texte, afin qu'elle soit relative aux préférences de l'utilisateur·trice

## Etape 2

Modifiez le SCSS en exploitant les fonctionnalités de cette outil, notamment la création de variables.

En SCSS, une variable se définit ainsi:

1. Créez un fichier `_variables.scss` et importez le **tout en haut** de `main.scss`
2. Dans le fichier `_variables.scss`, donnez un nom et une valeur à votre variable. Par exemple:

```
$myColor: green; /* Variable se nomme $myColor et a pour valeur "green" */
$myFontSize: 12px; /* Variable se nomme $myFontSize et a pour valeur "12px" */
```

3. Utilisez ensuite vos variables à chaque fois que la valeur de votre variable est présente dans le SCSS. Par exemple:

```
.my-element {
  font-size: 12px;
  color: black;
  background-color: green;
}
```

devient

```
.my-element {
  font-size: $myFontSize;
  color: black;
  background-color: $myColor;
}
```
