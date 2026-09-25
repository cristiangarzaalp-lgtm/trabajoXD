[6.1-objetos.js](https://github.com/user-attachments/files/32634175/6.1-objetos.js)
//datos y metodos de un obj
//fecha de menu
//los datos son distintos a proposito. compara la FORMA, no el contenido
const producto = {
    id: "p-07",
    nombre:"agua de jamaica",
    precio: 15,
    categoria: "bebida",
    disponible:true,

    //metodos
    resumen(){
        return this.nombre + " - $ " + this.precio + "(" + this.categoria + ")"
    },

    estaDisponible(){
        return this.disponible;
    }
};


console.log("paso 1 - imprimiendo el producto");
console.log(producto);

//paso 2 - tres formas de leer
console.log("paso 2")
const campo = "nombre"
console.log(producto.nombre);
console.log(producto["nombre"]);
console.log(producto[campo]);


console.log("paso 3");
console.log(producto.resumen());
console.log(producto.estaDisponible());

//paso 4 el usuario
const usuario = {
    id:"u-03",
    nombre:"pancho",
    correo:"pancho@cbtis.edu.mx",
    telefono:6767676767,
    rol:"alumno"
};


//paso 5
const pedido = {
    folio:"PR-0118",
    cliente: usuario,
    producto: producto,
    cantidad: 3,
    estado:"pendiente"
}


console.log("paso 5");
console.log(pedido.cliente.nombre);
console.log(pedido.producto.precio);
console.log(pedido.cliente.telefono);


//paso 6 destructuracion
console.log("paso 6");
const {nombre, precio} = producto;
console.log(nombre, precio);

const {cantidad, nota = "sin nota"} = pedido;
console.log(cantidad, nota);
console.log("cristian garza soy programador causa")
