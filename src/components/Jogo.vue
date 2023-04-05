 <template>
   <div class="jogo">

     <Forca
         :erros="erros"
     />
     <Palavra
         :palavra="palavra"
         :dica="dica"
         :verificarLetra="verificarLetra"
         :etapa="etapa"
     />
     <Teclado
         v-if="etapa === 'jogo'"
         :letras="letras"
         :verificarLetra="verificarLetra"
         :jogar="jogar"
     />

     <Final
         v-if="etapa !== 'jogo'"
         :etapa="etapa"
         :texto="etapa === 'ganhador' ? 'Boa Piazão, acertou !!' : 'Ai que bobo, errou feio !!'"
         :jogarNovamente="jogarNovamente"/>

   </div>
 </template>

 <script>
 import Forca from "./Forca";
 import Palavra from "./Palavra";
 import Teclado from "./Teclado";
 import Final from "./Final";

 export default {
   // eslint-disable-next-line vue/multi-word-component-names
   name: 'Jogo',
   props:{
     erros: Number,
     palavra: String,
     dica: String,
     etapa: String,
     verificarLetra: Function,
     letras: Array,
     jogar: Function,
     jogarNovamente: Function
   },
   data(){
     return{

     }
   },
   methods:{

   },
   components:{
     Forca,
     Palavra,
     Teclado,
     Final
   }
 }
 </script>

 <style>

 .jogo{
   width: 100%;
   display: flex;
   flex-direction: column;
   align-items: center;
   text-align: center;
 }
 </style>