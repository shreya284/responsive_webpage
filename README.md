<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Personal Portfolio Website - HTML, CSS & Vanilla Javascript</title>
     
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.2/css/all.min.css">
     
     <style>
         @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
  scroll-behavior: smooth;
}

section{
  padding: 100px 200px;
}

.main{
  position: relative;
  width: 100%;
  min-height: 100vh;
  display: flex;
  align-items: center;
  background: url(images/bg.jpg)no-repeat;
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}

.main .content{
  max-width: 800px;
}

.main .content h2{
  color: #fff;
  font-size: 2em;
  font-weight: 500;
}

.main .content h2 span{
  font-size: 2.8em;
  font-weight: 600;
}

.animated-text{
  position: relative;
  height: 70px;
  overflow: hidden;
}

.animated-text h3{
  color: #4e9eff;
  font-size: 3em;
  font-weight: 700;
  line-height: 70px;
  letter-spacing: 1px;
}

.animated-text h3:nth-child(1){
  animation: text-move 10s infinite;
}

@keyframes text-move{
  0%{
    margin-top: 0;
  }
  25%{
    margin-top: -70px;
  }
  50%{
    margin-top: -140px;
  }
  75%{
    margin-top: -70px;
  }
  100%{
    margin-top: 0;
  }
}

.btn{
  color: #fff;
  background: #3a6cf4;
  font-size: 1em;
  font-weight: 600;
  display: inline-block;
  padding: 10px 20px;
  text-transform: uppercase;
  text-decoration: none;
  letter-spacing: 1px;
  border-radius: 2px;
  margin-top: 30px;
  transition: 0.5s ease;
}

.btn:hover{
  background: #235bf6;
}

.media-icons{
  margin-top: 50px;
}

.media-icons a{
  color: #fff;
  font-size: 25px;
  margin-right: 30px;
}

header{
  z-index: 999;
  position: fixed;
  background: rgba(255, 255, 255, 0.1);
  top: 0;
  left: 0;
  width: 100%;
  padding: 15px 200px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: 0.5s ease;
}

header.sticky{
  background: #3a6cf4;
  padding: 10px 200px;
}

header .brand{
  color: #fff;
  font-size: 1.8em;
  font-weight: 700;
  text-transform: uppercase;
  text-decoration: none;
}

header .navigation{
  position: relative;
}

header .navigation a{
  color: #fff;
  font-size: 1em;
  font-weight: 500;
  text-decoration: none;
  margin-left: 30px;
}

header .navigation a:hover{
  color: #3a6cf4;
}

header.sticky .navigation a:hover{
  color: #000;
}

body{
  min-height: 110vh;
}

