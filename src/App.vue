<script setup>
import { ref, computed } from 'vue';


const carrinho = ref([]);
const lancamentos =ref ([
   {
   id: "01",
   titulo: "Chain of Iron: Volume 2",
   autor: "Cassandra Clare",
   preco :23.24,
   capa:"https://m.media-amazon.com/images/I/81IP261kwlL.jpg",
   quantidade: 1,
   },
   {
   id: "02",
   titulo: "Chain of Thorns",
   autor: "Cassandra Clare",
   preco :23.24,
   capa:"https://m.media-amazon.com/images/I/91PtVqr8spL.jpg",
   quantidade: 1,
   },
   {
   id: "03",
   titulo: "City of Fallen Angels",
   autor: "Cassandra Clare",
   preco :13.94,
   capa:"https://m.media-amazon.com/images/I/81KL1LCy4bL._UF894,1000_QL80_.jpg",
   quantidade: 1,
   },
   {
   id: "04",
   titulo: "Nona the Ninth",
   autor: "Cassandra Clare",
   preco :16.84,
   capa:"https://m.media-amazon.com/images/I/81SiB5KufiL._UF894,1000_QL80_.jpg",
   quantidade: 1,
   },
   {
   id: "05",
   titulo: "Harlem Shuffle",
   autor: "Colson Whitehead",
   preco :26.92,
   capa:"https://m.media-amazon.com/images/I/81ZPFCh0xML.jpg",
   quantidade: 1,
   },
   {
   id: "06",
   titulo: "Two Old Women",
   autor: "Velma Wallis",
   preco :13.95,
   capa:"https://m.media-amazon.com/images/I/81Yo0MecUrL.jpg",
   quantidade: 1,
   },
   {
   id: "07",
   titulo: "Carrie Soto Is Back",
   autor: "Taylor Jenkins Reid",
   preco :26.04,
   capa:"https://thumb.spokesman.com/wdxMerykWELlZzs-g_JW0iILVis=/2500x2500/smart/media.spokesman.com/photos/2022/08/19/62fd217156308.image.jpg",
   quantidade: 1,
   },
   {
   id: "08",
   titulo: "Book Lovers",
   autor: "Emily Henry",
   preco :15.81,
   capa:"https://m.media-amazon.com/images/I/71Xy4AL7jKL._AC_UF1000,1000_QL80_.jpg",
   quantidade: 1,
   },
]);

function adicionarlancamentos(book) {
  const existente = carrinho.value.find(p => p.id === book.id);
  if (existente) {
    existente.quantidade++;
  } else {
    carrinho.value.push({ ...book }); // cria cópia do livro
  }
}

 function incrementar(book) {
  book.quantidade++
}

function decrementar(book) {
  book.quantidade--
  if (book.quantidade <= 0) {
    const index = carrinho.value.findIndex(p => p.id === book.id)
    if (index !== -1) {
      carrinho.value.splice(index, 1)
    }
  }
}

function subTotal(book) {
   return book.preco * book.quantidade;
}

const totalProdutos = computed(() => {
  return carrinho.value.reduce((soma, item) => {
    return soma + (item.preco * item.quantidade);
  }, 0);
});
const valorBooleano = ref(true);
 </script>

