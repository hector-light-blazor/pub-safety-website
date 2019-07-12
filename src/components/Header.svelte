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


<style>

    header {
        position: fixed;
        background: #fff;
        width: 100%;
        height: 110px;
        z-index: 3;
        box-shadow: 1px 2px 4px rgba(0, 0, 0, .5);
         font-family: Helvetica Neue; font-size: 20px; font-style: normal; font-variant: normal; font-weight: 700; line-height: 26.4px;  
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