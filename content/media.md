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
            width: 605px;
            height: 793px;
            background-image: url("/img/catsuit.jpg");
            display: flex;
            justify-items: center;
            align-items: center;
        }
        .eyes{
            position: relative;
            top: -215px;
            left: 39%;
            display: flex;
        }
        .eyes .eye{
            position: relative;
            width: 50px;
            height: 50px;
            display: block;
            background: #fff;
            margin: 0 15px;
            border-radius: 50%;
        }
        .eyes .eye::before{
            content: '';
            position: absolute;
            top: 50%;
            left: 15px;
            transform: translate(-50%,-50%);
            width: 20px;
            height: 20px;
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


<!-- {{< rawhtml >}}
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
{{< /rawhtml >}} -->



