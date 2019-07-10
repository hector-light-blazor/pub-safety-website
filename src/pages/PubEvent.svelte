
<Header />

    <div class="container-grid">
        <form>
            <input type="text" />
        </form>

    </div>



<style>
    .container-grid {
        display: grid;
        grid-template-columns: auto;
        grid-gap: 20px;
        background-color: #2196F3;
        padding: 14px;
    }

    .container-grid > form {
        background-color: rgba(255, 255, 255, 0.8);
        text-align: center;
        padding: 20px 0;
        font-size: 30px;
    }

</style>
<script>
    import Header from "../components/Header.svelte";

</script>