<template>
  <body>
      <header>
            <div>
                <div class="logo">
                <h1>IFBooks</h1>
                <p class="linha">Apreço <br> a leitura</p>
                </div>
                <div class="barra-de-pesquisa">
                <p>Pesquisar</p>
                <img src="/img/Search.png" alt="icone-de-lupa">
                </div>
            </div>
            <div class="menu">
                <nav>
                <ul>
                    <li>
                        <a href="#">Termos</a>
                    </li>
                    <li>
                        <a href="#">Equipe</a>
                    </li>
                    <li>
                        <a href="#">Envio</a>
                    </li>
                    <li>
                        <a href="#">Devoluções</a>
                    </li>
                    <li>
                        <img src="/img/Download.png" alt="carrinho" >
                    </li>
                    <li>
                        <span class="fa-solid fa-heart"></span>
                    </li>
                    <li>
                        <span class="fa-solid fa-user"></span>
                    </li>
                    </ul>
                </nav>
            </div>
        </header>
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
          <section class="lancamentos">
              <div id="loja">
               <h2>Lançamentos</h2>
               <ul>
                <li v-for="livro in lancamentos" :key="livro.id">
                  <p> <img :src="livro.capa" alt="" width="200" height="200"></p>
                  <p>{{ capa }}</p>
                  <p class="titulo">{{ livro.titulo }}</p>
                  <p class="autor">{{ livro.autor }}</p>
                  <p class="preco">{{ "R$" + livro.preco }}<i class="fa-solid fa-heart"></i></p>
                  <button class="botao" @click="adicionarlancamentos(livro)">compra</button>
                </li>
               </ul>  
              </div>
          </section>
          <section class="carrinho" v-if="carrinho.length > 0">
              <div class="classificacao">
                <h2>Carrinho</h2>
                <ul class="tabela">
                  <li>
                    Título
                  </li>
                  <li>
                    Quantidade
                  </li>
                  <li>
                    Subtotal
                  </li>
                </ul>
                <div class="compra" v-for="book in carrinho" :key="book.id">
                  <p>
                    <img :src="book.capa" alt="" width="150" height="200">
                  </p>
                  <p class="texto">
                    <p class="titulo"> {{ book.titulo }}</p>
                    <p class="autor">{{ book.autor }}</p>
                    <p class="preco">R$ {{ book.preco.toFixed(2) }}</p> 
                  </p>
                  <p class="quantidade">
                    <button @click="decrementar(book)">-</button>
                    {{ book.quantidade }}
                    <button @click="incrementar(book)">+</button>
                  </p>
                  <p class="subTotal">
                    R$ {{ subTotal(book).toFixed(2) }}
                  </p>
                </div>
                <p>
                  <a href="#loja">Voltar para loja</a>
                </p>
              </div>
              <div class="tabelas">
                <div class="total">
                  <form>
                    <label for="name">
                      <input type="text" id="name" name="user_name">
                    </label>
                    <p>
                      <input type="submit" value="Inserir Cupom">
                    </p>
                  </form>
                </div>
                <div class="resumo-compra">
                  <h3>Total da Compra</h3>
                  <div class="linha">
                   <span>Produtos:</span>
                   <span>R$ {{ totalProdutos.toFixed(2) }}</span>
                  </div>
                  <div class="linha">
                    <span>Frete:</span>
                    <span>Grátis</span>
                  </div>
                  <div class="linha total">
                    <span>Total:</span>
                     <span>R$ {{ totalProdutos.toFixed(2) }}</span>
                  </div>
                  <button class="botao-pagamento">Ir para o pagamento</button>
                </div>
              </div>
          </section>
        </main>
        <footer>
            <div class="informacoes">
              <div class="redes-sociais">
                <p>IFbooks</p>
                <ul>
                  <li><span class="fa-brands fa-square-facebook"></span></li>
                  <li><span class="fa-brands fa-square-instagram"></span></li>
                  <li><span class="fa-brands fa-square-twitter"></span></li>
                </ul>
              </div>
              <div class="contato">
                <h2>Contato</h2>
                <p> <img src="/img/phone.png" alt="telefone-img"> +55 47 40045263 </p>
                <p> <span class="fa-solid fa-clock"></span> 8h às 23h - Seg a Sex</p>
                <p> <span class="fa-solid fa-envelope"></span> contato@ifbooks.com</p>
                <ul>
                    <li><img src="/img/Paypal-Logo.png" alt="img-paypal"></li>
                    <li><img src="/img/MasterCard-Logo.png" alt="img-mastercard"></li>
                    <li><img src="/img/VISA-Logo.png" alt="img-visa"></li>
                </ul>
              </div>
            </div>
            <p class="direitos-autorais">© Alguns direitos reservados. IFbooks 2025. </p>
        </footer>
  </body>
</template>

