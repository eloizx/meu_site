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
