
https://semantic-ui-vue.github.io/#/

1-) Para instalar o semantic ui : 
 #npm install semantic-ui-vue --save


2-)  Adicionar no main.js depois dos imports: 

...imports antigos
+ import SuiVue from 'semantic-ui-vue';

E depois das configurações:

Vue.config.productionTip = false
+ Vue.use(SuiVue);


3-) Para testar: 

#No Javascript:
import SuiVue from 'semantic-ui-vue';
#Na View:
<sui-button primary>click me</sui-button>
