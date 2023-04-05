 <template>
   <div class="final">

     <div :class="`final-texto ${etapa}`">
       {{texto}}
     </div>
     <button
         class="final-botao"
         @click="jogarNovamente"
         >Mais Umazinha ???</button>

   </div>
 </template>

 <script>

 export default {
   // eslint-disable-next-line vue/multi-word-component-names
   name: 'Final',
   props:{
     etapa: String,
     texto: String,
     jogarNovamente: Function

   },
   data(){
     return{
     }
   },
   methods:{
   }
 }
 </script>

 <style>

 .final-texto{
   margin:20px 0;
   font-size: 24px;
   font-weight: bold;
 }

 .final-texto.enforcado{
   color: var(--color-text-error);
 }

 .final-texto.ganhador{
   color: var(--color-text-success);
 }

 </style>