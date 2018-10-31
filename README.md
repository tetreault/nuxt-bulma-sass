# Bulma/SASS/Nuxt Demo

Dead simple demo of just getting bulma and sass working on a nuxt project.

## Build Setup

Run these steps:

```bash
# when you run this, select Bulma as the style module
$ create-nuxt-app PROJECT_NAME

# install these dependencies needed for SASS
$ npm i --save-dev nuxt-sass-resources-loader vue-style-loader node-sass sass-loader

# run this in the project directory created by create-nuxt-app
$ npm run dev

# create a global styles file
$ touch assets/css/main.scss
```

## Global CSS file SASS imports

Add this to the top of your `assets/css/main.scss` file:

```css
@import "~bulma/sass/utilities/_all.sass";
@import "~bulma/bulma";
```

## Update nuxt.config.js modules array

Update your nuxt.config.js file so the modules array looks like this:

```javascript
  modules: [
    ['nuxt-sass-resources-loader', './assets/main.scss']
    // we dont need bulma imported here anymore, since we import it in assets/css/main.scss
    // '@nuxtjs/bulma'
  ],
```
