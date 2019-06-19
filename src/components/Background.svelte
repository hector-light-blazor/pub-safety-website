<script>
    export let src;
    export let mobile;

</script>


{#if mobile}
     <div  style="background: url('{src}');
            background-repeat: no-repeat;background-size: cover; width: 100%; height: 100%;">

    <slot></slot>

</div>
{:else}
     <div  style="background:#2c3e50;  width: 100%; height: 100%;">

    <slot></slot>
    
</div>
{/if}
