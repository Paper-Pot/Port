<script>

</script>

<footer>
    <div class="container">
        <div class="logoContainer">
            <img src="../src/assets/logo.svg" alt="">
        </div>
        <div class="footerContainer">
            <ul class="contact">
                <li class="method method1"><a class="links" href="https://github.com/Paper-Pot"><img src="../src/assets/github.svg" class="logo" style=" filter:invert(100%)" alt="">Github</a></li>
                <li class="method method2"><a class="links" href="https://www.linkedin.com/in/banerjeerhitam/"><img src="../src/assets/linkedin.svg" class="logo" style=" filter:invert(100%)" alt="">Linked in</a></li>
                <li class="method method3"><a class="links" href="https://www.codechef.com/users/banerjeerhitam"><img src="../src/assets/codechef.svg" class="logo" style=" filter:invert(100%)" alt=""> CodeChef</a></li>
                <li class="method method4"><a class="links" href="mailto:banerjeerhitam1@gmail.com"><img src="../src/assets/outline.svg" class="logo" style=" filter:invert(100%)" alt="">Email</a></li>
            </ul>
        </div>
    </div>
    <div class="footerSpanEnd">
        <p>Made with <ion-icon name="heart" style="color: red; margin:0 5px;" ></ion-icon> by Rhitam</p>
    </div>


</footer>

<style>
    footer{
        padding:  50px;
        background-color: var(--textColorDark2);
    }
    .container{
        max-width: 1500px;
        margin: auto;
    }
    .logoContainer{
        max-width: 210px;
    }
    .logoContainer img{
        width: 100%;
    }
    .links{
        color: var(--textColorLight);
        font-weight: 500;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
    }
    .links img{
        margin-right: 10px;
    }
    .footerContainer{
        margin: auto;
        margin-top: 50px;
        width: 100%;
        height: 100%;
    }
    .contact{
        height: 100%;
        width: 100%;
        margin-top: auto;
        display: flex;
        /* flex-direction: column; */
        justify-content: space-around ;
    }
    .contact li{
        width: 100%;
    }
    .logo{
        max-width: 30px;
    }
    .footerSpanEnd{
        margin-top: 50px;
        text-align: center;
        color: var(--textColorLight2);
    }
    .footerSpanEnd p{
        display: flex;
        align-items:center;
        justify-content:center;
    }
    @media (max-width:600px){

        .footerContainer{
            height: 90%;
            padding: 0;
            flex-direction: column;
            justify-content: space-evenly;
        }
        .contact{
            display: grid;
            width: 100%;
            place-items: center;
            grid-template-areas: 
            "git linkedin"
            "email code"
            ;
            grid-gap: 40px;
        }
        .method1{grid-area: git;}
        .method2{grid-area: linkedin;}
        .method3{grid-area: code;}
        .method4{grid-area: email;}
    }

</style>