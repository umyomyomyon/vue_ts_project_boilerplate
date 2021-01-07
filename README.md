`vue create project-name`
```
Vue CLI v4.5.10
? Please pick a preset:
  Default ([Vue 2] babel, eslint)
  Default (Vue 3 Preview) ([Vue 3] babel, eslint)
❯ Manually select features
```
```
Vue CLI v4.5.10
? Please pick a preset: Manually select features
? Check the features needed for your project:
 ◉ Choose Vue version
 ◉ Babel
 ◉ TypeScript
 ◯ Progressive Web App (PWA) Support
 ◉ Router
 ◉ Vuex
 ◉ CSS Pre-processors
 ◉ Linter / Formatter
❯◉ Unit Testing
 ◯ E2E Testing
```
```
Vue CLI v4.5.10
? Please pick a preset: Manually select features
? Check the features needed for your project: Choose Vue version, Babel, TS, Rou
ter, Vuex, CSS Pre-processors, Linter, Unit
? Choose a version of Vue.js that you want to start the project with (Use arrow
keys)
❯ 2.x
  3.x (Preview)
```
```
? Use class-style component syntax? No
? Use Babel alongside TypeScript (required for modern mode, auto-detected polyfi
lls, transpiling JSX)? Yes
? Use history mode for router? (Requires proper server setup for index fallback
in production) Yes
? Pick a CSS pre-processor (PostCSS, Autoprefixer and CSS Modules are supported
by default): Sass/SCSS (with node-sass)
? Pick a linter / formatter config: Prettier
? Pick additional lint features: Lint on save
? Pick a unit testing solution: Jest
? Where do you prefer placing config for Babel, ESLint, etc.? In package.json
```
```
vue add vuetify
```
vuetifyを入れると、main.tsで No overload matches this call. というエラーが起こる  
この場合は、tsconfig.jsonのtypesの中に "vuetify" を追加する  
```
"types": [
      "webpack-env",
      "jest",
      "vuetify"
    ],
```
Vue2系でComposition APIを使用するために @vue/composition-api を導入する  
```
yarn add @vue/composition-api
```
tsconfig.jsonに追加した項目  
```
"noImplicitAny": false,
"isolatedModules": true,
"noUnusedParameters": true,
"noFallthroughCasesInSwitch": true,
"forceConsistentCasingInFileNames": true,
```

# ↓default README.md↓ 

# obj_nodesass

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Run your unit tests
```
yarn test:unit
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
