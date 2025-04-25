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
        <li class="borda">
         <p><img src="/img/caminhao.png" alt="caminhao">Frete grátis para SC</p> 
        </li>
        <li class="borda">
            <p><img src="/img/estrela.png" alt="estrela">Livros recomendados</p>
        </li>
        <li>
            <p><img src="/img/livro.png" alt="livro">Mais vendidos</p>
        </li>
    </ul>
  </div>
   </section>
   <section class="lançamentos">
    <div>
      <h1>Lançamentos</h1>
      <ul>
        <li>
          <p><img src="/img/vestido-amarelo.png" alt="vestido-amarelo"></p>
          <h3>Chain of Iron: Volume 2</h3>
          <p>Cassandra Clare</p>
          <h3 class="coracao">R$23.24 <img src="/img/coracao.png" alt="coracao"></h3>
          <button>compra</button>
        </li>
        <li>
          <p><img src="/img/vestido-verde.png" alt="vestido-verde"></p>
          <h3>Chain of Thorns</h3>
          <p>Cassandra Clare</p>
          <h3 class="coracao">R$23.24 <img src="/img/coracao.png" alt="coracao"></h3>
          <button>compra</button>
        </li>
        <li>
          <p><img src="/img/chicote.png" alt="chicote"></p>
          <h3>City of Fallen Angels</h3>
          <p>Cassandra Clare</p>
          <h3 class="coracao">R$13.94 <img src="/img/coracao.png" alt="coracao"></h3>
          <button>compra</button>
        </li>
        <li>
          <p><img src="/img/anjo.png" alt="anjo"></p>
          <h3>Nona the Ninth</h3>
          <p>Cassandra Clare</p>
          <h3 class="coracao">R$16.84 <img src="/img/coracao.png" alt="coracao"></h3>
          <button>compra</button>
        </li>
      </ul>
    </div>
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
    margin: 0vw 5vw 0vw 5vw;
}
main section.faixa li.borda{
    padding: 0px 50px 0px 0px;
    margin: 0vw 5vw 0vw 5vw;
    border-right: 1px solid rgba(147, 125, 194, 1);
}

main section.faixa li p {
    font-weight: bold;
    font-size: 1rem;
    margin: 0px 30px 0px 0px;
}
main section.faixa li p img {
    height: 20px ;
    width: 20px;
   margin: 0px 10px 0px 0px;
}
/*/////////////////////////////
         LANÇAMENTOS 
/////////////////////////////*/
main section.lançamentos div{
  margin: 4vw 4vw 4vw 4vw;
}
main section.lançamentos div ul {
  display: flex;
  margin: 30px;
}
main section.lançamentos div p img  {
  height:25vw ;
  width: 17vw;
}
main section.lançamentos div h1{
   font-weight: bold;
}
main section.lançamentos div ul li {
  margin: 1vw 2vw 1vw 1vw;
  list-style: none;
}
main section.lançamentos div ul li h3{
  font-weight: bold;
}
main section.lançamentos div ul li p{
  color: rgba(79, 76, 87, 1);
}
main section.lançamentos div ul li h3 img {
 height: 17px;
 width: 20px;
 text-align: right;
}
main section.lançamentos div ul li h3.coracao{
  justify-content: space-between;
}
main section.lançamentos div button{
  height:5vw;
  width:15vw;
  font-size: 1rem;
  border: 20px solid white;
  background-color: rgba(39,174,96,1);
  color: white;
}



</style>





