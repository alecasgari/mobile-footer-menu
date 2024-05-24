# Magic Mobile Footer Menu
## Demo
Take a look at this beatiful demo here: [Link Coming Soon]
## How 2 Use?
You have a `CSS` file here:
```CSS
@import url('https://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900');
*
{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

:root
{
    --clr: #223327;
}

body
{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: var(--clr);
}

.navigation
{
    position: relative;
    width: 400px;
    height: 70px;
    background: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 10px;

}
.navigation ul
{
    display: flex;
    width: 350px;
}
.navigation ul li
{
    position: relative;
    list-style: none;
    width: 70px;
    height: 70px;
    z-index: 1;
}
.navigation ul li a
{
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
    text-align: center;
    font-weight: 500;
}
.navigation ul li a .icon
{
    position: relative;
    display: block;
    line-height: 75px;
    font-size: 1.5em;
    text-align: center;
    transition: 0.5s;
    color: var(--clr);
}
.navigation ul li.active a .icon
{
    transform: translateY(-32px);
}
.navigation ul li a .text
{
    position: absolute;
    color: var(--clr);
    font-weight: 400;
    font-size: 0.75em;
    letter-spacing: 0.05;
    transition: 0.5s;
    opacity: 0;
    transform: translateY(20px);
}
.navigation ul li.active a .text
{
    opacity: 1;
    transform: translateY(10px);
}
.indicator
{
    position: absolute;
    top: -50%;
    width: 70px;
    height: 70px;
    background: #29fd53;
    border-radius: 50%;
    border: 6px solid var(--clr);
    transition: 0.5s;

}
.indicator::before
{
    content: '';
    position: absolute;
    top: 50%;
    left: -22px;
    width: 20px;
    height: 20px;
    background: transparent;
    border-top-right-radius: 20px;
    box-shadow: 0px -10px 0 0 var(--clr);
}
.indicator::after
{
    content: '';
    position: absolute;
    top: 50%;
    right: -22px;
    width: 20px;
    height: 20px;
    background: transparent;
    border-top-left-radius: 20px;
    box-shadow: -1px -10px 0 0 var(--clr);
}
.navigation ul li:nth-child(1).active ~ .indicator
{
transform: translateX(calc(70px * 0));
}
.navigation ul li:nth-child(2).active ~ .indicator
{
transform: translateX(calc(70px * 1));
}
.navigation ul li:nth-child(3).active ~ .indicator
{
transform: translateX(calc(70px * 2));
}
.navigation ul li:nth-child(4).active ~ .indicator
{
transform: translateX(calc(70px * 3));
}
.navigation ul li:nth-child(5).active ~ .indicator
{
transform: translateX(calc(70px * 4));
}
```
and `HTML` here:
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Magic Menu Indicator</title>
    <link rel="stylesheet" type="text/css" href="style.css"
</head>
<body>
    <div class="navigation">
        <ul>
            <li class="list active">
                <a href="#">
                    <span class="icon">
                        <ion-icon name="home-outline"></ion-icon>
                    </span>
                    <span class="text">Home</span>
                </a>
            </li>
            <li class="list">
                <a href="#">
                    <span class="icon">
                        <ion-icon name="person-outline"></ion-icon>
                    </span>
                    <span class="text">Profile</span>
                </a>
            </li>
            <li class="list">
                <a href="#">
                    <span class="icon">
                        <ion-icon name="chatbubble-outline"></ion-icon>
                    </span>
                    <span class="text">Message</span>
                </a>
            </li>
            <li class="list">
                <a href="#">
                    <span class="icon">
                        <ion-icon name="camera-outline"></ion-icon>
                    </span>
                    <span class="text">Photos</span>
                </a>
            </li>
            <li class="list">
                <a href="#">
                    <span class="icon">
                        <ion-icon name="settings-outline"></ion-icon>
                    </span>
                    <span class="text">Setting</span>
                </a>
            </li>
            <div class="indicator">

            </div>
        </ul>
    </div>
</body>
</html>
```
Also this `Javascrip` is neede:
```Javascript
 <script>
        const list = document.querySelectorAll('.list');
        function activeLink(){
            list.forEach((item) => 
            item.classList.remove('active'));
            this.classList.add('active');
        }
        list.forEach((item) => 
        item.addEventListener('click',activeLink));
        </script>

    <script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
    <script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
```
## Enjoy It
