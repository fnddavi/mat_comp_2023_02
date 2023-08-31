2.6. Utilizando linguagem de programação defina: 

a)	Uma enumeração para os meses do ano. 
const Meses = {
    JANEIRO: 1,
    FEVEREIRO: 2,
    MARCO: 3,
    ABRIL: 4,
    MAIO: 5,
    JUNHO: 6,
    JULHO: 7,
    AGOSTO: 8,
    SETEMBRO: 9,
    OUTUBRO: 10,
    NOVEMBRO: 11,
    DEZEMBRO: 12
};

b)	Uma enumeração para os dias da semana. 
const DiaSemana = {
    DOMINGO: 0,
    SEGUNDA_FEIRA: 1,
    TERCA_FEIRA: 2,
    QUARTA_FEIRA: 3,
    QUINTA_FEIRA: 4,
    SEXTA_FEIRA: 5,
    SABADO: 6
};

c)	Uma função recursiva para o cálculo do fatorial de um número. 
function fatorial_fdf (nro: number): number {
    if (nro === 0) {
        return 1;
    } 
    else {
        return nro * fatorial_fdf (nro - 1);
    }
}

d)	Uma definição que corresponda a definição do tipo gênero-diferença para um uma pessoa que estude em uma faculdade. Utilize uma linguagem que dê suporte a herança.

class Pessoa_fdf { 
  nome: string; 
  idade: number; 
  genero: string; 
 
  constructor(nome: string, idade: number, genero: string) { 
      this.nome = nome; 
      this.idade = idade; 
      this.genero = genero; 
  } 
  estudar() { 
      console.log(`${this.nome} está estudando.`); 
  } 
} 
class Estudante extends Pessoa_fdf { 
  matricula: number; 
  curso: string; 

  constructor(nome: string, idade: number, genero: string, matricula: number, curso: string) { 
      super(nome, idade, genero); 
      this.matricula = matricula; 
      this.curso = curso; 
  } 
  apresentar() { 
      console.log(`Nome: ${this.nome}, Idade: ${this.idade}, Gênero: ${this.genero}, Matrícula: ${this.matricula}, Curso: ${this.curso}`); 
  } 
}

const estudante_fdf = new Estudante("Fernando", 34, "Masc", 987654, "Desenvolvimento de Software Multiplataforma"); 
estudante_fdf.estudar();  
estudante_fdf.apresentar();

