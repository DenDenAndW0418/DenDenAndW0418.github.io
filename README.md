<!DOCTYPE html>
<!--Hello dear friend.
    Sorry if the code is messy and considered approached in a primitive way.
    Did this at 3am on a school night.
-->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hi Crush! &lt;3</title>
    <link href="phone.css"rel="stylesheet">
</head>
<body>
    <div class="wrapper">
        <div class="btn button">
            <div class="bg btn circ"></div>
            <div class="bg circ" id="bg2"></div>
            <div class="bg circ" id="bg3"></div>
            <div class="bg circ" id="bg4"></div>
            <p class="text">Click Me!</p>
            <p class="text hide">Hi Crush</p>
            <p class="text hide">You are my favorite person!</p>
            <p class="text hide">Have a nice day! stay safe</p>
            <p class="text">Tap me</p>
            <p class="text hide">Hi Crush<small>Tap anywhere</small></p>
            <p class="text hide">You are my favorite person!<small>Tap anywhere</small></p>
            <p class="text hide">Have a nice day! stay safe<small>Tap again to refresh</small></p>
        </div>
        <div class="container">
            <div class="hearty heart x1"></div>
            <div class="hearty heart x2"></div>
            <div class="hearty heart x3"></div>
            <div class="hearty heart x4"></div>
            <div class="hearty heart x5"></div>
            <div class="hearty altheart x6"></div>
        </div>
    </div>
</body>
</html>
<script>
    const circ = document.querySelectorAll('.btn');
    const txt = document.querySelectorAll('.text');
    const bg = document.querySelectorAll('.bg');
    let i = 0;
    circ[0].addEventListener('click',()=>{
        circ[1].classList.toggle("inc");
        circ[0].classList.add("inc");
        bg[i].classList.add('inc');
        i++;
        if(i=>1){
            txt[i-1].classList.add('hide');
            txt[i].classList.remove('hide');
            if(i==3){
                circ[0].addEventListener('click',()=>{
                    txt[0].classList.remove('hide');
                    setTimeout(function(){
                        window.location.reload();
                    },1000);
                })
            }
        }
        else{
            txt[0].classList.add('hide');
            txt[i].classList.remove('hide');
        }
    })
</script>
