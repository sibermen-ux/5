<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Sana Özel ❤️</title>
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&display=swap');

        * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }

        body, html {
            margin: 0; padding: 0; width: 100%; height: 100%;
            font-family: 'Poppins', sans-serif;
            background-color: #fff5f7; overflow: hidden;
        }

        /* 💓 EMOJİ YAĞMURU SİSTEMİ (TEKNİK OLARAK GÜÇLENDİRİLDİ) */
        #emoji-layer {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            pointer-events: none; z-index: 1; overflow: hidden;
        }
        .emoji {
            position: absolute; top: -50px; font-size: 26px;
            will-change: transform; animation: flow linear forwards;
        }
        @keyframes flow { to { transform: translateY(110vh) rotate(360deg); } }

        /* KATMANLAR VE GEÇİŞLER */
        .katman {
            width: 100%; height: 100vh; position: absolute; top: 0; left: 0;
            display: flex; flex-direction: column; align-items: center;
            transition: transform 0.9s cubic-bezier(0.7, 0, 0.3, 1);
            z-index: 5; padding: 20px;
        }

        #katman1 { background: linear-gradient(to bottom, #fff5f7, #ffe3ec); justify-content: center; }
        #katman2 { background: #ffffff; transform: translateY(100%); overflow-y: auto; display: block; padding-top: 40px; }
        #katman3 { background: #fffcfd; transform: translateY(100%); overflow-y: auto; display: block; padding-top: 40px; }

        /* MEKTUP KUTUSU - MOBİL UYUMLU */
        .mektup-kutu {
            max-width: 550px; margin: 0 auto 30px auto; padding: 35px 25px;
            background: rgba(255, 255, 255, 0.95); border-radius: 25px;
            box-shadow: 0 15px 35px rgba(255, 77, 109, 0.1);
            border: 1px solid #fce4ec; position: relative; z-index: 10;
        }

        .mektup-metni {
            font-size: 1.05rem; line-height: 1.8; color: #444;
            white-space: pre-line; text-align: left;
        }

        /* TUŞLARIN DÜZELTİLMİŞ HALİ */
        .devam-btn {
            display: inline-block; padding: 16px 45px;
            background: #ff4d6d; color: white; border: none;
            border-radius: 50px; font-size: 1.1rem; font-weight: 600;
            cursor: pointer; box-shadow: 0 8px 20px rgba(255, 77, 109, 0.3);
            text-align: center; margin: 20px auto; transition: 0.3s;
        }
        .devam-btn:active { transform: scale(0.95); }

        /* ŞİİRLER GRİD SİSTEMİ */
        .siir-grid {
            display: grid; grid-template-columns: repeat(5, 1fr); gap: 12px;
            max-width: 450px; margin: 20px auto; padding-bottom: 80px;
        }
        .kutucuk {
            aspect-ratio: 1; background: #ffe3ec; color: #ff4d6d;
            display: flex; align-items: center; justify-content: center;
            border-radius: 15px; font-weight: bold; cursor: pointer; transition: 0.3s;
        }
        .kutucuk:hover { background: #ff4d6d; color: white; }

        /* MODAL */
        .modal {
            display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.85); z-index: 2000; align-items: center; justify-content: center;
            backdrop-filter: blur(5px);
        }
        .modal-icerik {
            background: white; padding: 35px; border-radius: 30px; width: 85%;
            max-width: 450px; text-align: center; position: relative;
        }

        @media (max-width: 500px) {
            .siir-grid { grid-template-columns: repeat(4, 1fr); }
            .mektup-kutu { margin: 10px; padding: 25px 20px; }
            .mektup-metni { font-size: 0.95rem; }
        }
    </style>
