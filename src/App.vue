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
                <p class="pesquisar">Pesquisar</p>
                <img src="/img/Search.png" alt="icone-de-lupa">
                </div>
            </div>
            <div>
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
                    <p><img src="/img/Download.png" alt="carrinho" ></p>
                </li>
                <li>
                    <p><i class="fa-solid fa-heart"></i></p>
                </li>
                <li>
                    <p><i class="fa-solid fa-user"></i></p>
                </li>
            </ul>
            </div>
        </header>
    </body>
</template>

<style scoped>
/*------------------------------
            TOPO
-------------------------------*/
header {
    display: flex;
    justify-content: space-between;
}
header div{
  display: flex;
  margin: 2vw 2vw 0 2vw;
}
header div.logo {
    display: flex;
    margin: 0 2vw 0 0;
}
header div.logo p.linha {
    border-left: 2px solid #27AE60;
    margin: 0.4vw 2vw 4.4vw 1vw;
    padding: 0 0 0 10px;
    color: #27AE60;
    font-size: 1rem;
}
header div.barra-de-pesquisa {
    display: flex;
    padding: 5px 0vw 5px 5px;
    background-color: #F1F1F1;
    margin: 0 0 5vw 2vw;
}
header div.barra-de-pesquisa p.pesquisar {
    font-size: 1.2rem ;
    padding: 0.5vw 30vw 0 2vw ;
    color: #B8B8B8;
}
header div.barra-de-pesquisa img {
    width: 80%;
    height: 100%;
    padding: 0.9vw 2vw 0.5vw 0;
    
}
header nav ul {
    list-style: none;
    display: flex;
    
}
header nav ul li {
    padding: 1vw 2vw 2vw 0;
}
header nav ul li a {
    text-decoration: none;
    color: #7B7881;
}
header ul {
    list-style: none;
    display: flex;
}
header ul li {
    padding: 1vw 2vw 2vw 0vw;
}
header ul li i {
    color: #27AE60;
    font-size: 1.3rem;
    border-left: 2px solid #27AE60;
    padding: 0 0 0 10px;
}
</style>
