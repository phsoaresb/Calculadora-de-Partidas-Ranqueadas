const readline = require('readline');
// IMPORTA UMA BIBLIOTECA QUE PERMITE INTERAÇÃO COM USUÁRIO

const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

function Nivel(vitorias, derrotas) {
    const saldoVitorias = vitorias - derrotas;
    let nivel;

    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 10 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Imortal";
    }

    return { saldoVitorias, nivel };
}

function main() {
    rl.question("Digite o número de vitórias: ", (vitoriasInput) => {
        const vitorias = parseInt(vitoriasInput, 10);

        rl.question("Digite o número de derrotas: ", (derrotasInput) => {
            const derrotas = parseInt(derrotasInput, 10);

            const { saldoVitorias, nivel } = Nivel(vitorias, derrotas);
            console.log(`O Herói tem de saldo de ${saldoVitorias} e está no nível de ${nivel}`);

            rl.close();
        });
    });
}

// Executa o programa
main();
