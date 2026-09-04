q8qu.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AYHAM — YHARNAM HOST</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html,body{
    width:100%;
    height:100%;
    overflow:hidden;
    font-family:Georgia, "Times New Roman", serif;
    background:#090a0c;
}

/* BACKGROUND */
body{
    background:
        linear-gradient(
            to bottom,
            rgba(5,7,10,.25),
            rgba(5,6,8,.88)
        ),
        url("gehrman.jpg") center center / cover no-repeat;
}

/* DARK OVERLAY */
.overlay{
    position:fixed;
    inset:0;
    background:
        radial-gradient(
            circle at center,
            transparent 15%,
            rgba(0,0,0,.35) 55%,
            rgba(0,0,0,.9) 100%
        );
    pointer-events:none;
}

/* FOG */
.fog{
    position:fixed;
    inset:-30%;
    background:
        radial-gradient(
            ellipse,
            rgba(210,215,210,.10),
            transparent 65%
        );
    filter:blur(35px);
    animation:fogMove 18s infinite alternate ease-in-out;
    pointer-events:none;
}

@keyframes fogMove{
    from{
        transform:translateX(-5%) translateY(0);
    }
    to{
        transform:translateX(5%) translateY(-2%);
    }
}

/* MAIN */
.container{
    position:relative;
    z-index:5;

    width:100%;
    height:100%;

    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;

    padding:25px;
    text-align:center;
}

/* HEADER */
.small{
    font-size:12px;
    letter-spacing:5px;
    color:#aaa79d;
    margin-bottom:15px;
}

h1{
    font-size:clamp(35px,7vw,75px);
    letter-spacing:9px;
    color:#ddd8ca;
    text-shadow:
        0 3px 15px #000,
        0 0 30px rgba(130,20,20,.35);
}

.subtitle{
    margin-top:8px;
    font-size:14px;
    letter-spacing:7px;
    color:#8e8880;
}

.motto{
    margin-top:25px;
    font-style:italic;
    font-size:18px;
    letter-spacing:3px;
    color:#b7b0a3;
}

.divider{
    width:230px;
    height:1px;
    background:linear-gradient(
        90deg,
        transparent,
        #8d2929,
        transparent
    );
    margin:30px 0;
}

/* HOST PANEL */
.panel{
    width:min(620px,92vw);

    padding:35px 25px 40px;

    background:rgba(5,6,8,.72);

    border:1px solid rgba(150,120,90,.28);

    box-shadow:
        0 20px 70px rgba(0,0,0,.8),
        inset 0 0 40px rgba(0,0,0,.5);

    backdrop-filter:blur(5px);
}

.panel-title{
    font-size:12px;
    letter-spacing:5px;
    color:#817a70;
    margin-bottom:10px;
}

.panel h2{
    font-size:25px;
    letter-spacing:5px;
    color:#d0c8b8;
    margin-bottom:12px;
}

.panel p{
    color:#8d8981;
    font-size:14px;
    letter-spacing:1px;
    margin-bottom:25px;
}

/* HOST BUTTONS */
.host-button{
    position:relative;

    width:min(480px,90%);

    padding:18px 25px;
    margin:8px auto;

    border:1px solid #8e2929;

    background:
        linear-gradient(
            180deg,
            rgba(120,25,25,.65),
            rgba(45,8,8,.85)
        );

    color:#ddd5c5;

    font-family:Georgia,serif;
    font-size:16px;
    font-weight:bold;

    letter-spacing:3px;

    cursor:pointer;

    transition:.3s ease;

    box-shadow:
        0 0 20px rgba(100,0,0,.25),
        inset 0 0 20px rgba(0,0,0,.5);
}

.host-button:hover{
    transform:scale(1.025);

    border-color:#c24a4a;

    background:
        linear-gradient(
            180deg,
            rgba(150,30,30,.8),
            rgba(65,8,8,.9)
        );

    box-shadow:
        0 0 35px rgba(150,20,20,.45),
        inset 0 0 25px rgba(0,0,0,.5);
}

.host-button:active{
    transform:scale(.98);
}

.version{
    display:block;
    font-size:11px;
    letter-spacing:2px;
    color:#8b8175;
    margin-top:7px;
}

/* STATUS */
.status{
    margin-top:20px;

    font-size:11px;
    letter-spacing:3px;

    color:#77736c;
}

.status span{
    color:#9b3737;
}

/* FOOTER */
footer{
    position:absolute;
    bottom:20px;

    font-size:10px;
    letter-spacing:4px;

    color:#67635c;
}

.created{
    margin-top:7px;
    color:#504d48;
}

/* MOBILE */
@media(max-width:600px){

    h1{
        letter-spacing:5px;
    }

    .subtitle{
        letter-spacing:4px;
    }

    .motto{
        font-size:15px;
    }

    .panel{
        padding:28px 15px 32px;
    }

    .host-button{
        font-size:13px;
        letter-spacing:2px;
        padding:17px 12px;
    }

    .version{
        font-size:9px;
    }
}
</style>
</head>

<body>

<div class="overlay"></div>
<div class="fog"></div>

<div class="container">

    <div class="small">
        PLAYSTATION 4 • PRIVATE HOST
    </div>

    <h1>AYHAM</h1>

    <div class="subtitle">
        YHARNAM HOST
    </div>

    <div class="motto">
        Fear the old blood
    </div>

    <div class="divider"></div>

    <div class="panel">

        <div class="panel-title">
            HUNTER'S DREAM
        </div>

        <h2>
            PS4 HOST
        </h2>

        <p>
            Select your compatible firmware host
        </p>

        <!-- 7.00 - 11.02 -->
        <button
            class="host-button"
            onclick="launchHost('https://zecoxao.github.io/ntfonto/')">

            ★ &nbsp; PS4 7.00 → 11.02 &nbsp; ★

            <span class="version">
                NT FONT TOOL
            </span>

        </button>

        <!-- 11.50 - 13.00 -->
        <button
            class="host-button"
            onclick="launchHost('https://raw-game.com/zrm')">

            ★ &nbsp; PS4 11.50 → 13.00 &nbsp; ★

            <span class="version">
                ZRM HOST
            </span>

        </button>

        <div class="status">
            HOST STATUS:
            <span id="state">READY</span>
        </div>

    </div>

    <footer>
        FEAR THE OLD BLOOD

        <div class="created">
            CREATED BY AYHAM
        </div>
    </footer>

</div>

<script>

function launchHost(url){

    const state =
        document.getElementById("state");

    state.textContent =
        "OPENING HOST...";

    setTimeout(function(){

        window.location.href = url;

    },350);
}

</script>

</body>
</html>
