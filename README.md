<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz sobre Inteligência Artificial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .question {
            margin-bottom: 20px;
        }
        .question h2 {
            font-size: 1.2em;
        }
        .answers label {
            display: block;
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <h1>Quiz sobre Inteligência Artificial</h1>
    
    <div class="question">
        <h2>1. O que é Inteligência Artificial?</h2>
        <div class="answers">
            <label><input type="radio" name="q1" value="a"> A) Um tipo de software que apenas armazena dados.</label>
            <label><input type="radio" name="q1" value="b"> B) A capacidade de uma máquina realizar tarefas que normalmente exigiriam inteligência humana.</label>
            <label><input type="radio" name="q1" value="c"> C) Um sistema que só funciona com comandos pré-programados.</label>
        </div>
    </div>

    <div class="question">
        <h2>2. Qual é um exemplo de aplicação de IA?</h2>
        <div class="answers">
            <label><input type="radio" name="q2" value="a"> A) Diagnóstico médico avançado.</label>
            <label><input type="radio" name="q2" value="b"> B) Escrever em um caderno.</label>
            <label><input type="radio" name="q2" value="c"> C) Pintar uma parede.</label>
        </div>
    </div>

    <div class="question">
        <h2>3. Qual é um dos principais desafios da IA?</h2>
        <div class="answers">
            <label><input type="radio" name="q3" value="a"> A) Aumentar a capacidade de armazenamento de dados.</label>
            <label><input type="radio" name="q3" value="b"> B) Reduzir o consumo de energia dos computadores.</label>
            <label><input type="radio" name="q3" value="c"> C) Garantir que os algoritmos não sejam tendenciosos.</label>
        </div>
    </div>

    <button onclick="checkAnswers()">Verificar Respostas</button>

    <script>
        function checkAnswers() {
            const correctAnswers = {
                q1: 'b',
                q2: 'a',
                q3: 'c'
            };

            let score = 0;
            for (const [question, answer] of Object.entries(correctAnswers)) {
                const selected = document.querySelector(`input[name="${question}"]:checked`);
                if (selected && selected.value === answer) {
                    score++;
                }
            }

            alert(`Você acertou ${score} de 3 perguntas.`);
        }
    </script>
</body>
</html>