</head>
<body>

    <div id="emoji-layer"></div>

    <section id="katman1" class="katman">
        <div style="padding: 30px; border-radius: 30px; background: rgba(255,255,255,0.5); border: 2px solid #ffe3ec;">
            <div id="mesaj-ekrani" style="font-family: 'Dancing Script'; font-size: 2.8rem; color: #ff4d6d;">Seni Bekliyorum...</div>
            <div id="sayac" style="font-size: 6rem; font-family: 'Dancing Script'; color: #ff4d6d; display: none;"></div>
        </div>
        <button id="btn-baslat" class="devam-btn" style="display: none;" onclick="katmanDegistir(2)">Yolculuğa Başla ✨</button>
    </section>

    <section id="katman2" class="katman">
        <div class="mektup-kutu">
            <h2 style="font-family: 'Dancing Script'; font-size: 2.5rem; color: #ff4d6d; text-align: center; margin-bottom: 20px;">Canım Sevgilime... 💌</h2>
            <div class="mektup-metni">
                Merhaba şwmspwsm biraz heycan var kusura bakma aslında bu yazıyı çok önceden yazmıştım ama tamda hediyeni vereceğim zaman tartıştık olsun hayat işte her zaman mutlu olmuyoz hiç istemezdim doğum gününden önce tartışmak malesef oldu ama ne olursa olsun seni çok seviyorum bazen kırıyorum üzüyorum ne bilim bişiler oluyo ama ne kadar tartışsakda kavga etsekte sana olan aşkım sevgim güvenim hiç bir zaman bitmedi bitmicekte benim için o kadar kıymetlsinki kelimelere dökemem o kadar değişik, benim hakkımda düşüncelerini biliyorum insanlara olan sinirimi senden çıkarıyorum sinirlenince azarlıyorum ve daha fazlası aslında böyle yapmıyorum ama öyle anlaşılıyor seni suçlamıyorum hata bende , korkuyorum böyle bi an senin gözünden kalbinden bi anlık bile olsa çizik olmasını herşey için çok pişmanım, seni çok seviyorum be kızım 1 ay önceden başladım bu hediyeyi yapmaya bana gerçek aşkı sevgiyi güveni saf duyguyu yaşattın ne desem boş çok teşekkür ederimm bazen ne kadar salaklığım olsada beni üzmemek için yalnız kaldın yuttun hakkın ödenmez ama bu gün benim için milad oldu biliyormusun sanki bir yaşıma daha girmiş gibiyim sana söz veriyorum oturucam kendimi ölçücem herşeyi düşünücem sana karşı o eskş hatalarımı geri tekrarlamıcam buda sana İlhan sözü olsun seni çokmu çok seven adamın sözü senden ricam bana biras daha açık olman garip bir kişiliğim var biliyorum anlaması güç hala haraketlerim tavırlarım çocukca anlıyorum ama senden isteğim biras daha bana karşı açık olman, biliyormusun hayatımda ilk defa aşkı sevilmeyi yaşadım gerçek saf karşılıksız sevgiyi umarım bende sana yaşatabilmişimdir,İlk defa odamda bu kadar çok ağlıyorum bilmiyom normlade söylemem ama içimden geldi şqmspwms valla varya seni çok seviyorum be güzelim herşey için çok özür dilerim. 

                Saygılarımla seni deliler gibi seven İlhan...
            </div>
            <div style="text-align: center;">
                <button class="devam-btn" onclick="katmanDegistir(3)">30 Günlük Şiirlerim ❤️</button>
            </div>
        </div>
    </section>

    <section id="katman3" class="katman">
        <h2 style="font-family: 'Dancing Script'; font-size: 2.5rem; color: #ff4d6d; text-align: center;">Her Güne Bir Şiir ✨</h2>
        <div class="siir-grid" id="siir-grid"></div>
        <p style="text-align: center; color: #ff8fa3; padding-bottom: 40px;">Seni her gün daha çok seveceğim...</p>
    </section>

    <div id="modal" class="modal" onclick="modalKapat()">
        <div class="modal-icerik">
            <p id="modal-metin" style="font-size: 1.1rem; white-space: pre-line; line-height: 1.7; color: #444;"></p>
            <div style="margin-top: 20px; font-size: 1.5rem;">🌹</div>
        </div>
    </div>

    <script>
        const hitaplar = ["İYİ Kİ DOĞDUN PRENSESİM", "HAYATIMIN ANLAMI", "AŞK BAHÇEM", "YAVRUM", "CEYLAN GÖZLÜM"];
        const emojiler = ['💓','🍥','💖','🥰','🤩','🫶'];
        let yagmurBaslasin = false;

        // GİRİŞ SIRALAMASI
        window.onload = () => {
            const ekran = document.getElementById('mesaj-ekrani');
            let idx = 0;
            const interval = setInterval(() => {
                if(idx < hitaplar.length) {
                    ekran.style.opacity = 0;
                    setTimeout(() => {
                        ekran.innerText = hitaplar[idx];
                        ekran.style.opacity = 1;
                        idx++;
                    }, 400);
                } else {
                    clearInterval(interval);
                    setTimeout(geriSayimBaslat, 1000);
                }
            }, 1800);
        };

        function geriSayimBaslat() {
            document.getElementById('mesaj-ekrani').style.display = 'none';
            const sayac = document.getElementById('sayac');
            sayac.style.display = 'block';
            let s = 3;
            let timer = setInterval(() => {
                sayac.innerText = s;
                if(s <= 0) {
                    clearInterval(timer);
                    sayac.innerHTML = "İYİ Kİ DOĞDUN!<br><small style='font-size: 1.5rem'>Dünyama Hoş Geldin ❤️</small>";
                    confetti({ particleCount: 150, spread: 70, origin: { y: 0.6 } });
                    document.getElementById('btn-baslat').style.display = 'block';
                }
                s--;
            }, 1000);
        }

        // EMOJİ YAĞMURU FONKSİYONU
        function emojiYarat() {
            if(!yagmurBaslasin) return;
            const container = document.getElementById('emoji-layer');
            const e = document.createElement('div');
            e.className = 'emoji';
            e.innerText = emojiler[Math.floor(Math.random() * emojiler.length)];
            e.style.left = Math.random() * 100 + 'vw';
            e.style.animationDuration = (Math.random() * 2 + 3) + 's';
            e.style.opacity = Math.random() * 0.6 + 0.4;
            container.appendChild(e);
            setTimeout(() => e.remove(), 5000);
        }

        function katmanDegistir(n) {
            yagmurBaslasin = true;
            setInterval(emojiYarat, 300); // 300ms'de bir emoji düşer

            if(n === 2) {
                document.getElementById('katman1').style.transform = 'translateY(-100%)';
                document.getElementById('katman2').style.transform = 'translateY(0)';
            } else if(n === 3) {
                document.getElementById('katman2').style.transform = 'translateY(-100%)';
                document.getElementById('katman3').style.transform = 'translateY(0)';
                gridYap();
            }
        }

        const siirler = ["Gözlerin uzağımda, hayalin yanı başımda...","Haritada bir nokta, senin olduğun şehir...","Telefonun ekranı, tek pencerem sana...","Güneş seninle doğar, bende ise batıyor...","Mektuplar yazılmıyor, mesajlar çok hızlı...","Uçak kanatlarında, selam yolladım sana...","Aynı gökyüzü altındayız, bu yeter şimdilik...","Kilometreler saydım, bitmek bilmedi yollar...","Sesin bir ilaç gibi, kulaklarımda çınlar...","Bir kahve içerim ben, senin için burada...","Uykuya dalmadan evvel, resmine bakıyorum...","Bulutlar haber uçurur, belki benim yerime...","Gün saymak yorucuymuş, aylar geçmek bilmiyor...","Gülüşün bir video, izleyip durduğum her an...","Camın buğusuna ben, adını yazıyorum...","Uzaklık dediğin şey, bir rakamdan ibaret...","Yastığımda kokun yok, ama fikrimde varsın...","Yağmur yağar buralara, belki oraya da yağar...","Penceremden bakarım, geçtiğin yollar diye...","Bir gün aynı sofrada, ekmek bölüşeceğiz...","Aramızdaki o yol, çiçeklensin gelince...","Geceleri yıldızlara, anlatırım derdimi...","Gömleğinin bir teki, bende kaldı hatıra...","Şehirler arası otobüs, seni bana getirsin...","Gözden ırak olan yar, gönülden ırak olmaz...","Bana 'günaydın' yazman, günümü aydınlatır...","Hasretin rüzgarı sert, ama gemim sağlamdır...","Seni sevmek uzakken, bir ibadet gibidir...","Gözlerimi kapatsam, yanındayım aslında...","Bitti dörtlükler ama, bitmez sana bu sevdam..."];

        function gridYap() {
            const g = document.getElementById('siir-grid');
            if(g.children.length > 0) return;
            for(let i=1; i<=30; i++) {
                const k = document.createElement('div');
                k.className = 'kutucuk'; k.innerText = i;
                k.onclick = () => {
                    document.getElementById('modal-metin').innerText = siirler[i-1];
                    document.getElementById('modal').style.display = 'flex';
                };
                g.appendChild(k);
            }
        }
        function modalKapat() { document.getElementById('modal').style.display = 'none'; }
    </script>
</body>
</html>
