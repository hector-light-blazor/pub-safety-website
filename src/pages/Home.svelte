<script>
    import Carousel from "../components/Carousel.svelte";
    import Box from "../components/Box.svelte";
</script>
<style>

    .center {
    

      background: #e7ebed;
      width: 100%;
      padding-right: 15px;
      padding-left: 15px;
      margin-right: auto;
      margin-left: auto;
      text-align: center;
      padding-top: 150px;
      padding-bottom: 150px;
      padding: 70px 0;  
          }
    p {
      text-align:center;
      color: #D5AF34;
    }

   
    .wrapper {
     
      width:60%;
      margin: 0 auto;
    }
    

    button:hover { opacity: 0.5;}
    .flex-grid {
      padding-left: 20%;
      padding-right: 20%;
      display: flex;
      justify-content: space-between;
    }

</style>
<Carousel />

<div class="center">
  <div class="wrapper">
      <p>The 9-1-1 Department of the Lower Rio Grande Valley Development Council provides support services and equipment for 9-1-1 Call Centers in Hidalgo and Willacy Counties. Our 18 Public Safety Answering Points (PSAPs) are located at (and staffed by) area police departments, fire stations, and the sheriffs office.</p>
    <div style="text-align: center;">
        <button style="border-radius: 10px;cursor: pointer;width: 200px; height: 60px;color: white; background: #263E70;">Read more...</button>
    </div>
  
  </div>

  <div class="flex-grid">
      <Box />
  <Box />
  <Box />
  
  </div>

</div>

