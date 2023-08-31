class Veiculo{
    longitude: number;
    latitude: number;

    constructor(longitude:number,latitude:number){
        this.longitude = longitude;
        this.latitude = latitude;
    }
    print(): void {
        console.log(`Esta é a longitude: ${this.longitude} e a latitude: ${this.latitude}`);
      }
}
class Eletrico extends Veiculo{
    bateria: number;
    constructor(bateria:number, longitude: number, latitude: number){
        super(longitude, latitude);
        this.bateria = bateria;
    }
    print(): void {
        console.log(`Esta é a porcentagem da bateria: ${this.bateria} e a longitude: ${this.longitude} e a latitude: ${this.latitude}`);
      }
}
class Voador extends Eletrico{
    vertical: number;
    constructor(vertical:number,bateria:number, longitude: number, latitude: number){
        super(bateria,longitude, latitude);
        this.vertical = vertical;
    }
    print(): void {
        console.log(`Esta é a posição vertical: ${this.vertical} , porcentagem de bateria ${this.bateria} e a longitude: ${this.longitude} e a latitude: ${this.latitude}`);
      }
}
export {Veiculo, Eletrico, Voador}

//

import { Veiculo, Eletrico, Voador } from "./ex2_7_MODEL_ARSC";

const veiculo = new Voador(100,100, 500 ,200);
console.log("Exemplo de veiculo eletrico e voador");
veiculo.print();
