```markdown
# String.Utils — Librería de utilidad para operaciones con cadenas

## Descripción

**String.Utils** es una librería de clases en .NET 8 diseñada como ejercicio práctico para comprender el proceso de creación, empaquetado y gestión de paquetes NuGet.

El objetivo de este proyecto es servir como base para estudiar cómo construir una biblioteca reutilizable, empaquetarla correctamente y preparar su publicación y consumo mediante NuGet.

---

## Estructura del proyecto

```text
String.Utils/
├── LICENSE
├── README.md
├── String.Utils.sln
├── String.Utils.csproj
├── StringUtil.cs
├── bin/
│   ├── Debug/
│   │   └── net8.0/
│   └── Release/
│       ├── String.Utils.1.0.0.nupkg
│       ├── String.Utils.1.0.1.nupkg
│       └── net8.0/
├── obj/
│   ├── Debug/
│   └── Release/

## Implementación actual

```csharp
namespace String.Utils;

public class StringUtil
{
    public string Plus(string param1, string param2)
    {
        return $"param1 + param2";
    }
}

**Nota:** Actualmente el método `Plus` retorna el string literal `"param1 + param2"`, sin realizar la concatenación real. Este comportamiento se mantuvo intencionalmente como parte del ejercicio.

---

## Uso del proyecto

### Compilación

```bash
dotnet build -c Release
### Empaquetado NuGet

```bash
dotnet pack -c Release
El paquete NuGet resultante (`.nupkg`) se genera en el directorio `bin/Release/`.

---

## Objetivos del repositorio

- Practicar la creación de proyectos classlib en .NET.
- Comprender cómo empaquetar librerías como paquetes NuGet.
- Observar y entender la estructura generada por MSBuild y NuGet.
- Preparar el terreno para una posible publicación en NuGet.org.

---

## Futuras mejoras

- Corregir la lógica del método `Plus` para realizar una concatenación efectiva.
- Incorporar pruebas unitarias.
- Documentar la API pública de la librería.
- Configurar una pipeline de CI para automatizar el empaquetado.

---

## Licencia

Este proyecto está licenciado bajo los términos de la licencia MIT. Consulta el archivo [`LICENSE`](LICENSE) para más detalles.