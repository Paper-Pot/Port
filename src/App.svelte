<script>
  import Preloader from "./lib/Preloader.svelte";
  import Header from "./lib/Header.svelte";
  import Navigation from "./lib/Navigation.svelte";
  import About from "./lib/About.svelte";
  import Footer from "./lib/Footer.svelte";

  import { spring } from 'svelte/motion';
  import {onMount} from "svelte";

  //---------- pre-loader
  let isPageLoaded = false;
  
  onMount(()=>{
    setTimeout(()=>{
      isPageLoaded = true;
      style.dispProp = "all";
    },700)
  })

  let style = {
    "dispProp":"none"
  };

  $: cssVarStyles = Object.entries(style)
		.map(([key, value]) => `--${key}:${value}`)
		.join(';');

  //---------- export from header
  let source  

  // -------- custom cursor position
  let coords = spring({ x:0, y:0}, {
    stiffness: 5,
    damping: 2
  });

  let size = spring(1);

  // ---------- header redirect message
  function handleMessage(event) {
      if(confirm(event.detail.text)){
        source = "https://github.com/Paper-Pot";
      }
  }

</script>

<svelte:window
  on:mousemove="{e => coords.set({ x: e.clientX, y: e.clientY })}"
  on:mouseup="{() => size.set(1)}"
  on:mousedown="{() => size.set(3)}"/>

  {#if (!isPageLoaded)}
    <Preloader />
  {/if}

<main >

  <!--  custom cursor -->
  <div class="ball" style="left :{$coords.x - 10}px; top: {$coords.y -10}px; transform: scale({$size})">
    <div class="innerBall"></div>
  </div>


  <div class="components" style="{cssVarStyles}">
    
    <Navigation />

    <Header on:message="{handleMessage}" {source}/>

    <div class="container">
      <About />
    </div>

    <Footer />
  
  </div>

</main>

<style>
  .components{
    display: var(--dispProp);
  }
.ball{
  position: fixed;
  height: 25px;
  width: 25px;
  border-radius: 50%;
  background: red;
  border: 3px solid white;
  z-index: 10;
  /* mix-blend-mode: difference; */
  pointer-events: none;
}
.container{
  position: relative;
  background-color: var(--textColorDark);
  margin-top: 200px;
  padding-bottom: 100px;
}
.container::before,.container::after{
  content: "";
  position: absolute;
  top: -50px;
  width: 100%;
  height: 200px;
  background-color: var(--textColorDark);
  z-index: -1;
}
.container::before{
  transform: skewY(5deg);
}
.container::after{
  transform: skewY(-5deg);
}

  
</style>
