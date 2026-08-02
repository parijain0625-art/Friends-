// ---------------- Typewriter ----------------
const text =
"Every smile, every memory, every festival, every laugh... Thank you for being my forever best friend, Nonny ❤️";

let i = 0;

function typeWriter() {
    if (i < text.length) {
        document.getElementById("typing").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeWriter, 45);
    }
}

window.onload = () => {
    typeWriter();
};

// ---------------- Scroll ----------------
function scrollToGallery() {
    document.getElementById("gallery").scrollIntoView({
        behavior: "smooth"
    });
}

// ---------------- Music ----------------
const music = document.getElementById("music");
const musicBtn = document.getElementById("musicBtn");

let playing = false;

musicBtn.onclick = () => {
    if (!playing) {
        music.play();
        musicBtn.innerHTML = "⏸️";
    } else {
        music.pause();
        musicBtn.innerHTML = "🎵";
    }
    playing = !playing;
};

// ---------------- 100 Reasons ----------------
const reasons = [

"You always understand me ❤️",
"You make every day brighter.",
"You never judge me.",
"You always support my dreams.",
"You know me better than anyone.",
"You make me laugh.",
"You stand beside me.",
"You celebrate my happiness.",
"You cheer me up.",
"You are my comfort zone.",

"Your smile is priceless.",
"You are my safe place.",
"You are my biggest blessing.",
"You are family.",
"You make ordinary days special.",
"You never give up on me.",
"You listen patiently.",
"You inspire me.",
"You believe in me.",
"You make life beautiful."

];

// Fill remaining automatically
while(reasons.length<100){
reasons.push("Because you're simply the best friend anyone could ever ask for. ❤️");
}

let index=0;

function nextReason(){

document.getElementById("reasonCard").innerHTML=reasons[index];

index++;

if(index>=100){
index=0;
}

}

nextReason();

// ---------------- Floating Hearts ----------------

function createHeart(){

const heart=document.createElement("div");

heart.innerHTML="❤️";

heart.style.position="fixed";
heart.style.left=Math.random()*100+"vw";
heart.style.top="-30px";
heart.style.fontSize=(20+Math.random()*25)+"px";
heart.style.zIndex="999";

document.body.appendChild(heart);

let pos=-30;

const timer=setInterval(()=>{

pos+=3;

heart.style.top=pos+"px";

if(pos>window.innerHeight){

clearInterval(timer);

heart.remove();

}

},25);

}

setInterval(createHeart,500);

// ---------------- Surprise ----------------

function celebrate(){

document.getElementById("finalMessage").style.display="block";

confetti();

fireworks();

}

// ---------------- Confetti ----------------

function confetti(){

for(let i=0;i<180;i++){

const c=document.createElement("div");

c.style.position="fixed";
c.style.width="8px";
c.style.height="8px";
c.style.left=Math.random()*100+"vw";
c.style.top="-20px";

const colors=["#ff4d88","#ffd700","#ffffff","#00ffff","#90ee90"];

c.style.background=colors[Math.floor(Math.random()*colors.length)];

document.body.appendChild(c);

let y=-20;

const t=setInterval(()=>{

y+=5;

c.style.top=y+"px";

if(y>window.innerHeight){

clearInterval(t);

c.remove();

}

},15);

}

}

// ---------------- Fireworks ----------------

function fireworks(){

for(let j=0;j<12;j++){

setTimeout(()=>{

const x=Math.random()*window.innerWidth;
const y=Math.random()*window.innerHeight/2;

for(let i=0;i<40;i++){

const spark=document.createElement("div");

spark.style.position="fixed";
spark.style.width="6px";
spark.style.height="6px";
spark.style.borderRadius="50%";
spark.style.background="gold";
spark.style.left=x+"px";
spark.style.top=y+"px";

document.body.appendChild(spark);

const angle=Math.random()*2*Math.PI;
const speed=Math.random()*6+2;

let dx=Math.cos(angle)*speed;
let dy=Math.sin(angle)*speed;

let px=x;
let py=y;

const timer=setInterval(()=>{

px+=dx;

py+=dy;

dy+=0.05;

spark.style.left=px+"px";
spark.style.top=py+"px";

spark.style.opacity-=0.02;

if(parseFloat(spark.style.opacity)<=0){

clearInterval(timer);

spark.remove();

}

},20);

}

},j*350);

}

}
