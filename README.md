<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>navbar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    < a href="file:///C:/Users/sutha/Desktop/navbar/index.html/" target*"_blank">Animated web page</a>
    <nav class="nav">
        <span> Dashboard </span>
        <u1>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Projects</a></li>
        </u1>
        <div class="hamburger">
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
        </div>
    </nav>

    <script src="script.js"></script>
</body>
</html>

*{
    margin: 0;
    font-family: sans-serif;
    text-decoration: none;
    list-style: none;
    font-weight: bold;
}
body{
    background-image:url("pic.avif");
    
    
}
.nav{
    width: 100%;
    height: 50px;
    background-color:black;
    
}
span{
    margin: 1.5px 20px;
    color: yellow;
    font-size:20px;
    padding-right:0px;
    line-height: 50px;
}
.nav u1{
    float: right;
    padding:15px 5px ;
}
.nav u1 li{
    display: inline-block;
    margin: 2px 10px;
    line-height: 20px;
    padding-right: 35px;
}
.nav u1 li a{
    color: white;
    padding: 10px 5px;
}
.nav u1 li a:hover{
    color:yellow ;
    border-bottom: 2px solid yellow;
}

@media (max-width:768px){
  .nav u1{
    position:fixed;
    left:0;
    width:100px;
    height:100vh;
    background-color:rgb(216,216,79);
    text-align: center;
    padding: 0;
    top:50px;
    left: -100%;
    transition:2s ;
  }

  .nav u1 li {
    display:block ;
    width:100%;
    margin:0 ;
  }
}
.nav u1.slide{
    left: 0;
    transition:2s ;
}
.nav u1 li a{
    border:none;
    color:violet;
    padding-top:10px ;
}
.nav u1 li:hover{
    border-bottom:50px ;

}
.nav u1 li a:hover{
    border: none;
}
.nav u1 li:hover a{
    color:red;
}
/*.nav u1.slide{
    left: 0;
    transition:2s ;
}*/
  .hamburger{
    float:right;
    margin:1.5px;
    padding: right  20px;
    padding-top: 10px;
  }
  .hamburger line{
    width: 15px;
    height: 20px;
    background-color:white;
    margin-bottom: 10px;
    display:block;
  }
  
  const hamburger = document.querySelector('.hamburger');
const navbar = document.querySelector('u1');

hamburger.addEventListener('click', ()=>{
    navbar.classList.toggle('slide');
});
