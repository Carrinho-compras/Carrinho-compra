<script setup>
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
    </body>
</template>

<style scoped>
/*------------------------------
            TOPO
-------------------------------*/

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
header div.barra-de-pesquisa {
    display: flex;
    margin:  1vw 1vw 1vw 1vw;
    padding: 10px;
}
header div.barra-de-pesquisa p {
    color: #B8B8B8;
    background-color: #F1F1F1;
    padding:  0.7vw 30vw 0.7vw 1vw;
    
}
header div.barra-de-pesquisa img {
    background-color: #F1F1F1;
    padding:  0.7vw 1vw 0.7vw 0vw;
}
header nav ul {
    list-style: none;
    display: flex;
    margin: 0 5vw 0 0;
}
header nav ul li {
    margin: 0 1.1vw 0 1.1vw;
}
header nav ul li a {
    text-decoration: none;
    color: #7B7881;
}
header nav ul li span {
    color: #27AE60;
    font-size: 1.3rem;
    border-left: 1px solid #27AE60;
    padding: 0 0 0 20px;
}
</style>
