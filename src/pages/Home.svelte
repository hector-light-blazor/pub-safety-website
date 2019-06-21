<script>
    import Carousel from "../components/Carousel.svelte";
</script>
<style>

    header {
        position: fixed;
        background: #fff;
        width: 100%;
        height: 110px;
        box-shadow: 1px 2px 4px rgba(0, 0, 0, .5);
    }
    .sub {
        width: 100%;
        height: 40px;
        background: #707070;
    }
    ul {
        list-style: none;
        color: #263E70;
        min-width: 696px;
    }
    ul li {
        padding-left: 20px;
		display: inline;
    }

    li{
        cursor: pointer;
    }
      


    li:nth-of-type(1):hover ~ .underbar {
        left: 12px;
        width: 62px;
        background: rgba(200,100,100,1);
        display: block;
    }

    li:nth-of-type(2):hover ~ .underbar {
        left: 80px;
        width: 190px;
        background: rgba(200,100,100,1);
         display: block;
    }
    li:nth-of-type(3):hover ~ .underbar {
        left: 272px;
        width: 88px;
        background: rgba(200,100,100,1);
         display: block;
    }
    li:nth-of-type(4):hover ~ .underbar {
        left: 366px;
        width: 94px;
        background: rgba(200,100,100,1);
         display: block;
    }
    li:nth-of-type(5):hover ~ .underbar {
        left: 466px;
        width: 226px;
        background: rgba(200,100,100,1);
         display: block;
    }
    li:nth-of-type(6):hover ~ .underbar {
        left: 698px;
        width: 165px;
        background: rgba(200,100,100,1);
         display: block;
    }
    li:nth-of-type(7):hover ~ .underbar {
        left: 870px;
        width: 86px;
        background: rgba(200,100,100,1);
         display: block;
    }

    .underbar{
        width: 0;
        height: 5px;
        background: rgba(100,100,200,0);
        display: none;
        position: relative;
        transition: 0.5s ease;
}



</style>
<header>
    <div class="sub">
    heloo
    </div>
    <div style="position: relative;height: 2px;width: 120px;margin-left: 40px;margin-top: 6px;">
        <img width="120" height="120" src="assets/public_safety_logo.webp" alt="Safety">
    </div>
    <div style="float: right; padding-right: 50px;">
        <ul>
            <li>HOME</li>
            <li>LOCATION VALIDATION</li>
            <li>MAPPING</li>
            <li>DATABASE</li>
            <li>SYSTEM & PSAP OPERATIONS</li>
            <li>PUBLIC EDUCATION</li>
            <li>TRAINING</li>
            <div class="underbar"></div>
        </ul>
    </div>
    
</header>
<div style="height: 110px;width:100%;"></div>

<Carousel />

<div>

  test

</div>
<div class="container-fluid bg-1 text-center">
  <h3>Who Am I?</h3>
  <img src="bird.jpg" class="img-circle" alt="Bird">
  <h3>I'm an adventurer</h3>
</div>

<div class="container-fluid bg-2 text-center">
  <h3>What Am I?</h3>
  <p>Lorem ipsum..</p>
</div>

<div class="container-fluid bg-3 text-center">
  <h3>Where To Find Me?</h3>
  <p>Lorem ipsum..</p>
</div>
<div class="container-fluid bg-1 text-center">
  <h3>Who Am I?</h3>
  <img src="bird.jpg" class="img-circle" alt="Bird">
  <h3>I'm an adventurer</h3>
</div>

<div class="container-fluid bg-2 text-center">
  <h3>What Am I?</h3>
  <p>Lorem ipsum..</p>
</div>

<div class="container-fluid bg-3 text-center">
  <h3>Where To Find Me?</h3>
  <p>Lorem ipsum..</p>
</div>
<div class="container-fluid bg-1 text-center">
  <h3>Who Am I?</h3>
  <img src="bird.jpg" class="img-circle" alt="Bird">
  <h3>I'm an adventurer</h3>
</div>

<div class="container-fluid bg-2 text-center">
  <h3>What Am I?</h3>
  <p>Lorem ipsum..</p>
</div>

<div class="container-fluid bg-3 text-center">
  <h3>Where To Find Me?</h3>
  <p>Lorem ipsum..</p>
</div>