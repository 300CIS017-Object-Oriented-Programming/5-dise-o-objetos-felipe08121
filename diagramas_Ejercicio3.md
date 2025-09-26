``` mermaid
classDiagram
    Usuario: + crearRepositorios()
    Usuario: - String nombre
    Usuario: - String correoElectronico
    Usuario: - Repositorio [] repositorios

    Usuario "Posee" o-- Repositorio

    class Repositorio{
         - String nombre
         - Commit [] historialDeCommits
         + agregarCommits( Usuario Autor )
    }
    
    Commit "Tiene Autor"--> Usuario
    Commit "Almacena" --o Repositorio
    class Commit{
        + String ID
        + String mensaje
        + date fechaCambio
        + Usuario autor
        + Archivo [ ] archivos
        + agregarAlStaggingarea( )
        
    }

    Archivo "Modifica" o-- Commit
    class Archivo{
        + string nombre
        + string contenido
    }
```