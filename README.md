# ansaml.karlygash
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Поздравление</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            overflow: hidden;
        }
        .container {
            text-align: center;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            animation: fadeIn 1s ease-in-out;
        }
        h2 {
            margin-bottom: 15px;
            color: #333;
        }
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 100%;
            padding: 10px;
            background: #ff6b81;
            border: none;
            color: white;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }
        button:hover {
            background: #ff4757;
        }
        .error {
            color: red;
            margin-top: 10px;
            display: none;
        }
        .video-container {
            display: none;
            text-align: center;
            animation: fadeIn 1s ease-in-out;
        }
        video {
            width: 100%;
            max-width: 600px;
            border-radius: 10px;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="container" id="login-container">
    <h2>Введите логин и пароль</h2>
    <input type="text" id="login" placeholder="Логин">
    <input type="password" id="password" placeholder="Пароль">
    <button onclick="checkLogin()">Войти</button>
    <p class="error" id="error-message">Неверный логин или пароль</p>
</div>

<div class="video-container" id="video-container">
    <h2>Поздравление для тебя!</h2>
    <video id="video" controls></video>
</div>

<script>
    const users = {
        "aurora": "qwerty123",
        "milena": "love456",
        "darya1": "star789",
        "sonya": "moon321",
        "miruet": "happy987",
        "darya2": "cool654",
        "milana": "dance852",
        "viktoria": "queen741",
        "alisa": "magic369",
        "anya": "bright159",
        "dina": "lucky258",
        "zlata": "shine753",
        "angelina": "sweet951",
        "bekzat": "strong147",
        "enesa": "dream753",
        "danara": "hero852",
        "veronika": "charm369",
        "lena": "smart456"
    };

    function checkLogin() {
        let login = document.getElementById("login").value.toLowerCase();
        let password = document.getElementById("password").value;
        let errorMessage = document.getElementById("error-message");

        if (users[login] === password) {
            document.getElementById("login-container").style.display = "none";
            document.getElementById("video-container").style.display = "block";
            document.getElementById("video").src = `videos/${login}.mp4`;
        } else {
            errorMessage.style.display = "block";
        }
    }
</script>

</body>
</html>
