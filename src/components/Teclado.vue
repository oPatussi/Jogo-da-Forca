 <template>
   <div class="teclado">

     <button
         class="teclado-botao"
         v-for="(letra,key) in 'abcdefghijklmnopqrstuvwxyz'"
         :key="key"
         :disabled="verificarLetra(letra)"
         @click="jogar(letra)"
     >
       {{letra}}
     </button>

   </div>
 </template>

 <script>

 export default {
   // eslint-disable-next-line vue/multi-word-component-names
   name: 'Teclado',
   props:{
     letras: Array,
     verificarLetra: Function,
     jogar: Function
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

  .teclado{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 85%;
    margin-top: 20px;
  }
  .teclado-botao{
    margin: 5px;
    text-transform: uppercase;
  }


 </style>