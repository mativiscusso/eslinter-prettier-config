# eslinter-prettier-config

###### Manual de instrucciones para inicializar un proyecto con las bondades que ofrecen ambos paquetes a la hora de mantener un codigo limpio

1-

```bash
yarn add eslint -D
```

2-

```bash
npx eslint --init
```

3- How would you like to use ESLINT?
`To check syntax, find problems and enforce code style`

4- What type of modules does your project use?
`JavaScript modules`

5- Which framework does your project use?
`React`

6- Does your project use TypeScript?
`No`

7- Where does your code run?
`Browser & Node` (press < space > to select)

8- How would you like to define a style for yout project?
`Guide > Standard`

9- What format do you want yout config file to be in?
`JavaScript`

10-

```bash
yarn add eslint-plugin-react eslint-config-standard  eslint-plugin-import eslint-plugin-node eslint-plugin-promise -D
```

11- Crear un script en el `package.json`
`"lint": "eslint . --fix"`

12-

```bash
yarn add eslint-config-prettier -D
```

13- Agregar `prettier` al array de `extends` en el archivo `.eslintrc.js`

14- Instalar Prettier

```bash
yarn add prettier -D
```

15- Crear un archivo llamado `.prettierrc.js ` e introducirle el siguiente codigo:

```js
module.exports = {
    trailingComma: "es5",
    tabWidth: 4,
    semi: false,
    singleQuote: true,
};
```

16- Correr el script `npx prettier . --check`
17- Añadir el archivo `.prettierignore` para ignorar las carpetas necesarias
18- Correr el script `npx prettier . --write`
19- Para una mejor experiencia a la hora de integrar estas correcciones de codigo, es necesario instalar las extensiones **Prettier** y **ESLint** y configurar el VS Code para que el formateo automatico lo haga con estas extensiones.
Para ello debemos agregar/modificar en el `settings.json` de VS Code lo siguiente:

```json
{
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    }
}
```

Para mas informacion visitar:

-   [Prettier]('https://prettier.io/docs/en/configuration.html)
-   [ESLint]('https://eslint.org/docs/user-guide/getting-started')
