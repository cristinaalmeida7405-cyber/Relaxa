<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site Gigante</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }
        body {
            background-color: #0f172a;
            color: #f8fafc;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        header {
            background-color: #1e293b;
            padding: 20px;
            text-align: center;
            border-bottom: 2px solid #334155;
        }
        header h1 {
            color: #38bdf8;
            font-size: 1.8rem;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #1e293b;
            padding: 10px;
            gap: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
        }
        nav button {
            background-color: #334155;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 1rem;
            transition: background 0.3s;
        }
        nav button:hover, nav button.active {
            background-color: #38bdf8;
            color: #0f172a;
            font-weight: bold;
        }
        main {
            flex: 1;
            padding: 20px;
            max-width: 800px;
            margin: 0 auto;
            width: 100%;
        }
        .tab-content {
            display: none;
            background-color: #1e293b;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.5);
            animation: fadeIn 0.5s ease-in-out;
        }
        .tab-content.active {
            display: block;
        }
        h2 {
            color: #38bdf8;
            margin-bottom: 15px;
        }
        p {
            line-height: 1.6;
            color: #cbd5e1;
            margin-bottom: 10px;
        }
        footer {
            text-align: center;
            padding: 15px;
            background-color: #1e293b;
            color: #64748b;
            font-size: 0.9rem;
            border-top: 2px solid #334155;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <header>
        <h1>🚀 O Meu Espaço Digital</h1>
    </header>

    <nav>
        <button onclick="mudarAba('inicio')" id="btn-inicio" class="active">Início</button>
        <button onclick="mudarAba('projetos')" id="btn-projetos">Projetos</button>
        <button onclick="mudarAba('sobre')" id="btn-sobre">Sobre</button>
    </nav>

    <main>
        <section id="inicio" class="tab-content active">
            <h2>Bem-vindo à Página Principal</h2>
            <p>Este é um site de teste robusto, construído inteiramente do zero, direto no telemóvel e sem enrolação.</p>
            <p>Usa os botões no topo para alternar entre as abas e ver como a estrutura reage de forma fluida.</p>
        </section>

        <section id="projetos" class="tab-content">
            <h2>Meus Trabalhos & Ideias</h2>
            <p>🔹 <strong>Repositório Relaxa:</strong> O começo de tudo, focado em autonomia e código limpo.</p>
            <p>🔹 <strong>Prototipagem Web:</strong> Experiências rápidas em HTML, CSS e JavaScript puro.</p>
        </section>

        <section id="sobre" class="tab-content">
            <h2>Sobre Mim</h2>
            <p>Focado em aprender a programar na prática, dominando as ferramentas reais da internet sem depender de frameworks complexos ou funis corporativos.</p>
            <p>Liberdade criativa em primeiro lugar.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 - Criado com autonomia total.</p>
    </footer>

    <script>
        function mudarAba(idAba) {
            // Esconde todas as abas
            const abas = document.querySelectorAll('.tab-content');
            abas.forEach(aba => aba.classList.remove('active'));

            // Remove a classe active de todos os botões
            const botoes = document.querySelectorAll('nav button');
            botoes.forEach(botao => botao.classList.remove('active'));

            // Mostra a aba escolhida e ativa o botão correspondente
            document.getElementById(idAba).classList.add('active');
            document.getElementById('btn-' + idAba).classList.add('active');
        }
    </script>

</body>
</html>

