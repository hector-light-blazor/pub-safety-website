<script>
    import { onMount } from 'svelte';
    import { fade } from 'svelte/transition';
    import DropDown from "./DropDown.svelte";
    import LoadingCube from './LoadingCube.svelte';

    let iOS = !!navigator.platform && /iPad|iPhone|iPod/.test(navigator.platform); //What type of platform we are in...
    
    let images = [ {svg: "assets/carousel/cell_phone_sally_friends.svg", webp: 'assets/carousel/cell_phone_sally_friends.webp', img: "", title: "Cell Phone Sally", subTitle: "& Friends", selected: true},
     {svg: null, webp: 'assets/carousel/dispatcher.webp',img: 'assets/carousel/dispatcher.jpg', selected: false, title: "Welcome", subTitle: "ECOMMS/9-1-1", readMore: true },
                   {webp: 'assets/carousel/call_if_you_can.webp',img: 'assets/carousel/call_if_you_can.jpg',title: "Text to 9-1-1",subTitle: null, selected: false}, 
                   {webp: null,img: 'assets/carousel/Karis_Lawsides.jpg', title: "Kari's Law",subTitle: null, selected: false}, 
                   {webp: null,svg: 'assets/carousel/pocket_dial.svg', img: 'assets/carousel/pocket_dial.jpg', title: "Pocket Dial",subTitle: null, selected: false},
                   {webp: "assets/carousel/english_tips_txt.webp", img: "assets/carousel/english_tips_txt.jpg", title:'TXT Tips', subTitle: null, selected: false}]

    let currentIndex = 0;
    
    let fadeOut = false;
    let interval = null;
    let timeout  = null;
    
    $:Title    = (currentIndex > -1) ?  images[currentIndex].title : "";
    $:SubTitle = (currentIndex > -1) ?  (images[currentIndex].subTitle) ? images[currentIndex].subTitle : "ECOMMS/9-1-1" : "";
    $:selected = (currentIndex > -1) ?  selectImage() : "";
    $:display  = (fadeOut) ? "block" : "none";


    function selectImage() {
        let select = '';
        if(iOS) {
            if(images[currentIndex].svg) {
                select = images[currentIndex].svg;
            }
            else {
               select = images[currentIndex].img
            }
        }else {
            if(images[currentIndex].webp) {
                select = images[currentIndex].webp;
            }else if(images[currentIndex].svg)
            {
                 select = images[currentIndex].svg;
            }
            else {
               select = images[currentIndex].img;
            }
        }
        console.log(select);
        return select;
        
    }

    onMount(async () => {
    
        fadeOut = true;
        play();
		
    });
    
    function play() {
        interval = setInterval(() => {
            fadeOut = false;
            var length = images.length;
           
            if(currentIndex < length ) {
                images[currentIndex].selected = false;

                currentIndex = (currentIndex + 1 == length) ? 0 : currentIndex + 1;
                images[currentIndex].selected = true;
            }
           timeout = setTimeout(() => {
                fadeOut = true;
            }, 200);

            
        }, 5000);
    }

    function stop() {
        clearInterval(interval);
        clearTimeout(timeout)
    }


    function changePic(index) {
        stop()
        fadeOut = false;
        images[currentIndex].selected = false;
        currentIndex = index;
        images[index].selected = true;
       
         setTimeout(() => {
                fadeOut = true;
            }, 200);

             play();
    }

    function onErrorIMG (event) {

    }
</script>
<style>
    img{
        
        cursor: pointer;
        height: 600;
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 100%;
    }
 
    
    .container {
        height: 600px; width:100%
    }

    .cover {
        height: 600px;width: 100%
    }
    .rounded {
        border-radius: 20px;
        cursor: pointer;
        width: 20px;height: 20px;
        margin-bottom: 10px;
         
    }
    

    .red {
        border: 1px solid #fff;
        background: #7B120E;
    }

    .blue {
        border: 1px solid #263E70;
    }


    .animate-zoom {animation:animatezoom 0.6s}@keyframes animatezoom{from{transform:scale(0)} to{transform:scale(1)}}


    @media only screen and (max-width: 1370px) {

            img {
                
                height: 450;
            }

            .container {
                height: 450px;
            }

            .cover {
                height: 450px;width: 100%
            }

    }


</style>
<div class="container">
    <div style="position: absolute;left: 10%;margin-top: 20px; height: 240px; width: 340px; z-index:2;" >
            <div style="float: left;width: 50px;">
                {#each images as image, i}
                    <!-- content here -->
                    <div on:click="{()=> {changePic(i)}}" class:red={image.selected} class:blue={!image.selected}  class="rounded"></div>
                {/each}
            </div>
            <div style="float: left;width: 20px;"><div style="height: 120px;width:0px; " class="blue"></div></div>
            <div style="float: left;">
                <h2>{Title}</h2>
                <div  class="blue" style="position: absolute;width: 170px;bottom: 184px;"></div>
                <h3>{SubTitle}</h3>
                <a style="color: #D5AF34; cursor: pointer;">READ MORE</a>
                </div>
    </div>

    {#if fadeOut}
         <!-- content here -->
         <img on:error="{onErrorIMG}" class="animate-zoom" style="display: {display}"   src="{selected}" alt="TEST">
    {:else} 
        <div class="cover" style="background-color:#263E70 !important; ">
          
        </div>
    {/if}
    

    <DropDown title="I need to Contact..." color="#C4C5C8" />
    <DropDown title="I'm looking for..." color="#7B120E" />
    <DropDown title="I want to..." color="#263E70" />
</div>
