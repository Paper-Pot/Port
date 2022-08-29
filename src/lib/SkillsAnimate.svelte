<script>
// @ts-nocheck

    import { Swiper, SwiperSlide } from "swiper/svelte";
    // import required modules
    import { Autoplay, Pagination, Navigation } from "swiper";
  
    // Import Swiper styles
    import "swiper/css";
    import "swiper/css/autoplay";
    import "swiper/css/pagination";
    import "swiper/css/navigation";
  

    let sources = {
        "html": "../src/assets/html.png",
        "css": "../src/assets/css.png",
        "sass": "../src/assets/sass.png",
        "git":"../src/assets/Git.png",
        "js":"../src/assets/js.png",
        "svelte":"../src/assets/svelte.png",
        "adobeXd":"../src/assets/adobeXd.png",
        "gimp":"../src/assets/gimp.png"
    }

  </script>
  

  <h1 class="gridHeader afterHighlight">Tools I use</h1>
  <Swiper
    slidesPerView={0.5}
    autoplay={{
        delay: 1,
        disableOnInteraction: false,
    }}
    breakpoints={{
        1220:{
            slidesPerView:2
        },
        400:{
            slidesPerView:1
        }
    }}
    speed={5000}
    loop={true}
    pagination={{
      clickable: true,
    }}
    navigation={true}
    modules={[Autoplay, Pagination, Navigation]}
    
  >
    
        <SwiperSlide >
            <div class="langGridContainer">
                <div class="langCell cell1 langHtml">
                    <img class="langImg" src={sources.html} alt=Html />
                </div>
                <div class="langCell cell2 langJs">
                    <img class="langImg" src={sources.js} alt=Js />
                </div>
            </div>
        </SwiperSlide>
        <SwiperSlide >
            <div class="langGridContainer invertOrientation">                
                <div class="langCell cell1 ">
                    <img class="langImg" src={sources.css} alt=Css />
                </div>
                <div class="langCell cell2 ">
                    <img class="langImg" src={sources.svelte} alt=svelte />
                </div>
            </div>
        </SwiperSlide>
        <SwiperSlide >
            <div class="langGridContainer">                
                <div class="langCell cell1">
                    <img class="langImg" src={sources.sass} alt=sass />
                </div>
                <div class="langCell cell2">
                    <img class="langImg" src={sources.adobeXd} alt=adobeXd />
                </div>
            </div>
        </SwiperSlide>
        <SwiperSlide >
            <div class="langGridContainer invertOrientation">                
                <div class="langCell cell1">
                    <img class="langImg" src={sources.git} alt=git />
                </div>
                <div class="langCell cell2">
                    <img class="langImg" src={sources.gimp} alt=gimp />
                </div>
            </div>
        </SwiperSlide>

        
  </Swiper>

  <style>
    h1{
        position: relative;
        font-family: "DeathStar",sans-serif;
        position: relative;
        width: max-content;
    }
    .gridHeader{
        margin: 150px auto 100px;
        color: var(--textColorLight);
        font-family: "DeathStar",sans-serif;
        text-align: center;
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
    .langGridContainer {
        margin: auto;
        padding: 50px;
        background-color: var(--textColorDark2);
        display: grid;
        place-items: center;
        grid-row-gap: 40px;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(2, 1fr);
    }
    .cell1 { 
        grid-area: 1 / 1 / 2 / 2; 
    }
    .cell2 {
        padding-left:25%;
        grid-area: 2 / 2 / 3 / 3; 
    }
 

  </style>

  <!--  -->
  <!-- <Swiper
  spaceBetween={30}
  centeredSlides={true}
  autoplay={{
      delay: 2500,
      disableOnInteraction: false,
  }}
  loop={true}
  pagination={{
    clickable: true,
  }}
  navigation={true}
  modules={[Autoplay, Pagination, Navigation]}
  class="langGridContainer"
>
  <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
    <SwiperSlide>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, eligendi?</SwiperSlide>
  </Swiper> -->