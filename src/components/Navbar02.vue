<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
</script>

<template>
  <nav class="navbar">
    <ul class="menuderoulant" :class="{ open: menuOpen }">
      <li>
        <a href="#">Geoservices</a>
        <ul class="sousmenu">
            <li><a href="#">Géomatique</a></li>
            <li><a href="#">Topographie</a></li>
            <li><a href="#">Aménagement</a></li>
            <li><a href="#">Urbanisme</a></li>
            <li><a href="#">Assainissement</a></li>
            <li><a href="#">Lotissement</a></li>
        </ul>
    </li>
      <li>
        <a href="#">FranShop</a>
        <ul class="sousmenu">
          <li><a href="#"> Habits & T-shirts </a></li>
          <li><a href="#">Sous-menu 2</a></li>
          <li><a href="#">Sous-menu 3</a></li>
          <li><a href="#">Sous-menu 4</a></li>
        </ul>
      </li>

      <li>
        <a href="#">Services de livraisons</a>
        <ul class="sousmenu">
          <li><a href="#">Sous-menu 1</a></li>
          <li><a href="#">Sous-menu 2</a></li>
          <li><a href="#">Sous-menu 3</a></li>
          <li><a href="#">Sous-menu 4</a></li>
        </ul>
      </li>

      <li>
        <a href="#">Map </a>
        <ul class="sousmenu">
          <li><router-link to="/map"> Ma carte </router-link></li>
          <li><a href="#">Sous-menu 2</a></li>
          <li><a href="#">Sous-menu 3</a></li>
          <li><a href="#">Sous-menu 4</a></li>
        </ul>
      </li>
      <li>
        <a href="#">🔍 Recherche</a>
        <ul class="sousmenu">
          <li><a href="#">Sous-menu 1</a></li>
          <li><a href="#">Sous-menu 2</a></li>
          <li><a href="#">Sous-menu 3</a></li>
          <li><a href="#">Sous-menu 4</a></li>
        </ul>
      </li>
      <li>
        <a href="#">Contact</a>
        <ul class="sousmenu">
          <li><a href="#">Mail: koffifrancois1990@gmail.com</a></li>
          <li><a href="#">⋮+228 96 40 44 26 </a></li>
          <li><a href="#"> Tel: +228 70 93 69 13 </a></li>
        </ul>
      </li>
       <li>
        <a href="#"> ☰ Paramètre</a>
        <ul class="sousmenu">
          <li><a href="#">Sous-menu 1</a></li>
          <li><a href="#">Sous-menu 2</a></li>
          <li><a href="#">Sous-menu 3</a></li>
          <li><a href="#">Sous-menu 4</a></li>
        </ul>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.menuderoulant {
    height: 0px;
    list-style: none;
    padding: 0px;
    margin: 0px;
}

.menuderoulant li {
    float: left;
    width: 200px;
}

.menuderoulant li a:link, .menuderoulant li a:visited{
    display: block;
    color: #FFFFFF;
    background: #293245;
    padding: 6px 10px;
    border-right: 1PX solid #ffffff;
    text-align: center;
    text-decoration: none;
}

.menuderoulant li a:hover { background-color: #1998D2;}
.menuderoulant li a:active{background-color: #808080;}

.menuderoulant  .sousmenu{
    list-style-type: none;
    display: none;
    padding: 0;
    margin: 0;
    position: absolute;
}
.menuderoulant .sousmenu li {
    float: none;
    margin:0 ;
    padding: 0;
    border-top: 1px solid transparent;
    border-right: 1px solid transparent;
}

.menuderoulant .sousmenu li a:link, .menuderoulant li a:visited{
    display: block;
    color: #eae9f0;
    text-decoration: none;
    background-color: #0890eb;
}

.menuderoulant .sousmenu li a:hover {
    background-color: #1998D2;
}

.menuderoulant .sousmenu li :hover{
    display: block;
}

.menuderoulant li:hover  .sousmenu{
    display: block;
}




</style>
