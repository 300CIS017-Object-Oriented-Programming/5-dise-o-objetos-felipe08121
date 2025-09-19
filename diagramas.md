...
classDiagram
    Sistema: - Libro [ ] libros
    Sistema: - Usuario [ ] usuarios
    Sistema: + Registrarlibro()
    
    Sistema: + MostrarListaLibros()
    Sistema: + ConsultarPrestamosUsuarios()
    Sistema "Tiene"o--> Libro
    Sistema "Tiene"o--> Usuario


    class Usuario{
        - String nombre
        - int ID 
        - Libro [ ] libros

    }

    Usuario "tiene"o--> Libro
    Usuario "tiene" o--> Prestamo
    Libro "Tiene"--> Usuario
    class Libro{
         - String titulo
         - String Autor
         - String Genero
         - int ID
         - Usuario usuario
    }
    
    class Prestamo{
        - date fecha inicio
        - date fecha devolucion
        - string estado
        + RegistrarPrestamo( )
        + RegistrarDevolucion()
    }
...