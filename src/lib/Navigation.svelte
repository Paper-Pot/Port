<script>
import MediaQueries from "./MediaQueries.svelte";

// import { createEventDispatcher } from 'svelte';

let styles = {
    'rect_bg_color': '#000'
};

let burgerClicked = false;

function clickFun(){
    burgerClicked = !burgerClicked
    if(burgerClicked){
         styles.rect_bg_color = "#fff"
    }else{
        styles.rect_bg_color = "#000"
    }
}

$: cssVarStyles = Object.entries(styles)
		.map(([key, value]) => `--${key}:${value}`)
		.join(';');


// const dispatch = createEventDispatcher();

// function grantAccess() {

//     dispatch('message', {
//         text: "About To be Redirected to GitHub"
//     });
// }

</script>

<nav>
    <div class="logoContainer">
        <img src="../src/assets/logo.svg" alt="">
    </div>

    <MediaQueries query="(min-width: 501px)" let:matches>
        {#if matches}
            <div class="menuContainer">
                <ul class="menu">
                    <li><a target="blank" href="https://www.linkedin.com/in/banerjeerhitam/" class="navLinks">Linked In</a></li>
                    <li><a target="blank" href="https://github.com/Paper-Pot" class="navLinks">GitHub</a></li>
                    <li><a target="blank" href="https://www.codechef.com/users/banerjeerhitam" class="navLinks">CodeChef</a></li>
                </ul>
            </div>
        {/if}
    </MediaQueries>

    <MediaQueries query="(max-width: 500px)" let:matches>
        {#if matches}
        <div class="mobileMenuContainer" class:removeMenu="{burgerClicked}">
            <ul class="mobileMenu" >
                <li><a target="blank" href="https://www.linkedin.com/in/banerjeerhitam/" class="navLinks">Linked In</a></li>
                <li><a target="blank" href="https://github.com/Paper-Pot" class="navLinks">GitHub</a></li>
                <li><a target="blank" href="https://www.codechef.com/users/banerjeerhitam" class="navLinks">CodeChef</a></li>
            </ul>
        </div>
        <div class="burger" on:click="{clickFun}">
            <div class="rect" style="{cssVarStyles}" class:rectClicked="{burgerClicked}"></div>
        </div>
        {/if}
    </MediaQueries>

</nav>

<style>
nav{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: rgba(255, 175, 1, 0.971);
    z-index: 9;
}
.logoContainer{
    width: 50%;   
    max-width: 200px;
}
.logoContainer img{
    width: 100%;
}
.menuContainer{
    margin-left: auto;
    width: 100%;
    max-width: 500px;
}
.menu{
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-around;
}
.navLinks{
    color: var(--textColorLight);
    font-weight: 500;
    position: relative;
}
.navLinks::after{
    content: "";
    position: absolute;
    bottom: -5px;
    left: 50%;
    transform: translateX(-50%);
    height: 4px;
    width: 0%;
    border-radius: 20px;
    background-color: var(--textColorDark);
    z-index: -1;
    transition: 0.5s ease;
}
.navLinks:hover::after{
    width: calc(100% + 10px);
}
.burger{
    position: fixed;
    top: 40px;
    right: 40px;
    z-index: 10;
}
.rect{
    position: relative;
    width: 30px;
    height: 3px;
    margin: 3px 0;
    background-color: var(--rect_bg_color);
    border-radius: 20px;
}
.rect::before,.rect::after{
    content: "";
    position: absolute;
    width: 30px;
    height: 3px;
    background-color: var(--rect_bg_color);
    border-radius: 20px;
}
.rect::before{
    top: -7px;
    left: 0;
}
.rect::after{
    top: 7px;
    left: 0;
}
.mobileMenuContainer{
    position: fixed;
    top: 0px;
    right: 0px;
    width: 100%;
    max-width: 400px;
    height: 100%;
    background: rgba(0, 0, 0, 0.925);
    clip-path: circle(0% at calc(100% - 55px) calc(0% + 40px));
    transition: 1s ease;
}
.mobileMenu{
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: center;
    align-items: center;
}
.removeMenu{
    clip-path: circle(100%);
}
.rectClicked{
    background: transparent;
}
.rectClicked::before{
    transform: rotate(45deg);
    transform-origin: 6px 6px;
}
.rectClicked::after{
    transform: rotate(-45deg);
    transform-origin: 7px -1px;
}
@media (max-width:500px){
    .mobileMenu{
        width: 100%;
        text-align: center;
    }
    .mobileMenu li{
        width: 100%;
        /* background-color: burlywood; */
        display: flex;
    }
    .mobileMenu li a{
        padding: 40px;
        width: 100%;
        /* background-color: red; */
    }
    .mobileMenu li a:hover{
        background-color: var(--textColorDark2);
    }
    .mobileMenu li a::after{
        display: none;
    }
}
</style>