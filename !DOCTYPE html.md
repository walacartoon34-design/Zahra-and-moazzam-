#   
<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>Wedding Invitation | Zahra & Moaazam</title>  
  <link rel="preconnect" href="https://fonts.googleapis.com">  
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>  
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Great+Vibes&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">  
  <style>  
    :root {  
      --bg-cream: #fbf7f4;  
      --gold: #c5a059;  
      --dark-gold: #9e7d3b;  
      --burgundy: #72202b;  
      --text-dark: #3a322d;  
      --text-muted: #7d7268;  
    }  
    * {  
      box-sizing: border-box;  
      margin: 0;  
      padding: 0;  
    }  
    body {  
      background-color: #2b2623;  
      font-family: 'Montserrat', sans-serif;  
      color: var(--text-dark);  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      min-height: 100vh;  
      overflow-x: hidden;  
    }  
    .mobile-frame {  
      width: 100%;  
      max-width: 430px;  
      min-height: 100vh;  
      background: var(--bg-cream);  
      position: relative;  
      box-shadow: 0 10px 40px rgba(0,0,0,0.4);  
      overflow-x: hidden;  
    }  
  
    /* Envelope Splash Screen */  
    #envelope-screen {  
      position: fixed;  
      top: 0;  
      left: 50%;  
      transform: translateX(-50%);  
      width: 100%;  
      max-width: 430px;  
      height: 100vh;  
      background: #f4eee8;  
      background-image: radial-gradient(#dfd4c8 1px, transparent 1px);  
      background-size: 20px 20px;  
      z-index: 1000;  
      display: flex;  
      flex-direction: column;  
      align-items: center;  
      justify-content: center;  
      transition: opacity 0.8s ease, visibility 0.8s ease;  
    }  
    .envelope-box {  
      width: 310px;  
      height: 220px;  
      background: #eae2d8;  
      position: relative;  
      border-radius: 6px;  
      box-shadow: 0 15px 35px rgba(0,0,0,0.15);  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      border: 1px solid #d8ccbf;  
    }  
    .envelope-flap {  
      position: absolute;  
      top: 0;  
      left: 0;  
      width: 0;  
      height: 0;  
      border-left: 155px solid transparent;  
      border-right: 155px solid transparent;  
      border-top: 120px solid #dfd5c8;  
      transform-origin: top;  
      transition: transform 0.6s ease;  
      z-index: 3;  
    }  
    .wax-seal {  
      width: 75px;  
      height: 75px;  
      background: radial-gradient(circle, #85222d 40%, #5a141d 100%);  
      border-radius: 50%;  
      position: absolute;  
      top: 85px;  
      z-index: 5;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      color: #dfba73;  
      font-family: 'Cinzel', serif;  
      font-size: 20px;  
      font-weight: 700;  
      cursor: pointer;  
      box-shadow: 0 6px 15px rgba(0,0,0,0.3), inset 0 0 0 2px rgba(223, 186, 115, 0.4);  
      animation: pulse 1.8s infinite;  
    }  
    @keyframes pulse {  
      0% { transform: scale(1); }  
      50% { transform: scale(1.06); }  
      100% { transform: scale(1); }  
    }  
    .tap-text {  
      position: absolute;  
      bottom: -45px;  
      font-size: 13px;  
      color: var(--burgundy);  
      letter-spacing: 2px;  
      text-transform: uppercase;  
      font-weight: 500;  
    }  
  
    /* Music Floating Button */  
    .music-btn {  
      position: fixed;  
      bottom: 25px;  
      right: calc(50% - 195px);  
      width: 44px;  
      height: 44px;  
      border-radius: 50%;  
      background: var(--burgundy);  
      color: #fff;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      border: 2px solid var(--gold);  
      cursor: pointer;  
      z-index: 99;  
      box-shadow: 0 5px 15px rgba(0,0,0,0.25);  
    }  
  
    /* Main Invitation Content */  
    .card-content {  
      padding: 40px 25px 90px 25px;  
      text-align: center;  
      background-image: linear-gradient(to bottom, #fdfbf9, #f7f1ea);  
    }  
    .bismillah {  
      font-family: 'Cinzel', serif;  
      font-size: 19px;  
      color: var(--dark-gold);  
      margin-bottom: 12px;  
    }  
    .dua-arabic {  
      font-size: 18px;  
      line-height: 1.8;  
      color: var(--burgundy);  
      font-weight: 600;  
      margin: 15px 0 6px 0;  
    }  
    .dua-trans {  
      font-size: 12.5px;  
      font-style: italic;  
      color: var(--text-muted);  
      margin-bottom: 25px;  
      line-height: 1.5;  
    }  
    .couple-title {  
      font-family: 'Cinzel', serif;  
      letter-spacing: 3px;  
      font-size: 11px;  
      text-transform: uppercase;  
      color: var(--text-muted);  
      margin-bottom: 10px;  
    }  
    .couple-names {  
      font-family: 'Great Vibes', cursive;  
      font-size: 48px;  
      color: var(--burgundy);  
      line-height: 1.2;  
      margin-bottom: 25px;  
    }  
    .divider {  
      width: 80px;  
      height: 2px;  
      background: var(--gold);  
      margin: 20px auto;  
      position: relative;  
    }  
    .divider::after {  
      content: '◆';  
      position: absolute;  
      top: -9px;  
      left: 50%;  
      transform: translateX(-50%);  
      background: #fdfbf9;  
      padding: 0 6px;  
      color: var(--gold);  
      font-size: 12px;  
    }  
  
    /* Countdown */  
    .countdown-title {  
      font-family: 'Cinzel', serif;  
      font-size: 13px;  
      letter-spacing: 2px;  
      text-transform: uppercase;  
      color: var(--dark-gold);  
      margin-top: 15px;  
      margin-bottom: 12px;  
    }  
    .countdown-timer {  
      display: flex;  
      justify-content: center;  
      gap: 10px;  
      margin-bottom: 35px;  
    }  
    .time-unit {  
      background: #fff;  
      border: 1px solid #ebd9c2;  
      border-radius: 8px;  
      padding: 10px 8px;  
      min-width: 65px;  
      box-shadow: 0 4px 10px rgba(0,0,0,0.03);  
    }  
    .time-number {  
      font-size: 20px;  
      font-weight: 700;  
      color: var(--burgundy);  
      display: block;  
    }  
    .time-label {  
      font-size: 10px;  
      text-transform: uppercase;  
      color: var(--text-muted);  
      letter-spacing: 1px;  
    }  
  
    /* Event Cards */  
    .section-heading {  
      font-family: 'Cinzel', serif;  
      font-size: 20px;  
      letter-spacing: 2px;  
      color: var(--dark-gold);  
      margin: 30px 0 20px 0;  
      text-transform: uppercase;  
    }  
    .event-card {  
      background: #fff;  
      border-radius: 12px;  
      border: 1px solid #ebdfd0;  
      padding: 22px 18px;  
      margin-bottom: 20px;  
      box-shadow: 0 6px 18px rgba(0,0,0,0.04);  
      text-align: center;  
    }  
    .event-card.barat {  
      border-top: 4px solid var(--burgundy);  
    }  
    .event-card.mehndi {  
      border-top: 4px solid #d49826;  
    }  
    .event-name {  
      font-family: 'Cinzel', serif;  
      font-size: 20px;  
      color: var(--burgundy);  
      margin-bottom: 6px;  
    }  
    .event-date {  
      font-size: 14px;  
      font-weight: 600;  
      color: var(--text-dark);  
      margin-bottom: 8px;  
    }  
    .event-venue {  
      font-size: 13.5px;  
      color: var(--text-muted);  
      margin-bottom: 15px;  
      line-height: 1.4;  
    }  
    .btn-map {  
      display: inline-block;  
      padding: 9px 20px;  
      background: transparent;  
      color: var(--burgundy);  
      border: 1.5px solid var(--burgundy);  
      border-radius: 25px;  
      font-size: 12px;  
      font-weight: 600;  
      text-decoration: none;  
      transition: all 0.3s;  
    }  
    .btn-map:hover {  
      background: var(--burgundy);  
      color: #fff;  
    }  
  
    /* Contacts & RSVP */  
    .contact-box {  
      background: #f5ece2;  
      border-radius: 10px;  
      padding: 18px;  
      margin: 25px 0;  
    }  
    .contact-box h4 {  
      font-family: 'Cinzel', serif;  
      font-size: 13px;  
      letter-spacing: 1.5px;  
      color: var(--dark-gold);  
      margin-bottom: 10px;  
      text-transform: uppercase;  
    }  
    .contact-numbers {  
      display: flex;  
      flex-direction: column;  
      gap: 6px;  
    }  
    .contact-numbers a {  
      color: var(--burgundy);  
      text-decoration: none;  
      font-weight: 600;  
      font-size: 14px;  
    }  
  
    /* RSVP Form */  
    .rsvp-section {  
      background: #fff;  
      border-radius: 12px;  
      border: 1px solid #ebdfd0;  
      padding: 22px 18px;  
      margin-top: 30px;  
      box-shadow: 0 6px 18px rgba(0,0,0,0.04);  
    }  
    .rsvp-section h3 {  
      font-family: 'Cinzel', serif;  
      font-size: 18px;  
      color: var(--burgundy);  
      margin-bottom: 10px;  
      letter-spacing: 1px;  
    }  
    .rsvp-input {  
      width: 100%;  
      padding: 12px;  
      margin: 8px 0;  
      border: 1px solid #d4c5b3;  
      border-radius: 6px;  
      font-size: 13px;  
      font-family: inherit;  
    }  
    .btn-submit {  
      width: 100%;  
      background: var(--burgundy);  
      color: #fff;  
      border: none;  
      padding: 13px;  
      border-radius: 25px;  
      font-size: 13px;  
      font-weight: 600;  
      letter-spacing: 1px;  
      cursor: pointer;  
      margin-top: 10px;  
      transition: opacity 0.3s;  
    }  
    .footer-msg {  
      font-family: 'Great Vibes', cursive;  
      font-size: 26px;  
      color: var(--dark-gold);  
      margin-top: 35px;  
    }  
  </style>  
</head>  
<body>  
  
  <div class="mobile-frame">  
  
    <!-- Envelope Screen -->  
    <div id="envelope-screen">  
      <div class="envelope-box">  
        <div class="envelope-flap" id="envelope-flap"></div>  
        <div class="wax-seal" id="wax-seal" onclick="openInvitation()">  
          <span>Z&M</span>  
        </div>  
        <div class="tap-text">Tap seal to open</div>  
      </div>  
    </div>  
  
    <!-- Music Button -->  
    <button class="music-btn" id="musicBtn" onclick="toggleMusic()" title="Play / Pause Music">  
      🎵  
    </button>  
    <audio id="bgAudio" loop preload="auto">  
      <source src="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=romantic-wedding-114058.mp3" type="audio/mp3">  
    </audio>  
  
    <!-- Main Card Body -->  
    <div class="card-content">  
      <div class="bismillah">بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ</div>  
        
      <div class="dua-arabic">  
        وَمِنْ آيَاتِهِ أَنْ خَلَقَ لَكُم مِّنْ أَنفُسِكُمْ أَزْوَاجًا لِّتَسْكُنُوا إِلَيْهَا وَجَعَلَ بَيْنَكُم مَّوَدَّةً وَرَحْمَةً  
      </div>  
      <div class="dua-trans">  
        "Aur uski nishaniyon me se hai ke usne tumhare liye tumhari hi jins se jode banaye taake tum unke paas sukoon pao, aur tumhare darmiyan mohabbat aur rehmat paida kardi." (Surah Ar-Rum: 21)  
      </div>  
  
      <div class="divider"></div>  
  
      <div class="couple-title">Together with their families</div>  
      <div class="couple-names">Zahra & Moaazam</div>  
      <div class="couple-title">Request the honor of your presence to celebrate their wedding</div>  
  
      <!-- Countdown -->  
      <div class="countdown-title">Countdown to Celebration</div>  
      <div class="countdown-timer">  
        <div class="time-unit">  
          <span class="time-number" id="days">00</span>  
          <span class="time-label">Days</span>  
        </div>  
        <div class="time-unit">  
          <span class="time-number" id="hours">00</span>  
          <span class="time-label">Hours</span>  
        </div>  
        <div class="time-unit">  
          <span class="time-number" id="minutes">00</span>  
          <span class="time-label">Mins</span>  
        </div>  
        <div class="time-unit">  
          <span class="time-number" id="seconds">00</span>  
          <span class="time-label">Secs</span>  
        </div>  
      </div>  
  
      <div class="divider"></div>  
      <div class="section-heading">Events & Schedule</div>  
  
      <!-- Mehndi -->  
      <div class="event-card mehndi">  
        <div class="event-name">Mehndi</div>  
        <div class="event-date">Friday, 23rd January 2027</div>  
        <div class="event-venue">  
          <strong>Venue:</strong> Gold Palace Hall, Lahore  
        </div>  
        <a href="https://maps.app.goo.gl/EAHgosgtGuVMXNow7?g_st=ic" target="_blank" class="btn-map">  
          📍 View Hall Location  
        </a>  
      </div>  
  
      <!-- Barat -->  
      <div class="event-card barat">  
        <div class="event-name">Barat</div>  
        <div class="event-date">Saturday, 24th January 2027</div>  
        <div class="event-venue">  
          <strong>Venue:</strong> Silk Marquee, Lahore  
        </div>  
        <a href="https://maps.app.goo.gl/mBFcH9pQB2NS5w2c9?g_st=ic" target="_blank" class="btn-map">  
          📍 View Marquee Location  
        </a>  
      </div>  
  
      <!-- Contacts -->  
      <div class="contact-box">  
        <h4>For Queries & Information</h4>  
        <div class="contact-numbers">  
          <a href="tel:03214701588">📞 0321-4701588</a>  
          <a href="tel:03046175021">📞 0304-6175021</a>  
        </div>  
      </div>  
  
      <!-- RSVP Form -->  
      <div class="rsvp-section">  
        <h3>Confirm Your Attendance</h3>  
        <p style="font-size: 12px; color: var(--text-muted); margin-bottom: 12px;">Kindly let us know if you will be joining us</p>  
        <input type="text" id="guestName" class="rsvp-input" placeholder="Your Full Name" required>  
        <input type="number" id="guestCount" class="rsvp-input" placeholder="Total Guests Attending" min="1" value="1">  
        <button class="btn-submit" onclick="sendRSVP()">Send RSVP on WhatsApp</button>  
      </div>  
  
      <div class="footer-msg">We look forward to celebrating with you!</div>  
    </div>  
  
  </div>  
  
  <script>  
    // Open Envelope  
    function openInvitation() {  
      const seal = document.getElementById('wax-seal');  
      const flap = document.getElementById('envelope-flap');  
      const screen = document.getElementById('envelope-screen');  
      const audio = document.getElementById('bgAudio');  
  
      flap.style.transform = 'rotateX(180deg)';  
      seal.style.opacity = '0';  
      seal.style.transition = 'opacity 0.4s ease';  
  
      // Play audio on user click  
      audio.play().catch(e => console.log('Audio autoplay prevented:', e));  
  
      setTimeout(() => {  
        screen.style.opacity = '0';  
        setTimeout(() => {  
          screen.style.display = 'none';  
        }, 800);  
      }, 600);  
    }  
  
    // Toggle Music  
    let isPlaying = true;  
    function toggleMusic() {  
      const audio = document.getElementById('bgAudio');  
      const btn = document.getElementById('musicBtn');  
      if (audio.paused) {  
        audio.play();  
        btn.innerHTML = '🎵';  
      } else {  
        audio.pause();  
        btn.innerHTML = '🔇';  
      }  
    }  
  
    // Countdown Timer (23 Jan 2027)  
    const weddingDate = new Date("Jan 23, 2027 19:00:00").getTime();  
    setInterval(function() {  
      const now = new Date().getTime();  
      const distance = weddingDate - now;  
  
      const days = Math.floor(distance / (1000 * 60 * 60 * 24));  
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));  
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));  
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);  
  
      document.getElementById("days").innerHTML = days > 0 ? (days < 10 ? '0' + days : days) : '00';  
      document.getElementById("hours").innerHTML = hours > 0 ? (hours < 10 ? '0' + hours : hours) : '00';  
      document.getElementById("minutes").innerHTML = minutes > 0 ? (minutes < 10 ? '0' + minutes : minutes) : '00';  
      document.getElementById("seconds").innerHTML = seconds > 0 ? (seconds < 10 ? '0' + seconds : seconds) : '00';  
    }, 1000);  
  
    // RSVP to WhatsApp  
    function sendRSVP() {  
      const name = document.getElementById('guestName').value.trim();  
      const count = document.getElementById('guestCount').value;  
        
      if (!name) {  
        alert("Please enter your name.");  
        return;  
      }  
        
      const message = `Assalam-o-Alaikum! RSVP Confirmation for Zahra & Moaazam Wedding:%0A- Name: ${name}%0A- Guests Attending: ${count}`;  
      const whatsappURL = `https://wa.me/923214701588?text=${message}`;  
      window.open(whatsappURL, '_blank');  
    }  
  </script>  
</body>  
</html>  
