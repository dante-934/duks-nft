<meta name='viewport' content='width=device-width, initial-scale=1'/><script>const canvas = document.getElementById('gameCanvas');
const ctx = canvas.getContext('2d');
let gameRunning = false;
let p, e, world = { joy: {x:0, y:0} };

function openBook() { 
    document.getElementById('book').classList.add('open'); 
    document.getElementById('start-btn').style.display = 'none';
}
function showMap() {
    document.getElementById('scene-menu').classList.remove('active');
    document.getElementById('scene-map').classList.add('active');
}
function startFight() {
    document.getElementById('scene-map').classList.remove('active');
    document.getElementById('scene-battle').classList.add('active');
    initGame();
}

const imgs = {
    p: 'https://i.pinimg.com/736x/8e/98/67/8e9867e24d43c056b5dbffa2f5a3e1dd.jpg',
    e: 'https://i.pinimg.com/736x/1f/f4/3a/1ff43ae3cffb05a3c30b3cb77d9a192b.jpg'
};
const loaded = {};

function initGame() {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
    let count = 0;
    for(let k in imgs) {
        loaded[k] = new Image(); loaded[k].src = imgs[k];
        loaded[k].onload = () => { if(++count === 2) { gameRunning = true; loop(); } };
    }
    p = { x: 100, y: 0, hp: 100, w: 180, h: 280, vy: 0 };
    e = { x: canvas.width - 300, y: 0, hp: 100, w: 180, h: 280 };
}

function doAttack() {
    if(Math.abs(p.x - e.x) < 250) {
        e.hp -= 5;
        document.getElementById('e-fill').style.width = Math.max(0, e.hp) + '%';
        // ТРЯСКА УБРАНА
    }
}

function loop() {
    if(!gameRunning) return;
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    
    // Движение
    p.x += world.joy.x * 10;
    if(world.joy.y < -0.5 && p.y === 0) p.vy = -20;
    p.y += p.vy;
    if(p.y < 0) p.vy += 1.2; else { p.y = 0; p.vy = 0; }
    
    const ground = canvas.height * 0.9;
    ctx.drawImage(loaded.p, p.x, ground - p.h + p.y, p.w, p.h);
    
    ctx.save();
    ctx.translate(e.x + e.w, ground - e.h);
    ctx.scale(-1, 1);
    ctx.drawImage(loaded.e, 0, 0, e.w, e.h);
    ctx.restore();

    if(e.hp > 0) requestAnimationFrame(loop);
}

// Джойстик
const joy = document.getElementById('joy'), stick = document.getElementById('stick');
const updateJoy = (ev) => {
    ev.preventDefault();
    const r = joy.getBoundingClientRect();
    const t = ev.touches ? ev.touches[0] : ev;
    let dx = t.clientX - (r.left + 45), dy = t.clientY - (r.top + 45);
    let d = Math.min(Math.sqrt(dx*dx+dy*dy), 40);
    let a = Math.atan2(dy, dx);
    world.joy.x = Math.cos(a) * d / 40;
    world.joy.y = Math.sin(a) * d / 40;
    stick.style.transform = `translate(${world.joy.x*30}px, ${world.joy.y*30}px)`;
};
joy.addEventListener('touchstart', updateJoy);
joy.addEventListener('touchmove', updateJoy);
joy.addEventListener('touchend', () => { world.joy = {x:0, y:0}; stick.style.transform = 'none'; });
document.getElementById('atk-btn').addEventListener('touchstart', (e) => { e.preventDefault(); doAttack(); });
</script>