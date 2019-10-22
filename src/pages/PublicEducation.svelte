<style>
    h1 {
        color: #2B4988;
        
    }
    h3{
        color: #2B4988;
    }

    h1 i {
        color: #707070;
    }



    .flex-container {
        max-width: 1200px;
     margin: auto;
     
     padding: 10px;
    }

    img {
       
        margin-right: 30px;
        margin-bottom: 20px;
    }

    p {
        color: #2B4988;
    }

    button {
        border-radius: 16px;
        color:white;
        background: #2B4988;
        cursor: pointer;
        text-align: center;
        width: 190px;
    }
    button:hover {
       background:rgb(12, 37, 90);
    }
    .grid-container-3 {
        display: grid;
        grid-template-columns: 60% 10% 20%;
        
    }

    .imgResponsive {
        width: 100%;
        height: auto;
    }

    .imgResponsive:hover {
        cursor: pointer;
    }

    #cellPhone {
        position: absolute;right:0; z-index: -1;top:1270px; bottom: 0;
    }
    #btnEvent{
        margin-top: 160px;
    }
    #imgCon {
        width: 520;
        height: 420;        
    }

    @media only screen and (max-width: 1370px) {
      #cellPhone {
        display: none;
      }

      #imgCon {
           width: 100%;
        height: auto;
      }

      .grid-container-3 {
          display: initial;
      
      }

       .flex-container {
            max-width: 100%;
            margin: 0;
            padding: 30px;
           
        }

         #btnEvent{
        margin-top: 60px;
    }

    }

   
</style>

<div class="flex-container">
     <h1><b>Public Education </b><i > Program</i></h1>
    <div class="grid-container-3">
        <div>
            
                 <p >
                    We attend several events which gives us the opportunity to promote and educate the public on how to properly use the 9-1-1 system.
                
                </p>
                <p>We give presentations that local cities, school, daycares, Fire, Police Depts. and Emergency Medical Services (EMS) companies within the Hidalgo and Willacy Counties. While attending these events, our mascots (Cell Phone Sally, Josh and Keith Friendly Kid) have become a great part of our education program

                </p>
                <p>
                    Using multi-media, we demonstrate the proper way to call 9-1-1 and what is considered a 9-1-1 emergency call. Promotional item distribution is a major part of our program.
                </p>

                <div id="btnEvent">
                   <button>EVENT REQUEST</button>
                </div>
        </div>
        <div></div>
        <div>
              <img id="imgCon"  src="/assets/photoPub1.webp"  alt="Kids with mascot" />
        </div>
    </div>

      

        <div>
            <h3><i>Do you know how to make 9-1-1 work for you?</i></h3>
            <p>For forty years, 9-1-1 has served as the vital link between the American public and emergency services. Public education and awareness initiatives throughout the years have contributed in large measure to the incredible and ongoing success of the emergency communications system as a whole. It is imperative that 9-1-1 professionals, teachers, government officials, media representatives, and industry leaders are equipped with the tools necessary to continue these efforts in the face of an ever-changing telecommunications landscape, and that citizens of all ages are well versed in the role they play in ensuring effective and efficient emergency response for themselves and their fellow citizens.The resources below provide you with the tools necessary to educate yourself and your community on the proper use of the 9-1-1 system, no matter which side of the phone you are on.</p>

            <img class="imgResponsive" src="/assets/jpg/karis_law_banner.jpg" alt="Kari Banner" />
            <img class="imgResponsive" src="/assets/jpg/lv_banner.jpg" alt="Lv banner" />
            <img class="imgResponsive" src="/assets/jpg/text_to_911_banner.jpg" alt="TXT 911 Banner" />

            
            <div >
                <img class="imgResponsive" width="850" src="/assets/jpg/team_banner.jpg" alt="Team Banner" /> 
            </div>

            <div id="cellPhone" >
                 <img style="margin-left: 100px; margin-top: 200px;" width="600" height="600" src="/assets/jpg/cpswave.jpg" alt="CPS Wave" />
            </div>
            
        </div>
   

</div>




