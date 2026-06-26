<oiiiiii>
<html>
<head>
    <title>Calculadora com Alert</title>
</head>
<body>

<button onclick="calcular()">Abrir Calculadora</button>

<script>
function calcular() {

    let n1 = Number(prompt("Que comecem os jogos! Escolha o primeiro número:"));
    let n2 = Number(prompt("Escolha o segundo número:"));

    let op = prompt(
        "Escolha a operação:\n" +
        "+ para somar\n" +
        "- para subtrair\n" +
        "* para multiplicar\n" +
        "/ para dividir"
    );

    let resultado;

    if (op == "+") {
        resultado = n1 + n2;
    } else if (op == "-") {
        resultado = n1 - n2;
    } else if (op == "*") {
        resultado = n1 * n2;
    } else if (op == "/") {
        if (n2 == 0) {
            alert("Erro: não é possível dividir por 0.");
            return;
        }
        resultado = n1 / n2;
    } else {
        alert("Operação inválida!");
        return;
    }

    alert("O resultado é: " + resultado);
}
</script>

</body>
</html>
