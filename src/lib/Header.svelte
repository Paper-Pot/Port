<script>
    
    export let source

    import draw from "svelte-transitions-draw";
    import { quintOut } from 'svelte/easing';
    
    import { createEventDispatcher } from 'svelte';

    let duration = 5500



    setTimeout(()=>{
        document.querySelectorAll("path").forEach(path =>{
            path.style.fill = "#fff"
        })
        document.querySelectorAll(".pathBlack").forEach(pathBlack =>{
            // @ts-ignore
            pathBlack.style.fill = "#000";
        })
    },duration-500)


    const dispatch = createEventDispatcher();

    function grantAccess() {
		dispatch('message', {
			text: "About To be Redirected to GitHub"
		});
	}

</script>
<header>

<div class="introContainer">
    <div class="intro introLeft">
        <svg width="359" height="72" viewBox="0 0 359 72" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path class="pathBlack loadFirst" d="M29.472 19.544V53H25.104V37.832H8.064V53H3.696V19.544H8.064V34.232H25.104V19.544H29.472Z"/>
            <path class="pathBlack loadFirst" d="M39.952 22.424C39.12 22.424 38.416 22.136 37.84 21.56C37.264 20.984 36.976 20.28 36.976 19.448C36.976 18.616 37.264 17.912 37.84 17.336C38.416 16.76 39.12 16.472 39.952 16.472C40.752 16.472 41.424 16.76 41.968 17.336C42.544 17.912 42.832 18.616 42.832 19.448C42.832 20.28 42.544 20.984 41.968 21.56C41.424 22.136 40.752 22.424 39.952 22.424ZM42.064 26.696V53H37.696V26.696H42.064Z"/>
            <path class="pathBlack loadFirst" d="M55.36 19.544L54.832 43.544H51.184L50.656 19.544H55.36ZM53.2 53.288C52.368 53.288 51.664 53 51.088 52.424C50.512 51.848 50.224 51.144 50.224 50.312C50.224 49.48 50.512 48.776 51.088 48.2C51.664 47.624 52.368 47.336 53.2 47.336C54 47.336 54.672 47.624 55.216 48.2C55.792 48.776 56.08 49.48 56.08 50.312C56.08 51.144 55.792 51.848 55.216 52.424C54.672 53 54 53.288 53.2 53.288Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' class="pathBlack" d="M80.064 19.544V53H75.696V19.544H80.064Z"/>            
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' class="pathBlack" d="M98.064 39.752C98.064 37.064 98.608 34.712 99.696 32.696C100.784 30.648 102.272 29.064 104.16 27.944C106.08 26.824 108.208 26.264 110.544 26.264C112.848 26.264 114.848 26.76 116.544 27.752C118.24 28.744 119.504 29.992 120.336 31.496V26.696H124.752V53H120.336V48.104C119.472 49.64 118.176 50.92 116.448 51.944C114.752 52.936 112.768 53.432 110.496 53.432C108.16 53.432 106.048 52.856 104.16 51.704C102.272 50.552 100.784 48.936 99.696 46.856C98.608 44.776 98.064 42.408 98.064 39.752ZM120.336 39.8C120.336 37.816 119.936 36.088 119.136 34.616C118.336 33.144 117.248 32.024 115.872 31.256C114.528 30.456 113.04 30.056 111.408 30.056C109.776 30.056 108.288 30.44 106.944 31.208C105.6 31.976 104.528 33.096 103.728 34.568C102.928 36.04 102.528 37.768 102.528 39.752C102.528 41.768 102.928 43.528 103.728 45.032C104.528 46.504 105.6 47.64 106.944 48.44C108.288 49.208 109.776 49.592 111.408 49.592C113.04 49.592 114.528 49.208 115.872 48.44C117.248 47.64 118.336 46.504 119.136 45.032C119.936 43.528 120.336 41.784 120.336 39.8Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' class="pathBlack" d="M164.328 26.216C166.376 26.216 168.2 26.648 169.8 27.512C171.4 28.344 172.664 29.608 173.592 31.304C174.52 33 174.984 35.064 174.984 37.496V53H170.664V38.12C170.664 35.496 170.008 33.496 168.696 32.12C167.416 30.712 165.672 30.008 163.464 30.008C161.192 30.008 159.384 30.744 158.04 32.216C156.696 33.656 156.024 35.752 156.024 38.504V53H151.704V38.12C151.704 35.496 151.048 33.496 149.736 32.12C148.456 30.712 146.712 30.008 144.504 30.008C142.232 30.008 140.424 30.744 139.08 32.216C137.736 33.656 137.064 35.752 137.064 38.504V53H132.696V26.696H137.064V30.488C137.928 29.112 139.08 28.056 140.52 27.32C141.992 26.584 143.608 26.216 145.368 26.216C147.576 26.216 149.528 26.712 151.224 27.704C152.92 28.696 154.184 30.152 155.016 32.072C155.752 30.216 156.968 28.776 158.664 27.752C160.36 26.728 162.248 26.216 164.328 26.216Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' d="M213.312 53L205.344 39.32H200.064V53H195.696V19.544H206.496C209.024 19.544 211.152 19.976 212.88 20.84C214.64 21.704 215.952 22.872 216.816 24.344C217.68 25.816 218.112 27.496 218.112 29.384C218.112 31.688 217.44 33.72 216.096 35.48C214.784 37.24 212.8 38.408 210.144 38.984L218.544 53H213.312ZM200.064 35.816H206.496C208.864 35.816 210.64 35.24 211.824 34.088C213.008 32.904 213.6 31.336 213.6 29.384C213.6 27.4 213.008 25.864 211.824 24.776C210.672 23.688 208.896 23.144 206.496 23.144H200.064V35.816Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' d="M237.752 26.216C239.736 26.216 241.528 26.648 243.128 27.512C244.728 28.344 245.976 29.608 246.872 31.304C247.8 33 248.264 35.064 248.264 37.496V53H243.944V38.12C243.944 35.496 243.288 33.496 241.976 32.12C240.664 30.712 238.872 30.008 236.6 30.008C234.296 30.008 232.456 30.728 231.08 32.168C229.736 33.608 229.064 35.704 229.064 38.456V53H224.696V17.48H229.064V30.44C229.928 29.096 231.112 28.056 232.616 27.32C234.152 26.584 235.864 26.216 237.752 26.216Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' d="M255.952 22.424C255.12 22.424 254.416 22.136 253.84 21.56C253.264 20.984 252.976 20.28 252.976 19.448C252.976 18.616 253.264 17.912 253.84 17.336C254.416 16.76 255.12 16.472 255.952 16.472C256.752 16.472 257.424 16.76 257.968 17.336C258.544 17.912 258.832 18.616 258.832 19.448C258.832 20.28 258.544 20.984 257.968 21.56C257.424 22.136 256.752 22.424 255.952 22.424ZM258.064 26.696V53H253.696V26.696H258.064Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' d="M271.024 30.296V45.8C271.024 47.08 271.296 47.992 271.84 48.536C272.384 49.048 273.328 49.304 274.672 49.304H277.888V53H273.952C271.52 53 269.696 52.44 268.48 51.32C267.264 50.2 266.656 48.36 266.656 45.8V30.296H263.248V26.696H266.656V20.072H271.024V26.696H277.888V30.296H271.024Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' d="M282.064 39.752C282.064 37.064 282.608 34.712 283.696 32.696C284.784 30.648 286.272 29.064 288.16 27.944C290.08 26.824 292.208 26.264 294.544 26.264C296.848 26.264 298.848 26.76 300.544 27.752C302.24 28.744 303.504 29.992 304.336 31.496V26.696H308.752V53H304.336V48.104C303.472 49.64 302.176 50.92 300.448 51.944C298.752 52.936 296.768 53.432 294.496 53.432C292.16 53.432 290.048 52.856 288.16 51.704C286.272 50.552 284.784 48.936 283.696 46.856C282.608 44.776 282.064 42.408 282.064 39.752ZM304.336 39.8C304.336 37.816 303.936 36.088 303.136 34.616C302.336 33.144 301.248 32.024 299.872 31.256C298.528 30.456 297.04 30.056 295.408 30.056C293.776 30.056 292.288 30.44 290.944 31.208C289.6 31.976 288.528 33.096 287.728 34.568C286.928 36.04 286.528 37.768 286.528 39.752C286.528 41.768 286.928 43.528 287.728 45.032C288.528 46.504 289.6 47.64 290.944 48.44C292.288 49.208 293.776 49.592 295.408 49.592C297.04 49.592 298.528 49.208 299.872 48.44C301.248 47.64 302.336 46.504 303.136 45.032C303.936 43.528 304.336 41.784 304.336 39.8Z"/>
            <path transition:draw='{{delay:0, easing: quintOut,duration}}' d="M344.328 26.216C346.376 26.216 348.2 26.648 349.8 27.512C351.4 28.344 352.664 29.608 353.592 31.304C354.52 33 354.984 35.064 354.984 37.496V53H350.664V38.12C350.664 35.496 350.008 33.496 348.696 32.12C347.416 30.712 345.672 30.008 343.464 30.008C341.192 30.008 339.384 30.744 338.04 32.216C336.696 33.656 336.024 35.752 336.024 38.504V53H331.704V38.12C331.704 35.496 331.048 33.496 329.736 32.12C328.456 30.712 326.712 30.008 324.504 30.008C322.232 30.008 320.424 30.744 319.08 32.216C317.736 33.656 317.064 35.752 317.064 38.504V53H312.696V26.696H317.064V30.488C317.928 29.112 319.08 28.056 320.52 27.32C321.992 26.584 323.608 26.216 325.368 26.216C327.576 26.216 329.528 26.712 331.224 27.704C332.92 28.696 334.184 30.152 335.016 32.072C335.752 30.216 336.968 28.776 338.664 27.752C340.36 26.728 342.248 26.216 344.328 26.216Z"/>
        </svg>

        <div class="introPara">
            <h2><span class="backPadd">Frontend</span> <span class="invert">Developer</span></h2>
            <p>Passionate about web design and development, writting clean and reusable code</p>
            <div class="linkAndAnimation">
                <div class="linkContainer" on:click="{grantAccess}">
                    <a href="{source}" class="links introLink">How I Work</a>
                </div>
                <div class="scrollIndicator">
                    <div class="outerIndicator">
                        <div class="innerIndicator"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="intro introRight">
        <img src="src/assets/hero4.jpg" alt="HERO BANNER">
    </div>
