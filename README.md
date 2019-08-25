# Vuetify with vue-property-decorator and vue-class-component

Projeto criado com o comando:
```
# vue create -d -n <nome_do_projeto>
```
Antes de adicionar o vuetify, o projeto possui as alterações:
```
# yarn add vue-property-decorator vue-class-component
```
Foi adicionado o parametro no parserOptions do eslintConfig no package.json
```
"ecmaFeatures": {
    "legacyDecorators": true
}
```
Além do parametro no rules:
```
 "no-console": "off"
``` 
O componente App foi convertido para classe.

### Nesse ponto o build funciona ###
----
Após essas alterações, o Vuetify foi instalado com:
```
# vue add vuetify
```
E o componente App foi convertido para classe igual a versão antes do vuetify.

### Nesse ponto o build falha ###

```
ERROR  Failed to compile with 1 errors                                                                                                   
 error  in ./src/App.vue?vue&type=script&lang=js&

Module parse failed: Unexpected character '@' (28:0)
File was processed with these loaders:
 * ./node_modules/vuetify-loader/lib/loader.js
 * ./node_modules/cache-loader/dist/cjs.js
 * ./node_modules/vue-loader/lib/index.js
You may need an additional loader to handle the result of these loaders.
| import HelloWorld from './components/HelloWorld';
|
> @Component({
|     components: {
|         HelloWorld,

 @ ./src/App.vue?vue&type=script&lang=js& 1:0-211 1:227-230 1:232-440 1:232-440
 @ ./src/App.vue
 @ ./src/main.js
 @ multi ./src/main.js

 ERROR  Build failed with errors.
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```