<script>
    import Carousel from "../components/Carousel.svelte";
    import Footer from "../components/Footer.svelte";
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

    .header-topstrip-wide {
    width: 100%;
    float: left;
    margin-left: 14%;
    padding: 0;
}
    .sub {
        width: 100%;
        height: 40px;
        background: #707070;
        color: #C9A737  !important;
    }

  a{
    color: #C9A737;
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
      transform: scale(3);
      -webkit-transform: scale(2.3);
      -ms-transform: scale(3);
      color: #7B120E;
    }

    .center {
      margin-left: 20%;
      width: 60%;
      margin-top: 20px;
      padding: 10px;
    }
    p {
      text-align:center;
      color: #D5AF34;
    }

    .grow {
      transition: all .2s ease-in-out;
    }

    .grow:hover {
      transition: all 0.2s ease-in-out;
      transform: scale(4);
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
        <div class="header-topstrip-wide">
											<span class="contact-hours"><i class="fa fa-calendar"></i>Monday-Friday 8AM – 5PM CST</span>
												<a href="tel:956-682-3481"><span class="contact-phone"><i class="fa fa-phone"></i>956.682.3481</span></a>
                        
										</div>
    </div>
    <div class="logo">
        <img width="140" height="140" src="assets/public_safety_logo.webp" alt="Safety">
    </div>
    <div class="menu">
        <ul>
            <li class="grow">HOME</li>
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

<div class="center">

  <p>The 9-1-1 Department of the Lower Rio Grande Valley Development Councilprovides support services and equipment for 9-1-1 Call Centers in Hidalgo and Willacy Counties. Our 18 Public Safety Answering Points (PSAPs) are located at (and staffed by) area police departments, fire stations, and the sheriffs office.</p>
  <div>
      <button style="cursor: pointer;">Read more...</button>
  </div>
</div>

<Footer />
