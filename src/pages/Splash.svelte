<script>
    import Background from "../components/Background.svelte";
    import LoadingBounce from "../components/LoadingBounce.svelte";
    import LoadingBounceTwo from "../components/LoadingBounceTwo.svelte";
    import LoadingCube from "../components/LoadingCube.svelte";
    import LoadingGrid  from "../components/LoadingGrid.svelte";
    import LoadingRect from "../components/LoadingRect.svelte";
    import LoadingSpinner from "../components/LoadingSpinner.svelte";
    

    let choose = Math.floor(Math.random() * 7);
    console.log(choose);

</script>

<Background >
    {#if choose == 0}
         
         <LoadingBounce />
    {:else if  choose == 1}
        
         <LoadingBounceTwo />
     {:else if choose == 2}
    
         <LoadingCube />
    {:else if choose == 3}

         <LoadingGrid />
     {:else if choose == 4} 

         <LoadingRect />
     {:else}
         <LoadingSpinner />
    {/if}
   
</Background>