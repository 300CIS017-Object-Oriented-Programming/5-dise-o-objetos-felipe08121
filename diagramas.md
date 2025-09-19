``` mermaid
classDiagram
    Sistema: - Libro [ ] libros
    Sistema: - Usuario [ ] usuarios
    Sistema: + Registrarlibro()
    
    Sistema: + mostrarListaLibros()
    Sistema: + consultarPrestamosUsuarios()
    Sistema "Tiene"o--> Libro
    Sistema "Tiene"o--> Usuario
    Sistema "Tiene"o--> Prestamo

    class Usuario{
        - String nombre
        - int ID 
        - Libro [ ] libros

    }

    
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
        + registrarPrestamo( )
        + registrarDevolucion()
    }
```