<script>
    import { onMount } from 'svelte';
    import { fade } from 'svelte/transition';
    import DropDown from "./DropDown.svelte";
    import LoadingCube from './LoadingCube.svelte';
    let images = [ {img: 'assets/carousel/dispatcher_2.jpg', selected: true, title: "Welcome", subTitle: "LRGVDC 911 Department", readMore: true },
                   {img: 'assets/carousel/call_if_you_can.jpg', selected: false}, 
                   {img: 'assets/carousel/609.jpg', selected: false}]

    let currentIndex = 0;
    
    let fadeOut = false;
    
    $:selected = (currentIndex > -1) ?  images[currentIndex].img : "assets/carousel/dispatcher_2.jpg";
    $:display  = (fadeOut) ? "block" : "none";
    onMount(async () => {
    
        fadeOut = true;
		setInterval(() => {
            fadeOut = false;
            var length = images.length;
           
            if(currentIndex < length ) {
                images[currentIndex].selected = false;

                currentIndex = (currentIndex + 1 == length) ? 0 : currentIndex + 1;
                images[currentIndex].selected = true;
            }
            setTimeout(() => {
                fadeOut = true;
            }, 200);

            
        }, 5000);
    });
    
    function changePic(index) {
        fadeOut = false;
        images[currentIndex].selected = false;
        currentIndex = index;
        images[index].selected = true;
         setTimeout(() => {
                fadeOut = true;
            }, 200);
    }
</script>
<style>
    img{
        width: 100%;
        object-fit: cover;
    }
    .rounded {
        border-radius: 20px;
        cursor: pointer;
        width: 20px;height: 20px;
        margin-bottom: 10px;
         
    }

    .red-round {
        border: 1px solid #fff;
        background: #7B120E;
    }

    .blue-round {
        border: 1px solid #263E70;
    }


    .animate-zoom {animation:animatezoom 0.6s}@keyframes animatezoom{from{transform:scale(0)} to{transform:scale(1)}}
</style>
<div style="height: 600px; width:100%">
    <div style="position: absolute;left: 16%;margin-top: 20px; height: 240px; width: 100px; z-index:2;" >
        <div style="float: left;width: 50px;">
            {#each images as image, i}
                <!-- content here -->
                <div on:click="{()=> {changePic(i)}}" class:red-round={image.selected} class:blue-round={!image.selected}  class="rounded"></div>
            {/each}
        </div>
        <div style="float: left"><div style="height: 120px;width:0px; " class="blue-round">
        </div></div>
        
    </div>

    {#if fadeOut}
         <!-- content here -->
         <img class="animate-zoom" style="display: {display}"  height="600" src="{selected}" alt="TEST">
    {:else} 
        <div style="color:#7B120E !important; height: 600px;width: 100%">
          <LoadingCube />
        </div>
    {/if}
    

    <DropDown title="I need to Contact..." color="#C4C5C8" />
    <DropDown title="I'm looking for..." color="#7B120E" />
    <DropDown title="I want to..." color="#263E70" />
</div>
