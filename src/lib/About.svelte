<script>

  import {fade,slide,fly} from "svelte/transition";
  // @ts-ignore
  import SkillsAnimate from "./SkillsAnimate.svelte";
  import Works from "./Works.svelte";


</script>

<div class="container">
  <div class="aboutLeft">
      <img src="../src/assets/about.svg" alt="">
  </div>
  <div class="aboutRight">
    <div class="aboutMe">
      <h1 class="afterHighlight">About M e</h1>
      <p>
        I am a Web Developer with an intrest to explore the tech stacks around and build some intresting projects.<br>
        During leasure i preffer playing tabla, helps me to get insight.<br> 
        Mainly i am programmer using c++ to solve problems, but have been learning about web stacks which intrigues.
      </p>
    </div>
  </div>
</div>

<SkillsAnimate/>
<Works />
<!-- https://paper-pot.github.io/QRcodeGenerator/ -->
<!-- https://paper-pot.github.io/To_Do/src/ -->
<!-- https://paper-pot.github.io/Creata2.0/src/ -->
<!-- https://paper-pot.github.io/Scorekeeper/ -->

<style>
  .container {
    padding: 0 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    max-width: 1500px;
    text-align: center;
    margin: auto;
  }
  .aboutMe{
    text-align: center;
    color: var(--textColorLight);
  }
  h1{
    position: relative;
    font-family: "DeathStar",sans-serif;
    position: relative;
    width: max-content;
  }
  .aboutMe h1{
    margin: auto;
    margin-bottom: 50px;
  }
  .afterHighlight::after{
    content: "";
    position: absolute;
    /* top: -5px; */
    bottom: 6px;
    right: -15px;
    /* transform: translateY(-50%); */
    width: 10px;
    height: 70%;
    background-color: red;
  }
  .aboutMe p{
    font-weight: 300;
    max-width: 1000px;
  }
  .aboutLeft {
    width: 100%;
  }
  .aboutLeft img{
    width: 100%;
    max-width: 500px;
  }
  .aboutRight {
    margin-top: 100px;
    width: 100%;
  }
  @media (min-width: 860px) {
    .container {
      padding: 0 50px;
      flex-direction: row;
    }
    .aboutMe{
      text-align: left;
      color: var(--textColorLight);
    }
    .aboutMe h1{
      margin: 0;
      margin-bottom: 100px;
    }
    .aboutLeft {
      width: 50%;
    }
    .aboutRight {
      width: 50%;
    }
  }
</style>
