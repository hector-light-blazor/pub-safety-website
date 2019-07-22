
<Header />

    <div class="container">

        <nav aria-label="breadcrumb">
        <ol class="breadcrumb">
            <li class="breadcrumb-item"><a href="#event">Event Info</a></li>
            <li class="breadcrumb-item"><a href="#main_contact">Main Contact</a></li>
            <li class="breadcrumb-item"><a href="#alternate_contact">Alternate Contact</a></li>
        </ol>
        </nav>

        <div class="info">
            <h5>** All Public Event Requests must be submitted to LRGVDC at a minimum of 14 business day prior to your event. **</h5>
            
            <h5>** Requests between the 14 day period will not be accepted by the online system **</h5>
            <h5>** If you are experiencing problems with your online request**</h5>
            <h5>** please call us directly at (956) 682-3481 ext. 167 to help resolve the issues. **</h5>
        </div>
        <div id="event" class="info">
          <form>
            <label>Event Name:</label>
            <input type="text" />
            </form>
        </div>

        <div class="info" id="main_contact">
        <form>
            <label>Event Name:</label>
            <input type="text" />
            </form>
        </div>
        <div class="info" id="alternate_contact">
            <form>
                <label>Event Name:</label>
                <input type="text" />
                </form>
        </div>
        

    </div>



<style>
    .container {
     margin: auto;
     width: 50%;
     padding: 10px;
    }

    .breadcrumb {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    padding: .75rem 1rem;
    margin-bottom: 1rem;
    list-style: none;
    background-color: #e9ecef;
    border-radius: .25rem;
}

.breadcrumb-item+.breadcrumb-item::before {
    display: inline-block;
    padding-right: .5rem;
    padding-left: .5rem;
    color: #6c757d;
    content: "/";

}

    .info {
        border-radius: 8px;
        border: 3px solid green;
        padding: 10px;
        margin-bottom: 14px;
    }

    input {border-radius: 10px;width: 100%;}
    h5 {
        text-align: center;
        color: red;
    }

</style>
<script>
    import Header from "../components/Header.svelte";

</script>