.title{
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.section-title{
  position: relative;
  color: #3a6cf4;
  font-size: 2.2em;
  font-weight: 800;
  margin-bottom: 60px;
}

.section-title:before{
  content: '';
  position: absolute;
  top: 56px;
  left: 50%;
  width: 140px;
  height: 4px;
  background: #3a6cf4;
  transform: translateX(-50%);
}

.section-title:after{
  content: '';
  position: absolute;
  top: 50px;
  left: 50%;
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: #3a6cf4;
  transform: translateX(-50%);
}

.about .content{
  position: relative;
  width: 100%;
  display: flex;
  justify-content: space-between;
  margin-top: 20px;
}

.about .content .col-left{
  position: relative;
  width: 45%;
}

.about .content .col-right{
  position: relative;
  width: 50%;
}

.about .content .col-left .img-card{
  position: relative;
  width: 100%;
  min-height: 450px;
}

.about .content .col-left .img-card img{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 10px;
}

.about .content .col-right .content-title{
  font-size: 2em;
  font-weight: 800;
  margin-bottom: 20px;
}

.about .content .col-right .paragraph-text{
  font-size: 1em;
}

.skills{
  background: #000016;
}

.skills .content{
  position: relative;
  width: 100%;
  display: flex;
  justify-content: space-between;
  color: #fff;
  margin-top: 20px;
}

.skills .content .col-left{
  position: relative;
  width: 46%;
}

.skills .content .col-left .content-title{
  margin-bottom: 20px;
}

.skills .content .col-right{
  position: relative;
  width: 46%;
}

.skills .content .col-right .bar{
  margin-bottom: 15px;
  padding: 10px;
}

.skills .content .col-right .bar .info{
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 5px;
}

.skills .content .col-right .bar .info span{
  font-size: 18px;
  font-weight: 500;
}

.skills .content .col-right .bar .line{
  position: relative;
  width: 100%;
  height: 15px;
  background: #ccc;
  border-radius: 2px;
}

.skills .content .col-right .bar .line:before{
  content: '';
  position: absolute;
  height: 100%;
  top: 0;
  left: 0;
  border-radius: 2px;
}

.skills .content .col-right .bar .html:before{
  width: 95%;
  background: #e45126;
}

.skills .content .col-right .bar .css:before{
  width: 90%;
  background: #0c73b8;
}

.skills .content .col-right .bar .javascript:before{
  width: 80%;
  background: #e3a324;
}

.skills .content .col-right .bar .jquery:before{
  width: 80%;
  background: #30dd6d;
}

.skills .content .col-right .bar .php:before{
  width: 75%;
  background: #6d7eb8;
}

.services .content{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  flex-direction: row;
  margin-top: 20px;
}

.title p{
  font-size: 1em;
  width: 80%;
}

.services .content .card{
  background: #fff;
  width: 340px;
  margin: 10px;
  padding: 25px;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  box-shadow: 0 5px 25px rgba(1 1 1 / 15%);
  border-radius: 10px;
}

.services .content .card .service-icon{
  color: #3a6cf4;
  font-size: 8em;
  text-align: center;
  transition: transform 0.5s ease;
}

.services .content .card:hover .service-icon{
  transform: translateY(-10px);
}

.services .content .card .info{
  text-align: center;
}

.services .content .card .info h3{
  color: #3a6cf4;
  font-size: 1.2em;
  font-weight: 700;
  margin: 10px;
}

.work{
  background: #000016;
}

.work .content{
  display: flex;
  justify-content: center;
  flex-direction: row;
  flex-wrap: wrap;
  margin-top: 20px;
}

.work .content .card{
  width: 340px;
  margin: 15px;
}

.work .content .card .card-img{
  position: relative;
  width: 100%;
  height: 260px;
  overflow: hidden;
  border-radius: 10px;
}

.work .content .card .card-img img{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 10px;
  transition: 0.5s ease;
}

.work .content .card .card-img img:hover{
  transform: scale(1.2);
}

.contact .content{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  flex-direction: column;
  margin-top: 20px;
}

.contact .content .row{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  flex-direction: row;
}

.contact .content .row .card{
  background: #fff;
  width: 240px;
  margin: 20px;
  padding: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  box-shadow: 0 5px 25px rgba(1 1 1 / 15%);
  border-radius: 10px;
}

.contact .content .row .card .contact-icon{
  color: #3a6cf4;
  font-size: 4em;
  text-align: center;
  transition: transform 0.5s ease;
}

.contact .content .row .card:hover .contact-icon{
  transform: translateY(-10px);
}

.contact .content .row .card .info{
  text-align: center;
}

.contact .content .row .card .info h3{
  color: #111;
  font-size: 1.2em;
  font-weight: 700;
  margin: 10px;
}

.contact .content .row .card .info span{
  color: #666;
  font-weight: 500;
}

.contact-form{
  background: #fff;
  max-width: 600px;
  margin-top: 50px;
  padding: 50px;
  border-radius: 10px;
  box-shadow: 0 5px 25px rgba(1 1 1 / 15%);
}

.contact-form h3{
  color: #111;
  font-size: 1.6em;
  font-weight: 600;
  text-align: center;
  margin-bottom: 40px;
}

.contact-form .input-box{
  position: relative;
  width: 100%;
  margin-bottom: 20px;
}

.contact-form .input-box input,
.contact-form .input-box textarea{
  color: #111;
  width: 100%;
  padding: 10px;
  font-size: 1em;
  font-weight: 400;
  outline: none;
  border: 1px solid #111;
  border-radius: 5px;
  resize: none;
}

.contact-form .input-box .send-btn{
  color: #fff;
  background: #3a6cf4;
  display: inline-block;
  font-size: 1.1em;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 2px;
  width: 100%;
  border: none;
  cursor: pointer;
  transition: 0.5s ease;
}

.contact-form .input-box .send-btn:hover{
  background: #235bf6;
}

.footer{
  background: #000016;
  color: #fff;
  text-align: center;
  padding: 2em;
}

.footer .footer-title{
  font-size: 20px;
  font-weight: 600;
}

.footer p{
  font-size: 16px;
  margin-top: 10px;
}

.footer p a{
  color: #3a6cf4;
  font-weight: 600;
  text-decoration: none;
}

@media (max-width: 1040px){
  header{
    padding: 12px 20px;
  }

  header.sticky{
    padding: 10px 20px;
  }

  header .navigation{
    display: none;
  }

  header .navigation.active{
    z-index: 888;
    position: fixed;
    background: #fff;
    top: 0;
    right: 0;
    width: 380px;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    box-shadow: 0 5px 25px rgba(1 1 1 / 15%);
    transition: 0.3s ease;
  }

  header .navigation a{
    color: #000;
    font-size: 1.2em;
    margin: 10px;
    padding: 0 20px;
    border-radius: 20px;
  }

  header .navigation a:hover{
    background: #3a6cf4;
    color: #fff;
    transition: 0.3s ease;
  }

  .menu-btn{
    position: absolute;
    background: url(images/menu.png)no-repeat;
    background-size: 30px;
    background-position: center;
    width: 40px;
    height: 40px;
    right: 0;
    margin: 0 20px;
    cursor: pointer;
    transition: 0.3s ease;
  }

  .menu-btn.active{
    z-index: 999;
    background: url(images/close.png)no-repeat;
    background-size: 25px;
    background-position: center;
    transition: 0.3s ease;
    filter: invert(1);
  }

  section{
    padding: 80px 20px;
  }

  .main .content h2{
    font-size: 1em;
  }

  .animated-text h3{
    font-size: 2.2em;
  }

  .section-title{
    font-size: 1.8em;
  }

  .about .content{
    flex-direction: column;
  }

  .about .content .column{
    position: relative;
    width: 100%;
  }

  .about .content .col-right{
    margin-top: 40px;
  }

  .skills .content{
    flex-direction: column;
  }

  .skills .content .column{
    position: relative;
    width: 100%;
  }

  .skills .content .col-right{
    margin-top: 40px;
  }

  .contact-form{
    padding: 35px 40px;
  }
}

.scrollToTop-btn{
  z-index: 999;
  position: fixed;
  background: #3a6cf4;
  color: #fff;
  width: 45px;
  height: 45px;
  right: 0;
  bottom: 10px;
  font-size: 22px;
  text-align: center;
  line-height: 45px;
  border-radius: 3px;
  cursor: pointer;
  pointer-events: none;
  opacity: 0;
  transition: all 0.3s ease;
}

.scrollToTop-btn.active{
  right: 20px;
  opacity: 1;
  pointer-events: auto;
}

.reveal{
  position: relative;
  transform: translateY(50px);
  opacity: 0;
  transition: all 1.5s ease;
}

.reveal.active{
  transform: translateY(0);
  opacity: 1;
}       
     </style>
  </head>
  <body>

    <div class="scrollToTop-btn">
      <i class="fas fa-angle-up"></i>
    </div>

    <header>
      <a href="#" class="brand">Jacob</a>
      <div class="menu-btn"></div>
      <div class="navigation">
        <a href="#main">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#services">Services</a>
        <a href="#work">Work</a>
        <a href="#contact">Contact</a>
      </div>
    </header>

    <section class="main" id="main">
      <div class="content">
        <h2>Hello, I'm<br><span>Jacob Stevens</span></h2>
        <div class="animated-text">
          <h3>Web Designer</h3>
          <h3>Web Developer</h3>
          <h3>Motion Graphic Designer</h3>
        </div>
        <a href="#" class="btn">See My Work</a>
        <div class="media-icons">
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-twitter"></i></a>
        </div>
      </div>
    </section>

    <section class="about" id="about">
      <div class="title reveal">
        <h2 class="section-title">About Me</h2>
      </div>
      <div class="content">
        <div class="column col-left reveal">
          <div class="img-card">
            <img src="images/img1.jpg" alt="">
          </div>
        </div>
        <div class="column col-right reveal">
          <h2 class="content-title">Hey There! I'm Jacob Stevens</h2>
          <p class="paragraph-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.<br><br>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          <a href="#" class="btn">See More</a>
        </div>
      </div>
    </section>

    <section class="skills" id="skills">
      <div class="title reveal">
        <h2 class="section-title">My Skills</h2>
      </div>
      <div class="content">
        <div class="column col-left reveal">
          <h2 class="content-title">My Skills and Experiences</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          <a href="#" class="btn">See More</a>
        </div>
        <div class="column col-right reveal">
          <div class="bar">
            <div class="info">
              <span>HTML</span>
              <span>95%</span>
            </div>
            <div class="line html"></div>
          </div>
          <div class="bar">
            <div class="info">
              <span>CSS</span>
              <span>85%</span>
            </div>
            <div class="line css"></div>
          </div>
          <div class="bar">
            <div class="info">
              <span>Javascript</span>
              <span>80%</span>
            </div>
            <div class="line javascript"></div>
          </div>
          <div class="bar">
            <div class="info">
              <span>JQuery</span>
              <span>80%</span>
            </div>
            <div class="line jquery"></div>
          </div>
          <div class="bar">
            <div class="info">
              <span>PHP</span>
              <span>75%</span>
            </div>
            <div class="line php"></div>
          </div>
        </div>
      </div>
    </section>

    <section class="services" id="services">
      <div class="title reveal">
        <h2 class="section-title">My Services</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      </div>
      <div class="content">
        <div class="card reveal">
          <div class="service-icon">
            <i class="fas fa-palette"></i>
          </div>
          <div class="info">
            <h3>Web Design</h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          </div>
        </div>
        <div class="card reveal">
          <div class="service-icon">
            <i class="fas fa-file-code"></i>
          </div>
          <div class="info">
            <h3>Web Development</h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          </div>
        </div>
        <div class="card reveal">
          <div class="service-icon">
            <i class="fas fa-object-group"></i>
          </div>
          <div class="info">
            <h3>Motion Graphic Design</h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="work" id="work">
      <div class="title reveal">
        <h2 class="section-title">My Work</h2>
      </div>
      <div class="content">
        <div class="card reveal">
          <div class="card-img">
            <img src="images/work1.jpg" alt="">
          </div>
        </div>
        <div class="card reveal">
          <div class="card-img">
            <img src="images/work2.jpg" alt="">
          </div>
        </div>
        <div class="card reveal">
          <div class="card-img">
            <img src="images/work3.jpg" alt="">
          </div>
        </div>
        <div class="card reveal">
          <div class="card-img">
            <img src="images/work4.jpg" alt="">
          </div>
        </div>
        <div class="card reveal">
          <div class="card-img">
            <img src="images/work5.jpg" alt="">
          </div>
        </div>
        <div class="card reveal">
          <div class="card-img">
            <img src="images/work6.jpg" alt="">
          </div>
        </div>
        <div class="title reveal">
          <a href="#" class="btn">See All</a>
        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <div class="title reveal">
        <h2 class="section-title">Contact Me</h2>
      </div>
      <div class="content">
        <div class="row">
          <div class="card reveal">
            <div class="contact-icon">
              <i class="fas fa-map-marker-alt"></i>
            </div>
            <div class="info">
              <h3>Address</h3>
              <span>Address, City, Country</span>
            </div>
          </div>
          <div class="card reveal">
            <div class="contact-icon">
              <i class="fas fa-phone"></i>
            </div>
            <div class="info">
              <h3>Phone</h3>
              <span>+00 0000 000 000</span>
            </div>
          </div>
          <div class="card reveal">
            <div class="contact-icon">
              <i class="fas fa-envelope"></i>
            </div>
            <div class="info">
              <h3>Email Address</h3>
              <span>contact@email.com</span>
            </div>
          </div>
          <div class="card reveal">
            <div class="contact-icon">
              <i class="fas fa-globe"></i>
            </div>
            <div class="info">
              <h3>Website</h3>
              <span>mywebsite.com</span>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="contact-form reveal">
            <h3>Send Message</h3>
            <div class="input-box">
              <input type="text" name="" value="" placeholder="Name">
            </div>
            <div class="input-box">
              <input type="text" name="" value="" placeholder="Email">
            </div>
            <div class="input-box">
              ,
            </div>
            <div class="input-box">
              <input type="submit" class="send-btn" name="" value="Send"/>
            </div>
          </div>
        </div>
      </div>
    </section>

    <footer class="footer">
      <span class="footer-title">Jacob Stevens</span>
      <p>Copyright @2021 <a href="#">Coding Snow</a>. All Rights Reserved.</p>
    </footer>

    <script>
     //javascript for navigation bar effects on scroll
window.addEventListener("scroll", function(){
  const header = document.querySelector("header");
  header.classList.toggle('sticky', window.scrollY > 0);
});

//javascript for responsive navigation sidebar menu
const menuBtn = document.querySelector(".menu-btn");
const navigation = document.querySelector(".navigation");
const navigationItems = document.querySelectorAll(".navigation a")

menuBtn.addEventListener("click",  () => {
  menuBtn.classList.toggle("active");
  navigation.classList.toggle("active");
});

navigationItems.forEach((navigationItem) => {
  navigationItem.addEventListener("click", () => {
    menuBtn.classList.remove("active");
    navigation.classList.remove("active");
  });
});

//javascript for scroll to top button
const scrollBtn = document.querySelector(".scrollToTop-btn");

window.addEventListener("scroll", function(){
  scrollBtn.classList.toggle("active", window.scrollY > 500);
});

//javascript for scroll back to top on click scroll-to-top button
scrollBtn.addEventListener("click", () => {
  document.body.scrollTop = 0;
  document.documentElement.scrollTop = 0;
});

//javascript for reveal website elements on scroll
window.addEventListener("scroll", reveal);

function reveal(){
  var reveals = document.querySelectorAll(".reveal");

  for(var i = 0; i < reveals.length; i++){
    var windowHeight = window.innerHeight;
    var revealTop = reveals[i].getBoundingClientRect().top;
    var revealPoint = 50;

    if(revealTop < windowHeight - revealPoint){
      reveals[i].classList.add("active");
    }
  }
}      
     </script>

  </body>
</html>
