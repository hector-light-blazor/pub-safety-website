
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
        width: 14%;
        margin-right: 44px;
        padding: 10px;
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