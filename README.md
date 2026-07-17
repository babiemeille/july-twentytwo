# july-twentytwo
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday 🎂</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:"Poppins",sans-serif;
}

body{
    background:linear-gradient(135deg,#ffd6e7,#ffeec9,#d8f3ff);
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
    overflow:hidden;
}

.card{
    width:90%;
    max-width:700px;
    background:rgba(255,255,255,.8);
    backdrop-filter:blur(10px);
    padding:40px;
    border-radius:25px;
    text-align:center;
    box-shadow:0 15px 35px rgba(0,0,0,.15);
    animation:fade 1.5s;
}

h1{
    color:#ff4f8b;
    font-size:2.8rem;
}

p{
    margin-top:20px;
    color:#444;
    line-height:1.8;
    font-size:18px;
}

button{
    margin-top:30px;
    padding:15px 35px;
    border:none;
    border-radius:30px;
    background:#ff6b9e;
    color:white;
    font-size:18px;
    cursor:pointer;
    transition:.3s;
}

button:hover{
    transform:scale(1.08);
    background:#ff4f8b;
}

#secret{
    margin-top:25px;
    color:#ff4f8b;
    font-size:22px;
    display:none;
    animation:fade 1s;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(20px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.heart{
    position:absolute;
    color:#ff5e95;
    animation:float 6s linear infinite;
}

@keyframes float{
    from{
        transform:translateY(100vh);
        opacity:1;
    }
    to{
        transform:translateY(-120vh);
        opacity:0;
    }
}
</style>
</head>

<body>

<div class="card">
    <h1>🎂 Happy Birthday 🎂</h1>

    <p>
        สุขสันต์วันเกิดนะ 🤍<br><br>

        ขอให้ปีนี้เป็นปีที่เต็มไปด้วยรอยยิ้ม ความสุข
        และเรื่องราวดี ๆ ที่เข้ามาไม่ขาดสาย
        ขอให้ทุกความตั้งใจของเธอค่อย ๆ กลายเป็นจริง
        มีคนรัก คนเอ็นดู และรายล้อมไปด้วยความอบอุ่นเสมอ

        ขอให้สุขภาพแข็งแรง
        ได้เจอสิ่งที่ทำให้หัวใจเต้นแรงในทุก ๆ วัน
        และไม่ว่าจะเหนื่อยแค่ไหน
        ก็ขอให้ยังมีความหวังและความสุขอยู่กับเธอเสมอ

        ขอให้เธอเป็นตัวเองในเวอร์ชันที่มีความสุขที่สุดนะ 💖
    </p>

    <button onclick="showMessage()">
        กดรับคำอวยพรพิเศษ 🎁
    </button>

    <div id="secret">
        🌸 ขอให้เธอมีความสุขมาก ๆ ในทุกวัน
        และจำไว้นะ...
        "เธอคือของขวัญที่มีค่าของโลกใบนี้" 💕
    </div>
</div>

<script>

function showMessage(){
    document.getElementById("secret").style.display="block";
}

function createHeart(){

    const heart=document.createElement("div");

    heart.className="heart";

    heart.innerHTML=["💖","💕","💗","💓","🌸","✨"][Math.floor(Math.random()*6)];

    heart.style.left=Math.random()*100+"vw";

    heart.style.fontSize=(20+Math.random()*25)+"px";

    heart.style.animationDuration=(4+Math.random()*4)+"s";

    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },7000);
}

setInterval(createHeart,300);

</script>

</body>
</html>
