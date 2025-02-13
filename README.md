<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Pequeno Site</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Meu Pequeno Site</h1>
        <nav>
            <ul>
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="sobre">
            <h2>Sobre Mim</h2>
            <p>Olá! Este é um pequeno site criado para demonstrar como fazer um site funcional.</p>
        </section>

        <section id="contato">
            <h2>Entre em Contato</h2>
            <form id="contact-form">
                <label for="nome">Nome:</label>
                <input type="text" id="nome" name="nome" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="mensagem">Mensagem:</label>
                <textarea id="mensagem" name="mensagem" required></textarea>

                <button type="submit">Enviar</button>
            </form>
            <p id="mensagem-enviada" style="display: none; color: green;">Mensagem enviada com sucesso!</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 Meu Pequeno Site</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* styles.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

header h1 {
    margin: 0;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

main {
    padding: 20px;
}

section {
    background-color: white;
    padding: 20px;
    margin: 20px;
    border-radius: 5px;
}

form label {
    display: block;
    margin-top: 10px;
}

form input, form textarea, form button {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

form button {
    background-color: #333;
    color: white;
    border: none;
    cursor: pointer;
}

form button:hover {
    background-color: #555;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: white;
}
// script.js
document.getElementById('contact-form').addEventListener('submit', function(event) {
    event.preventDefault(); // Impede o envio do formulário

    const nome = document.getElementById('nome').value;
    const email = document.getElementById('email').value;
    const mensagem = document.getElementById('mensagem').value;

    if (nome && email && mensagem) {
        // Exibe a mensagem de sucesso
        document.getElementById('mensagem-enviada').style.display = 'block';

        // Limpa o formulário após 3 segundos
        setTimeout(() => {
            document.getElementById('contact-form').reset();
            document.getElementById('mensagem-enviada').style.display = 'none';
        }, 3000);
    } else {
        alert('Por favor, preencha todos os campos.');
    }
});
