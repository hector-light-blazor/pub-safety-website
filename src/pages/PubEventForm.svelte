<script>
    import EventRequest from "../components/EventRequest.svelte";

</script>
<style>
    .grid-container {
        display: grid;
        height: 90%;
        grid-template-columns: auto auto auto;
       
    }


h1{
    text-decoration: underline;
    color: #263E70;
    text-align: center;
    margin-bottom: 8px;
}

h3{
  text-decoration: underline;
  color: #BB2026;
  
  
}




</style>

<div class="grid-container">
    <div class="grid-item">
        <img width="300" src="/assets/ECOMMSART_WORK.webp" alt="lrgvdc" />
    </div>
    <div class="grid-item">
        <h1>Event Request</h1>
        <div style="border: 1px solid #BB2026; text-align: center; color:#BB2026; ">
            <h3>NOTE</h3>
            <p>** All Public Event Requests must be submitted to LRGVDC at a minimum of 14 business day prior to your event. **</p>
            <p>** Requests between the 14 day period will not be accepted by the online system **</p>
            <p>** If you are experiencing problems with your online request**</p>
            <p>** please call us directly at (956) 682-3481 ext. 167 to help resolve the issues. **</p>
        </div>
        <h3 style="text-align: center; color: #263E70;cursor: pointer;"><img width="18" height="18" src="/assets/png/calendar.png" alt="Calendar" />Click to view scheduled events</h3>
        <EventRequest />     
    </div>
    <div class="grid-item">
        <img style="float:right;" width="300" src="/assets/LRGVDCART_WORK.webp" alt="lrgvdc" />
    </div>
</div>

      

        






   

