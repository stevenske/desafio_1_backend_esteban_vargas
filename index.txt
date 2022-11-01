class Usuario{
    constructor(nombre,apellido,libros = [],mascotas = []){
        this.nombre = nombre;
        this.apellido = apellido;
        this.libros = libros;
        this.mascotas = mascotas
    }
    getFullName(){
        return `${this.nombre} ${this.apellido}`
    }

    addMascota(mascota){
        this.mascotas.push(mascota);
    }
    countMascotas(){
        let mascotasTotal = this.mascotas.length;
        return mascotasTotal;
    }
    addBook(nombre,autor){
        this.libros.push({nombre:nombre, autor:autor});
    }
    getBookNames(){
        const libroNombre = this.libros.map(libros => libros.nombre)
        return libroNombre
    }
}

let usuario = new Usuario('Esteban','Vargas',[{nombre:'El camino de los reyes', autor:'Brandon Sanderson'}],['conejo'])
usuario.addMascota('perro')
usuario.addMascota('gato')
usuario.addBook('Juramentada','Brandon Sanderson')
usuario.addBook('Palabras Radiantes','Brandon Sanderson')
console.log(usuario.getFullName());
console.log(usuario.countMascotas());
console.log(usuario.getBookNames());