<style scoped>
/*------------------------------
              TOPO
------------------------------*/
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 1vw 0 2vw 0;
    padding: 0 0 0.5vw 0;
    border-bottom: 1px solid #27AE60;
}
header div{
  display: flex;
  justify-content: center;
}
header div.logo{
    display: flex;
    margin: 0 4vw 0 0;
}
header div.logo h1{
    margin: 1vw 1vw 0 2vw;
}
header div.logo p.linha{
    border-left: 1px solid #27AE60;
    padding: 0 0 0 1vw;
    margin: 1vw 0 1.5vw 0;
    color: #27AE60;
    font-size: 1.05rem;
}
header div.barra-de-pesquisa{
    display: flex;
    margin:  1vw 1vw 1vw 1vw;
    padding: 10px;
}
header div.barra-de-pesquisa p{
    color: #B8B8B8;
    background-color: #F1F1F1;
    padding:  0.7vw 30vw 0.7vw 1vw;  
}
header div.barra-de-pesquisa img{
    background-color: #F1F1F1;
    padding:  0.7vw 1vw 0.7vw 0vw;
}
header nav ul{
    list-style: none;
    display: flex;
    margin: 0 5vw 0 0;
}
header nav ul li{
    margin: 0 1.1vw 0 1.1vw;
}
header nav ul li a{
    text-decoration: none;
    color: #7B7881;
}
header nav ul li span{
    color: #27AE60;
    font-size: 1.3rem;
    border-left: 1px solid #27AE60;
    padding: 0 0 0 20px;
}
main section.inicio{
display: flex;
justify-content: center;
margin: 2vw 4vw 2vw 4vw;
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
main section.inicio div.texto h2{
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
main section.inicio div.imagem{
margin: 0vw 0vw 5vw 4vw;
}
/*------------------------------
             FAIXA
------------------------------*/
main section.faixa div{
   border-top: 1px solid rgba(39,174,96,1);
   border-bottom:  1px solid rgba(39,174,96,1);
}
main section.faixa ul{
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
main section.faixa li p{
   font-weight: bold;
   font-size: 1rem;
   margin: 0px 30px 0px 0px;
}
main section.faixa li p img{
   height: 20px ;
   width: 20px;
  margin: 0px 10px 0px 0px;
}
/*------------------------------
          LANÇAMENTOS
------------------------------*/
section.lancamentos h2{
   margin: 4vw 6vw 4vw 10vw;
   font-weight: bold;
   font-size: 2rem;
   color: black;
}
section.lancamentos ul{
   display: flex;
   flex-wrap: wrap;
   justify-content: space-between;
   margin:4vw 7vw 4vw 6vw;
}
section.lancamentos li{
   box-sizing: border-box;
   width: 20%;
   margin: 2vw 1vw 0vw 0;
   padding: 0 1vw;
   white-space: nowrap;
   list-style: none;
}
section.lancamentos img{
   width: 15vw;
   height: 20vw;
}
section.lancamentos ul button{
   padding: 10px 6vw 10px 6vw;
   border: 1px solid rgba(39,174,96,1);
   background-color:  rgba(39,174,96,1);
   color:white; 
}
section.lancamentos li p{
   margin: 8px;
}
section.lancamentos li p.titulo{
   font-weight: bold;
   font-size: 1.2rem;
}
section.lancamentos li p.autor{
   color: rgb(147, 146, 148);
}
section.lancamentos li p.preco{
   font-weight: bold;
   font-size: 1.2rem;
}
section.lancamentos li p.preco i{
   color : rgba(39,174,96,1);
   margin: 0 0 0 6vw;
}
/*------------------------------
           CARRINHO 
------------------------------*/
section.carrinho div.classificacao h2{
    color: rgba(39,174,96,1);
    font-size: 2.3em;
    font-weight: bold;
    margin-left: 10vw;
}
section.carrinho div.classificacao ul.tabela{
    display: flex;
    list-style: none;
    margin-left: 10vw;
    margin-right: 10vw;
    justify-content: center;
    border-bottom: 2px solid rgb(95, 219, 147);
}
section.carrinho div.classificacao ul.tabela li{
    font-size: 1.4rem;
    font-weight: bold;
    margin-bottom: 2vw;
    margin-top: 2vw;
    padding: 0 15vw 0 10vw;
}
section.carrinho div.classificacao div.compra{
   display: flex;
   border-bottom: 1px solid #BDBDBD;
   margin-left: 10vw;
   margin-right: 10vw;
}
section.carrinho div.classificacao div.compra p{
   margin : 40px 1vw 0px 1vw;
}
section.carrinho div.classificacao div.compra p.texto p.titulo{
   font-size: 1.3rem;
   font-weight: bold;
   margin: 1%;
}
section.carrinho div.classificacao div.compra p.texto p.autor{
   margin: 1%;
   padding: 10px 0 10px 0;
}
section.carrinho div.classificacao div.compra p.texto p.preco{
   margin: 1%;
   font-weight: bold;
   font-size: 1.1rem;
}
section.carrinho div.classificacao div.compra p.quantidade{
   margin : 40px 26vw 20px 10vw;
   border: 1px solid #000000;
   padding: 10px 20px 10px 20px;
   margin-bottom: 14vw;
   font-weight: bold;
}
section.carrinho div.classificacao div.compra p.quantidade button{
   border: none;
   background: transparent;
}
section.carrinho div.classificacao div.compra p.subTotal{
   font-size: 1.2rem;
   font-weight: bold;
}
section.carrinho div.classificacao a{
    color: black;
    text-decoration: none;
    border: 1px solid black;
    border-radius: 3px;
    padding: 10px 50px 10px 50px;
}
section.carrinho div.classificacao p{
    margin: 5vw 10vw 5vw 10vw;
}
section.carrinho div.tabelas {
   display: flex;
}
section.carrinho div.total form{
    display: flex;
    margin: 1vw 10vw 1vw 8vw;
}
section.carrinho div.total form p input{
   border: none;
   padding: 1vw 2vw 1vw 2vw;
   margin: 1vw 1vw 1vw 1vw;
   border-radius: 2px;
   background-color: rgba(39,174,96,1); 
   color: white;
   font-size: 1.1rem;
}
section.carrinho div.total form label input{
 border-radius: 2px;
 border-color: black;
 padding:1.1vw 4vw 1.1vw 4vw;
 margin: 1vw 1vw 1vw 2vw;
}
section.carrinho div.resumo-compra{
  border: 1px solid #000000;
  border-radius: 5px;
  padding: 2vw 2vw 2vw 2vw;
  width: 400px;
  margin: 1vw 1vw 1vw 10vw;
  font-family: Arial, sans-serif;
}
section.carrinho div.resumo-compra h3{
  font-size: 1.2rem;
  font-weight: bold;
  margin-bottom: 1vw;
}
section.carrinho div.resumo-compra div.linha{
  display: flex;
  justify-content: space-between;
  margin-bottom: 1vw;
}
section.carrinho div.resumo-compra .total{
  font-weight: bold;
  border-top: 1px solid #ccc;
  padding-top: 1vw;
  margin-top: 1vw;
}
section.carrinho div.resumo-compra button.botao-pagamento{
  background-color: rgba(39,174,96,1);
  color: white;
  border: none;
  border-radius: 4px;
  padding: 10px 20px;
  width: 100%;
  margin-top: 1vw;
  cursor: pointer;
  font-size: 1.1rem;
  }
/*------------------------------
             RODAPÉ 
------------------------------*/
footer{
    background: #27AE60;
    color: white;
    padding: 0 0 2vw 0;
}
footer div.informacoes{
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid rgba(255, 255, 255, 1);
}
footer div{
    padding: 2vw 2vw 2vw 2vw;
}
footer div.informacoes div.redes-sociais{
    margin: 0 0 0 6vw;
}
footer div.informacoes div.redes-sociais p{
    padding: 0 0 0.2vw 2.6vw;
    font-size: 1.3rem;
    color: rgba(255, 255, 255, 1);
}
footer div.informacoes div.redes-sociais ul{
    list-style: none;
    display: flex; 
}
footer div.informacoes div.redes-sociais ul li span{
    font-size: 1.8rem;
    padding: 10px;
    color: rgba(255, 255, 255, 1);
}
footer div.informacoes div.contato{
    margin: 0 0 0 45vw;
}
footer div.informacoes div.contato h2{
    font-size: 1.3rem;
    font-weight: 500;
    padding: 0 0 1.5vw 0;
}
footer div.informacoes div.contato p{
    color: rgba(255, 255, 255, 0.8);
    padding: 0 0 1vw 0;
    font-size: 1.1rem;
}
footer div.informacoes div.contato p span{
    padding: 0 10px 0 0 ;
    color: rgba(255, 255, 255, 0.8);
}
footer div.informacoes div.contato ul{
    list-style: none;
    display: flex;
    padding: 2vw 6vw 0 0 ;
}
footer div.informacoes div.contato ul li{
    padding: 0 30px 0 0;
}
footer div.informacoes div.contato ul li img{
   width: 120%;
   height: 90%;
   border-radius: 4px;
}
footer p.direitos-autorais{
    text-align: center;
    font-size: 1.2rem;
    color: rgba(255, 255, 255, 0.6);
    padding: 1.5vw 0 0 0;
}
</style>