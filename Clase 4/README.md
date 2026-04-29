# Clase 4

## Pasos para crear un proyecto web (en esta materia)

[Ir al código](https://github.com/lautaro-rojas/Desarrollo-y-arquitecturas-web/tree/main/Clase%204/rojas2)

### En visual studio 2022 (pc de la facultad)

Buscar la plantilla que se llama "Sitio de ASP.NET web forms".

### En visual studio 2026

Buscar la plantilla que se llama "Aplicación web ASP.NET (.NET Framework)".

![PlantillaVS2026](../images/PlantillaVS2026.png)

Lo importante es que debe tener la siguiete estructura y tener el archivo que se llama `Default.aspx`.

![EstructuraProy](../images/EstructuraProy.png)

## Ejercicio durante la clase

1. Levantar el proyecto
2. Ejecutar el proyecto

   > [!NOTE]
   > El error del roslyn se soluciona ejecutando el siguente comando en la "Consola del administrador de paquetes":
   >
   > ```Bash
   >Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r
   > ```

3. Crear un formulario web aspx que se llame `Respuesta.aspx`.

   1. Click derecho en el "mundito" de la solución.

      ![Mundito](../images/Mundito.png)

   2. Agregear -> Agregar nevo elemento -> Formulario Web Forms.

      ![FormularioWebForms](../images/FormularioWebForms.png)

4. Ingresar el valor de Usuario y Comentarios al objeto `Session`.

   1. `Session["Usuario"]`
   2. `Session["Comentario"]`

      [Ir al código](https://github.com/lautaro-rojas/Desarrollo-y-arquitecturas-web/blob/main/Clase%204/rojas2/rojas2/Default.aspx.cs)

5. Una vez ingresados estos datos redirigir a `Respuesta.aspx` y mostrar los datos ingresados.

   Se puede redirigir con `Response.Redirect("NombreArchivo");`

## Controles de verificación

Los controles de verificación se suelen colocar al lado de la herramienta que quiero controlar. Estos se encuentran en el "Cuadro de herramientas", el mismo lugar donde buscamos los `Button`, `TextBox`, `Label`...

### RequiredFieldValidator

Este control hace que otro sea requerido. No puede quedar vacío.

![RequiredValidator](../images/RequiredValidator.png)

No olvidarse de llenar la propiedad `ControlToValidate` con una herramienta.

### RangeValidator

Este control verifica un rango de datos, normalemnte se usa para controlar la edad.

![RangeValidator](../images/RangeValidator.png)

No olvidarse de llenar las propiedades:

- `ControlToValidate` con un control/herramienta.
- `MaximumValue` con el valor entero máximo.
- `MinimumValue` con el valor entero mínimo.
- `Type` con el tipo de dato `Integer`.

## Típico enunciado de parcial

> [!WARNING]
> Este ejercicio se entrega --> **Ejercicio ya entregado por correo durante la clase**
>
> - Hacer screenshot de la parte del cliente
> - Hacer screenshot de la parte del servidor
>
> santiago.sabato@uai.edu.ar
>
> [Ir al código - EjercicioClase4](https://github.com/lautaro-rojas/Desarrollo-y-arquitecturas-web/tree/main/Clase%204/EjercicioClase4)

Se necesita saber el efuerzo de un proyecto de desarrollo de sofware a través de la función de PUTNAM.

$$L = C_k * K^{1/3} * td^{4/3}$$

El despeje de esta ecuación quedaría:

$$K = \frac{L^{3}}{(C_k^{3} * td^{4})}$$

Ingresar por cliente:

- L = 33000 (líneas de código)
- Ck = 11000 (constante tecnológica de desarrollo) -- **Rrange validator Ck no puede ser > a 11000**
- td = 2 (duración del proyecto en años)

Mostrar en un form:

- El valor de K.

La ecuación en C# sería:

```CSharp
double K = Math.Pow(L, 3) / (Math.Pow(Ck, 3) * Math.Pow(td, 4));
```

[Ir al código](https://github.com/lautaro-rojas/Desarrollo-y-arquitecturas-web/blob/main/Clase%204/EjercicioClase4/EjercicioClase4/Respuesta.aspx.cs)

## Para la semana que viene

- Traer apuntes porque vamos a hacer un simulacro de parcial.
- Estudiar un poco.
- El parcial puede contener un ejercicio práctico de 45 minutos.

### Preguntas de parcial

- Diferencias entre Get y Post
- ¿Cuál es el problema de estado?
