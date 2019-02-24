
https://semantic-ui-vue.github.io/#/

1-) Para instalar o semantic ui : 
 
//gerador de dts
#npm install -g dts-gen
#npm install semantic-ui-vue --save 
#npm install semantic-ui --save
#cd src
#dts-gen -m semantic-ui-vue

2-)  Adicionar no tsconfig.json:

  "types": [
      "webpack-env",
+      "semantic-ui-vue",
+      "semantic-ui",
      "jest",
    ],


3-)  Adicionar no main.ts depois dos imports: 

...imports antigos
+// @ts-ignore
+import SuiVue from 'semantic-ui-vue';

E depois das configurações:

Vue.config.productionTip = false
+ Vue.use(SuiVue);


4-) Para testar: 

#No Javascript:
import SuiVue from 'semantic-ui-vue';
#Na View:
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.3.0/semantic.min.css"></link>
<sui-button primary>click me</sui-button>
