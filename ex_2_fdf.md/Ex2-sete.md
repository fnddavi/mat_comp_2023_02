[20:52] ABNER RODRIGO DA SILVA COSTA

// 2.7. Um veículo possui a capacidade de se mover, expressa pela alteração na sua coordenada de longitude e latitude. Um veículo elétrico é um veículo que possui como fonte de energia primária a eletricidade (armazenada em uma bateria). Um veículo elétrico e voador é um veículo que também possui a capacidade de se mover na vertical, expressa pela alteração de sua altitude em relação ao solo. Represente um veículo elétrico e voador utilizando uma cadeia de herança. Defina o código-fonte representativo do modelo em um arquivo separado daquele que faz uso desse e, adicionalmente exemplifique o acesso e a modificação desses atributos através de chamada de suas operações.  

 

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
