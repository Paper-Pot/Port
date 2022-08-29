<script>

let workLinks = [
    {
        "id":"creata",
        "imageLink":"../src/assets/creata.png",
        "title":"Creata",
        "description":"A single page web application that can be used as a landing page.",
        "source":"https://paper-pot.github.io/Creata2.0/src/"
    },
    {
        "id":"qrCodeGen",
        "imageLink":"../src/assets/QrCodeGenerator.png",
        "title":"QR Code Generaator",
        "description":"Generates QR code for any Text or an URL, uses an API for Fetching Data",
        "source":"https://paper-pot.github.io/QRcodeGenerator/"
    },
    {
        "id":"toDoList",
        "imageLink":"../src/assets/toDoList.png",
        "title":"To Do List",
        "description":"Dynamic addition and deletion of TODO elements to the DOM.",
        "source":"https://paper-pot.github.io/To_Do/src/"
    },
    {
        "id":"scoreKeeper",
        "imageLink":"../src/assets/scoreKeeper.png",
        "title":"Score Recording Application",
        "description":"Small scale application to record the score for 2 player games",
        "source":"https://paper-pot.github.io/Scorekeeper/"
    }
]

</script>

<h1 class="gridHeader afterHighlight">Work Demo</h1>
<div class="workGridContainer">
  {#each workLinks as work}
    <div class="workCell {work.id}">
      <img class="workImg" src={work.imageLink} alt={work.id} />
      <h2 class="gridTitle">{work.title}</h2>
      <p>{work.description}</p>
      <a href={work.source} target="blank">Visit Demo</a>
    </div>
  {/each}
</div>

<style>

h1{
    position: relative;
    font-family: "DeathStar",sans-serif;
    position: relative;
    width: max-content;
    margin: 200px auto 50px;
    color: var(--textColorLight);
}
.afterHighlight::after{
    content: "";
    position: absolute;
    bottom: 6px;
    right: -15px;
    width: 10px;
    height: 70%;
    background-color: red;
  }
  .workGridContainer{
    padding: 40px;
    width: 100%;
    max-width: 1220px;
    margin: auto;
    display: grid;
    grid-template-areas: 
    "creata" "qr"
    "toDo" "scoreKeep";
    grid-gap: 50px;
  }
  .creata{ grid-area: creata;}
  .qrCodeGen{ grid-area: qr;}
  .toDoList{ grid-area: toDo;}
  .scoreKeeper{ grid-area: scoreKeep;}
  .workCell{
    width: 90%;
    min-width: 300px;
    margin: auto;
    background-color: var(--textColorDark2);
    padding: 30px;
    border-radius: 15px;
    transition: 0.3s ease;

    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .workCell:hover{
    background-color: var(--textColorDark);
  }
  .workCell img{
    width: 100%;
    max-height: 250px;
    object-fit: contain;
    border-radius: 5px;
  }
  .gridTitle{
    margin: 30px 0 20px;
    color: var(--textColorLight);
    text-align: center;
  }
  .workCell p{
    color: var(--textColorLight2);
    text-align: center;
    margin-bottom: 50px;
  }
  .workCell a{
    margin: auto;
    width: max-content;
    padding: 10px 20px;
    background-color: rgb(251, 45, 45);
    border-radius: 3px;
    color: var(--textColorLight);
    font-weight: 700;
    position: relative;

  }
  .workCell a::after{
    content: "";
    position: absolute;
    top: 50%;
    right: 0px;
    transform: translateY(-50%) scale(0);
    width: 15px;
    height: 15px;
    background-color: rgb(251, 45, 45);
    clip-path: polygon(0% 0%,100% 50%,0% 100%);
    transition: 0.5s ease;
  }
  .workCell a:hover{
    padding: 6px 16px;
    background-color: transparent;
    border: 4px solid red;
  }
  .workCell a:hover::after{
    right: -30px;
    transform: translateY(-50%) scale(1);
    clip-path: polygon(0% 0%,100% 50%,0% 100%);
  }
  @media (max-width:350px){
    .workGridContainer{
        padding: 10px;
    }
  }
  @media (min-width:860px){
    .workGridContainer{
        grid-template-areas: 
        "creata qr"
        "toDo scoreKeep";
    }
    .workCell{
        width: 100%;
    }
  }
</style>