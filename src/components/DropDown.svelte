
<script>
    import { fade } from 'svelte/transition';
    export let color;
    export let title;
    let show = false;
</script>
<style>
    .header-fly {
        position: relative;
        float: right;
        z-index: 2;
        bottom: 24px;
        color: white;
        height: 20px;
        width: 24.54%;
        margin-right: 42px;
        padding: 8px;
        text-align: center;
        cursor: pointer;
    }
    img {
        color: white;
       float: right;
    }

    ul {
        position: absolute;
        left: 0;
        top: 26px;
        list-style: none;
        width: 100%;
        padding: 0;
        text-align: left;
    }
    
    ul >li {
        padding: 5px 0;
    }

     @media only screen and (min-width: 1110px) {
            .header-fly{
               
                width: 300px;
                
            }
     }

     @media only screen and (max-width: 767px) {
            .header-fly{
               
               display: none;
            }
     }
</style>
<div  on:click="{() => {show = !show; }}" class="header-fly" style="background: {color}">
    {title}
    <img width="20" height="20" src="./assets/chevron-circle-down-solid.svg" alt="Arrow">
    {#if show}
         <!-- content here -->
         <ul transition:fade style="background: {color}">
            <li>Request An Address</li>
            <li>Request An Event</li>
         </ul>
    {/if}
</div>