</div>

</header>

<style>

header{
    position: relative;
    height: 70vh;
    max-width: 1500px;
    margin: auto;
    margin-top: 170px;
}
.introContainer{
    position: relative;
    width: 100%;
    height: 100%;
    padding-left: 50px;
}
.introLeft{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    z-index: 2;
}
svg{
    width: 100%;
    max-width: 450px;
    transform: scale(1.3);
}
path {
    stroke : #fff;
    fill: none;
    stroke-width: 2px;
    transition: 3.5s ease-in-out;
}
.pathBlack{
    stroke: #000;
}
.loadFirst{
    fill: #000;
}
.introLeft svg:nth-child(2){
    margin-left: 10px;
}
.introPara{
    margin-top: 30px;
    width: 100%;
    max-width: 500px;
}
.introPara h2{
   font-weight: 600; 
}
.introPara p{
    margin: 20px 0 30px;
}
.introLink{
    color: var(--textColorLight);
    background-color: var(--textColorDark);
    border-radius: 30px;
    padding: 15px 20px;
    transition: 0.6s ease;
}
.introLink{
    transform : translateY(0px)
}
.introLink:hover{
    transform: translateY(10px);
    box-shadow: 0 0px 10px rgb(44, 44, 44);
}
.linkAndAnimation{
    display: flex;
}
.scrollIndicator{
    margin: -15px 0 0 15px;
}
.outerIndicator{
    width: 20px;
    height: 50px;
    background-color: var(--textColorLight);
    border-radius: 20px;
    display: grid;
    place-items: center;
}
.innerIndicator{
    margin-top: -30px;
    width: 14px;
    height: 14px;
    clip-path: circle(50% at 50%);
    background-color: red;
    animation : 1s translateBall 1s cubic-bezier(0.74,-0.02, 0.58, 1.3) alternate infinite;
}
.introRight{
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 100%;
    max-width: 800px;
    z-index: -1;
    background-color: var(--baseColor);
}
.introRight img{
    width: 100%;
}
.invert{
    color: var(--textColorLight);
}
.backPadd{
    padding: 10px;
    background-color: var(--textColorLight);
}
@media (max-width: 1100px){
    header{
        margin-top: 100px;
    }
    .introContainer{
        padding-left: 0;
    }
    svg{
        margin-left: 0;
    }
    .introLeft{
        width: 100%;
        top: 10%;
        left: 50%;
        transform: translateY(0%);
        transform: translateX(-50%);
        text-align: center;
    }
    .introPara{
        margin: auto;
        margin-top: 30px;
    }
    .linkAndAnimation{
        justify-content: center;   
    }
    .linkContainer{
        margin-left: 40px;
    }
    .introRight{
        top: 40%;
        right: 50%;
        transform: translateX(50%);
    }
}
@media (max-width:500px){
    .introRight{
        top: 50%;
    }
    svg{
        transform: scale(1);
    }
}
@media (max-width:370px){
    
    svg{
        transform: scale(0.8);
    }
}
   
@keyframes translateBall{
    from{
        transform: translateY(0%);
    }
    to{
        transform: translateY(30px);
    }
}

</style>