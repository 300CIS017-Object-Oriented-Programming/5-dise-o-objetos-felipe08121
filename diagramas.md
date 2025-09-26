``` mermaid
classDiagram
    Sistema: - Libro [ ] libros
    Sistema: - Usuario [ ] usuarios
    Sistema: - Prestamo [ ] prestamos
    Sistema: + Registrarlibro()
    
    Sistema: + mostrarListaLibros()
    Sistema: + consultarPrestamosUsuarios()


    Sistema o--  Usuario : gestiona
    Sistema o-- Libro : gestiona
    Sistema o--  Prestamo : gestiona

    class Usuario{
        - String nombre
        - int ID 
        - Prestamo [ ] prestamos
    }

    
    Usuario "tiene" o--> Prestamo
    Libro "Tiene"--> Prestamo


    class Libro{
         - String titulo
         - String autor
         - String genero
         - String estado
         - int ID
    }
    
    class Prestamo{
        - date fecha inicio
        - date fecha devolucion
        - String estado
        - Usuario usuario
        - Libro libro
        + registrarPrestamo( )
        + registrarDevolucion()
    }
```