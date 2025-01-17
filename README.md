﻿# Lazy Chameleon
A simple theme manager built with javascript to handle all the theme changes for your website/webapp.

## Setup

To use this library, import the 'lazychameleon.js' and add a 'themes.json' in your project.

### Create a themes.json file with this structure

```json
[
    {
        "name": "light",
        "colors": [
            {
                "name": "--text-color",
                "value": "#040316"
            },
            {
                "name": "--background-color",
                "value": "#fbfbfe"
            },
        ]
    },
]
```

### Your CSS must also have the names of the colors in your themes.json file

```css
:root {
    --text-color: #040316;
    --background-color: #fbfbfe;
}
```

## Usage

To create an instance of `LazyChameleon`, pass the following two parameters to the constructor:

```javascript
const lazychameleon = new LazyChameleon('project-name', 'themes.json');
```

### Built-in functions


```javascript
setTheme('themename')
```
This will set the theme you selected as the new theme and save a token in your browser

```javascript
getStoredTheme()
```
This will get the current theme that is stored locally in your browser

```javascript
sendChangeThemeEvent('themename')
```
This will send a message to all tabs of your project to change their theme 

## Demonstration
Example 1 simple use of Lazy Chameleon

https://github.com/user-attachments/assets/757b4a78-a0bd-4cfd-98d6-c9a6a07e0b8f

Example 2 syncing with other tabs

https://github.com/user-attachments/assets/b43f010e-caf9-416a-9ca8-4b862bb37dee






