<script setup>
import { computed, ref } from 'vue';
</script>

<template>
 <body>
   <main>
     <section class="inicio">
     <div class="texto">
       <p class="autor">
        <button> Autor de Abril</button>
       </p>
       <h2>
         Eric-Emanuel Schmitt
       </h2>
       <p class="informacao">
         Eric-Emmanuel Schmitt has been awarded more than 20 <br> literary prizes and distinctions, and in 2001 he received the<br> title of Chevalier des Arts et des Lettres. His books have been <br> translated into over 40 languages.
       </p>
       <p>
        <button>Acessar página do livro</button>
       </p>
     </div>
     <div class="imagem">
       <img src="/img/schmitt.png" alt="schmitt">
     </div>
   </section>
   <section class="faixa">
  <div>
    <ul>
        <li>
         <p><img src="/img/caminhao.png" alt="caminhao">Frete grátis para SC</p> 
        </li>
        <li>
            <p><img src="/img/estrela.png" alt="estrela">Livros recomendados</p>
        </li>
        <li>
            <p><img src="/img/livro.png" alt="">Mais vendidos</p>
        </li>
    </ul>
  </div>
  <p>
        kkkkkkkkkkkk
    </p>
   </section>
   </main>
 </body>
</template>

<style scoped>

main section.inicio {
 display: flex;
 justify-content: center;
 margin: 4vw 6vw 4vw 6vw;
}
main section.inicio div.texto{
    margin: 8vw 0vw 5vw 4vw;
}
main section.inicio div.texto p.autor button{
padding: 10px 10px 10px 10px;
border: 1px solid rgba(39,174,96,1);
background-color: white;
color: rgba(39,174,96,1);
}
main section.inicio div.texto h2 {
 margin: 1vw 0vw 0vw 0vw;
 font-weight:bold;
 font-size: 3rem;

}
main section.inicio p.informacao{
 font-size: 1rem;
 margin: 2vw 0vw 2vw 0vw;
}
main section.inicio p button{
 padding: 10px 20px 10px 20px;
border: 1px solid rgba(39,174,96,1);
background-color:  rgba(39,174,96,1);
color:white
}
main section.inicio div.imagem {
 margin: 0vw 0vw 5vw 4vw;
}
/*/////////////////////////////////////
                FAIXA
///////////////////////////////////*/

main section.faixa div {
    border-top: 1px solid rgba(39,174,96,1);
    border-bottom:  1px solid rgba(39,174,96,1);
}
main section.faixa ul {
    justify-content: center;
    display: flex;
    list-style: none;
    margin: 3vw 0vw 3vw 0vw;
}
main section.faixa li{
    padding: 0px 50px 0px 0px;
}
main section.faixa li p {
    font-weight: bold;
    margin: 0px 30px 0px 0px;
}
main section.faixa li p img {
    height: 20px ;
    width: 20px;
   margin: 0px 10px 0px 0px;
}

</style>





