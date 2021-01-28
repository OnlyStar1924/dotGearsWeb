---
title: "Media"
date: 2021-01-12T16:32:57+07:00
draft: false
---

{{< rawhtml >}}
<head>
    <meta charset="utf-8">
    <style>
        body{
            
            justify-content: center;
            align-items: center;
            
        }

        .face{
            position: relative;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: #ffcd00;
            display: flex;
            justify-items: center;
            align-items: center;
        }
        .face::before{
            content: '';
            position: absolute;
            top: 180px;
            left: 75px;
            width: 150px;
            height: 70px;
            background: #b57700;
            border-bottom-left-radius: 70px;
            border-bottom-right-radius: 70px;
            transition: 0.5s;
        }
        .face:hover::before{
            
            top: 210px;
            width: 150px;
            height: 20px;
            background: #b57700;
            border-bottom-left-radius: 0px;
            border-bottom-right-radius: 0px;
        }
        .eyes{
            position: relative;
            top: -40px;
            left: 35px;
            display: flex;
        }
        .eyes .eye{
            position: relative;
            width: 80px;
            height: 80px;
            display: block;
            background: #fff;
            margin: 0 15px;
            border-radius: 50%;
        }
        .eyes .eye::before{
            content: '';
            position: absolute;
            top: 50%;
            left: 25px;
            transform: translate(-50%,-50%);
            width: 40px;
            height: 40px;
            background: #333;
            border-radius: 50%;
        }





    
    </style>

</head>
<body>
    <div class="face">
        <div class="eyes">
            <div class="eye"></div>
            <div class="eye"></div>
        </div>
    </div>

    <script>
        document.querySelector('body').addEventListener('mousemove', eyeball);
        function eyeball(){
            var eye = document.querySelectorAll('.eye');
            eye.forEach(function(eye){
                let x = (eye.getBoundingClientRect().left) + (eye.clientWidth / 2);
                let y = (eye.getBoundingClientRect().top) + (eye.clientHeight / 2);
                let radian = Math.atan2(event.pageX - x, event.pageY - y);
                let rot = (radian * (180 / Math.PI) * -1) + 270;
                eye.style.transform = "rotate("+ rot + "deg)"; 

            })
        }
    </script>
</body>



{{< /rawhtml >}}




<!-- 
{{< rawhtml>}}
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <style>
        svg {
            display: block;
            width: 80px;
            height: 80px;
            pointer-events: none;
            transform-style: preserve-3d;
        }
        circle.eye {
            fill: #a1a1b6;
        }
        path.top, path.bottom {
            fill: transparent;
            stroke: #a1a1b6;
            stroke-width: 1.3px;
            stroke-linecap: round;
        }
        .eye-outer {
            display: flex;
            align-items: flex-start;
            justify-content: center;
            margin-top: 15px;
        }
        .face {
            border: 8px solid #a1a1b6;
            border-radius: 50%;
            width: 220px;
            height: 220px;
        }
        .mouth-outer {
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .mouth-outer svg {
            width: 100px;
            height: 100px;
        }
        .mouth-outer path.top, .mouth-outer path.bottom {
            stroke-width: 2px;
        }
    </style>
  </head>
  <body>
    <div class="face">
       <div class="eye-outer">
          <div class="left-eye">
            <svg viewBox="0 0 21 21">
                <circle class="eye eye-left" cx="10.5" cy="10.5" r="2.25"></circle>
                <path class="top" d="M2 10.5C2 10.5 6.43686 5.5 10.5 5.5C14.5631 5.5 19 10.5 19 10.5"></path>
                <path class="bottom" d="M2 10.5C2 10.5 6.43686 15.5 10.5 15.5C14.5631 15.5 19 10.5 19 10.5"></path>
            </svg>  
          </div>
          <div class="right-eye">
             <svg viewBox="0 0 21 21">
                  <circle class="eye eye-right" cx="10.5" cy="10.5" r="2.25"></circle>
                  <path class="top" d="M2 10.5C2 10.5 6.43686 5.5 10.5 5.5C14.5631 5.5 19 10.5 19 10.5"></path>
                  <path class="bottom" d="M2 10.5C2 10.5 6.43686 15.5 10.5 15.5C14.5631 15.5 19 10.5 19 10.5"></path>
             </svg>
          </div>
       </div>
       <div class="mouth-outer">
         <svg viewBox="0 0 21 21">
              <path class="top" d="M2 10.5C2 10.5 6.43686 5.5 10.5 5.5C14.5631 5.5 19 10.5 19 10.5"></path>
              <path class="bottom" d="M2 10.5C2 10.5 6.43686 15.5 10.5 15.5C14.5631 15.5 19 10.5 19 10.5"></path>
         </svg> 
       </div>
    </div>
    <script type="text/javascript">
        const eye1 = document.querySelector('.eye-left');
        const eye2 = document.querySelector('.eye-right')
        window.addEventListener('mousemove', (evt) => {
            const x = -(window.innerWidth / 2 - evt.pageX) / 160;
            const y = -(window.innerHeight / 2 - evt.pageY) / 160;
            eye1.style.transform = `translateY(${y}px) translateX(${x}px)`;
            eye2.style.transform = `translateY(${y}px) translateX(${x}px)`;
        });  
    </script>
  </body>
</html>
{{</ rawhtml>}} -->