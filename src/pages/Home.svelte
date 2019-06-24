<script>
    import Carousel from "../components/Carousel.svelte";
</script>
<style>

    header {
        position: fixed;
        background: #fff;
        width: 100%;
        height: 110px;
        z-index: 3;
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
      
    li:hover {
      font-size: 20px;
      color: #7B120E;
    }

    .menu {
      float: right; padding-right: 50px;
    }

    .logo {
      position: absolute;height: 2px;width: 120px;margin-left: 100px;bottom: 106px;
    }

    @media only screen and (max-width: 1370px) {
      .menu {
        display: none;
      }

      .logo {
        position: absolute;
        height: 2px;width: 120px;
        left: 50%;
        margin-left: -60px;
        bottom: 106px;
      }
  }


</style>
<header>
    <div class="sub">
    heloo
    </div>
    <div class="logo">
        <img width="140" height="140" src="assets/public_safety_logo.webp" alt="Safety">
    </div>
    <div class="menu">
        <ul>
            <li>HOME</li>
            <li>LOCATION VALIDATION</li>
            <li>MAPPING</li>
            <li>DATABASE</li>
            <li>SYSTEM & PSAP OPERATIONS</li>
            <li>PUBLIC EDUCATION</li>
            <li>TRAINING</li>
            
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