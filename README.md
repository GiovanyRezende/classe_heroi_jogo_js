# Criando a Classe para um Jogo
Esse é um projeto de JavaScript proposto pela [DIO](https://www.dio.me/). Se trata de um simples algoritmo na criação de uma classe para jogo em JavaScript. O objetivo é exerciar a lógica de programação.

## O que devia ser utilizado

- Variáveis;
- Operadores;
- Estruturas de decisões;
- Classes e Métodos

# O código
```
class Hero{
    constructor(nome,idade,tipo){
        this.nome = nome;
        this.idade = idade;
        
        const tiposValidos = {"guerreiro": 0, "mago": 1, "monge": 2, "ninja": 3};
        
        if (tipo in tiposValidos) {
            this.tipo = tipo;
        } else {
            this.tipo = "guerreiro";
        }
    }
    atacar(){
        let ataque;
        switch(this.tipo){
            case "guerreiro":
                ataque = "espada";
                break;
            case "mago":
                ataque = "magia";
                break;
            case "monge":
                ataque = "artes marciais";
                break;
            case "ninja":
                ataque = "shuriken";
                break;
            default:
                ataque = "poder oculto";
                break;
        }
        console.log(`o ${this.tipo} atacou usando ${ataque}`);
    }
}

guerreiro = new Hero("Golem",580,"guerreiro");
console.log(guerreiro.nome);
console.log(guerreiro.idade);
console.log(guerreiro.tipo);
guerreiro.atacar();

console.log("--------------------------------")

ninja = new Hero("Shozen",47,"ninja");
ninja.atacar();
```
