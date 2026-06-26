# <!DOCTYPE html>
<html>
<head>
    <title>Calculadora com Alert</title>
</head>
<body>

<button onclick="calcular()">Abrir Calculadora</button>

<script>
function calcular() {
    let n1 = Number(prompt(@"Que começem os jogos, escolha o primeiro número:"));
    let n2 = Number(prompt(@"escolha o segundo:"));

    let op = prompt(
        "Escolha o números que deseja operacioar:\n" +
        "+ para somar\n" +
        "- para subtrair\n" +
        "* para multiplicar\n" +
        "/para dividir" 
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
            alert("Erro: não é possivel dividir por 0");
            return;
        }
        resultado = n1 / n2;
    } else {
        alert("Operação inválida!");
        return;
    }

    alert("o resultado é : " + resultado);
}
</script>

</body>
</html>
