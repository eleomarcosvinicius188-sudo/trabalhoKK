# trabalhoKK
console.log("olá, Luiz! Seja bem vindo!");
console.log("olá,Gustavo! Seja bem vindo!");
console.log("olá, Cecilia! Seja bem vinda!");

function darBoasVindas(nome){
    console.log(`olá, ${nome}! seja bem vindo!`)
}

darBoasVindas("Luiz");
darBoasVindas("Gustavo");
darBoasVindas("Cecilia");


function apresentar(nome, idade){
    console.log(`meu nome é ${nome} e tenho ${idade} anos.`);

}

apresentar("Eleomarcos", 15)


// criar uma função que recebe o nome de uma pessoa e mostra uma mensagem dizendo que ela está estudando

function estudando(nome, Marcos){
    const estudar = (nome) => console.log(`${nome} está estudando.`);
estudar("Marcos");
}

function somar(a, b){
    return a + b;

}
somar ( 5, 3)

let resultado = somar( 5, 3);

console.log(resultado);

//crie uma função que apague dois valores e de a média deles se for acima de 6 é reprovado senão reprovado

/**
 * Função que calcula a média de duas notas e exibe se foi aprovado ou reprovado.
 * @param {number} nota1 - Primeira nota (0 a 10)
 * @param {number} nota2 - Segunda nota (0 a 10)
 */
function verificarMedia(nota1, nota2) {
    // Validação de tipo e faixa
    if (typeof nota1 !== 'number' || typeof nota2 !== 'number') {
        console.log("Erro: As notas devem ser números.");
        return;
    }
    if (nota1 < 0 || nota1 > 10 || nota2 < 0 || nota2 > 10) {
        console.log("Erro: As notas devem estar entre 0 e 10.");
        return;
    }

    const media = (nota1 + nota2) / 2;
    console.log(`Média: ${media.toFixed(2)}`);

    if (media > 6) {
        console.log("Resultado: Aprovado");
    } else {
        console.log("Resultado: Reprovado");
    }
}

// ===== Exemplo de uso =====
// No navegador, você pode usar prompt():
// const n1 = parseFloat(prompt("Digite a primeira nota:"));
// const n2 = parseFloat(prompt("Digite a segunda nota:"));
// verificarMedia(n1, n2);

// No Node.js, exemplo direto:
verificarMedia(7.5, 8.0); // Aprovado
verificarMedia(5.0, 6.0); // Reprovado
verificarMedia(11, 5);    // Erro de validação

function calcularMedia(nota1, nota2){
    return (nota1 + nota2) / 2;
}

let nome = prompt("digite o nome do aluno:");
 let nota1 = number(prompt("digite a primeira nota"));
let nota2 = number(prompt("digite a segunda nota:"));

let media1 = calcularMedia(nota1, nota2);

console.log(`${nome} ficou com media ${media1}`);

if (media1 >= 6){
    console.log(`${nome} está aprovado!`);
} else {
    console.log(`${nome} está reprovado!`);
}

calcularMedia(nota1, nota2)

// crie um progama que utilize uma função com vários parâmetros para calcular o custo total de uma viagem. o progama deverá receber os valores da passagem, hospedagem, alimentação e passeios, calcular o total e informar se a viagem está dentro do orçamento de r$ 2.000.00.

function calcularCusto(passagem, hospedagem, alimentacao, passeios) {
    return passagem + hospedagem + alimentacao + passeios;
}

let passagem = Number(prompt("Digite o valor da passagem: R$"));
let hospedagem = Number(prompt("Digite o valor da hospedagem: R$"));
let alimentacao = Number(prompt("Digite o valor da alimentação: R$"));
let passeios = Number(prompt("Digite o valor dos passeios: R$"));

let total = calcularCusto(passagem, hospedagem, alimentacao, passeios);

alert("Custo total da viagem: R$ " + total.toFixed(2));

if (total <= 2000) {
    alert("A viagem está dentro do orçamento de R$ 2.000,00!");
} else {
    alert("A viagem ultrapassou o orçamento de R$ 2.000,00.");
}

