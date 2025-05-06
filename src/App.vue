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
            </div>
            <div class="cartoes">
                <ul>
                    <li><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQQfuHHe9EHCFcjCaFVsVQKwz6eIfccoIxApQ&s" alt="img-paypal"></li>
                    <li><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRpnA2ApcYtLFB3m9foinEhb0I_T159HIkEJQ&s" alt="img-mastercard"></li>
                    <li><img src="data:image/png;base64,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" alt="img-visa"></li>
                </ul>
            </div>
        </div>
            <p class="direitos-autorais">© Alguns direitos reservados. IFbooks 2025. </p>
        </footer>
    </body>
</template>

<style scoped>
footer {
    background: #27AE60;
    color: white;
    padding: 2vw;
}
footer div.informacoes{
    display: flex;
    justify-content: center;
}
footer ul {
    list-style: none;
    display: flex;
}
</style>
