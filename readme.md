

# Documentación del comando Scaffold-DbContext 

## Database First

El comando `Scaffold-DbContext` en Entity Framework Core se utiliza para generar clases de modelo basadas en una base de datos existente. Esto es útil cuando se está trabajando con una base de datos existente y se desea generar automáticamente las clases de modelo correspondientes en un proyecto de .NET.

## Uso Básico:

```bash
Scaffold-DbContext "Server=<Servidor>;Database=<NombreBaseDatos>;User Id=<Usuario>;Password=<Contraseña>;TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir <DirectorioSalida>
```

- `Server`: La dirección del servidor de la base de datos.
- `Database`: El nombre de la base de datos.
- `User Id`: El ID de usuario para acceder a la base de datos.
- `Password`: La contraseña para acceder a la base de datos.
- `TrustServerCertificate` : Indica si se debe confiar en el certificado del servidor.


### Argumentos Adicionales:

- `OutputDir`: Especifica el directorio donde se generará el código de las clases de modelo.
- `force`: Opcional. Utilizado para actualizar las clases de modelo si la estructura de la base de datos ha cambiado.

```bash
Scaffold-DbContext "Server=localhost;Database=BaseDatos;User Id=sa;Password=1234;TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models -force
```

### Notas Importantes:

- Asegúrate de tener los permisos necesarios para acceder a la base de datos especificada.
- Reemplaza los valores `<Servidor>`, `<NombreBaseDatos>`, `<Usuario>`, `<Contraseña>` con los valores correspondientes de tu entorno.


### Referencia:
- Documentación oficial de Entity Framework Core: [Entity Framework Core](https://docs.microsoft.com/es-es/ef/core/cli/dotnet#scaffold-dbcontext)
