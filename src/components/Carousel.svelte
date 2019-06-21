<script>

    let images = ['assets/dispatcher_2.jpg']
</script>
<style>
    img{
        width: 100%;
        object-fit: cover;
    }
</style>
<div style="height: 400px; width:100%">
    {#each images as image}
        <img height="400" src="{image}" alt="TEST">
    {/each}
</div>
