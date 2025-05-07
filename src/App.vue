<script setup>
</script>

<template>
    <body>
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
                <p> <img src="/img/Icon.png" alt="telefone-img"> +55 47 40045263 </p>
                <p> <span class="fa-solid fa-clock"></span> 8h às 23h - Seg a Sex</p>
                <p> <span class="fa-solid fa-envelope"></span> contato@ifbooks.com</p>
                <ul>
                    <li><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQQfuHHe9EHCFcjCaFVsVQKwz6eIfccoIxApQ&s" alt="img-paypal"></li>
                    <li><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRpnA2ApcYtLFB3m9foinEhb0I_T159HIkEJQ&s" alt="img-mastercard"></li>
                    <li><img  class="img" src="https://img2.gratispng.com/20180522/apq/avqf1ih87.webp" alt="img-visa"></li>
                </ul>
            </div>
        </div>
            <p class="direitos-autorais">© Alguns direitos reservados. IFbooks 2025. </p>
        </footer>
    </body>
</template>

<style scoped>
footer{
    background: #27AE60;
    color: white;
    padding: 0 0 3vw 0;
}
footer div.informacoes{
    display: flex;
    justify-content: space-between;
}
footer div{
    padding: 2vw;
}
footer div.informacoes div.redes-sociais p{
    padding: 0 0 0 3.2vw;
    font-size: 1.3rem;
    color: rgba(255, 255, 255, 0.8);
}
footer div.informacoes div.redes-sociais ul{
    list-style: none;
    display: flex; 
}
footer div.informacoes div.redes-sociais ul li span{
    font-size: 1.6rem;
    padding: 10px;
    color: rgba(255, 255, 255, 1);
}
footer div.informacoes div.contato {
    margin: 0 0 0 55vw;
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
}
footer div.informacoes div.contato ul li img{
   width: 100%;
   height: 80%;
   border-radius: 5px;
}
footer div.informacoes div.contato ul li img.img{
    width: 30%;
    height: 50%;
}
</style>1