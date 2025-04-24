<script setup>
</script>

<template>
    <body>
        <header>
            <div class="logo">
                <h1>IFBooks</h1>
                <p class="linha">Apreço <br> a leitura</p>
            </div>
            <p>Pesquisar <img src="/img/Search.png" alt="icone-de-lupa"></p>
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
                </ul>
            </nav>
            <ul>
                <li>
                    <p><img src="/img/Download.png" alt="carrinho"> |</p>
                </li>
                <li>
                    <p><img src="/img/heart active.png" alt="favoritos"> |</p>
                </li>
                <li>
                    <p><img src="/img/User.png" alt="usuario"> |</p>
                </li>
            </ul>
        </header>
    </body>
</template>

<style scoped>
body header {
  display: flex;
  margin: 2vw;
}
body header div.logo {
    display: flex;
    margin: 0 2vw 0 0;
}
body header div.logo p {
    border-left: 1px solid #27AE60;
    margin: 0.9vw 2vw 0.9vw 2vw;
}
</style>
