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