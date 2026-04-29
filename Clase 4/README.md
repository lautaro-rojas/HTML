# Clase 4

## Pasos para crear un proyecto web (en esta materia)

1. Abrir visual studio 2022.
2. Buscar la plantilla que se llama "Sitio de ASP.NET web forms".

## Ejercicio durante la clase

1. Levantar el proyecto
2. Ejecutar el proyecto

    Nota: Error del roslyn se soluciona ejecutando el siguente comando en la "Consola del administrador de paquetes" el siguente comando:

    ```Bash
    Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r
    ```

3. Crear un formulario web aspx que se llame `Respuesta.aspx`.
   1. Click derecho en el "mundito" de la solución.
   2. Agregear -> Agregar nevo elemento -> Formulario Web Forms.

4. Ingresar el valor de Usuario y Comenrarios al objeto `Session`.
   1. `Session["Usuario"]`
   2. `Session["Comentario"]`

5. Una vez ingresados estos datos redirigir a `Respuesta.aspx` y mostrar los datos ingresados.

## Controles de verificación

Los controles de verificación se suelen colocar al lado de la herramienta que quiero controlar.

### RequiredFieldValidator

Este control hace que otro sea requerido. No puede quedar vacío.

No olvidarse de llenar la propiedad `ControlToValidate` con un control/herramienta.

### RangeValidator

Este control verifica un rango de datos, normalemnte se usa para controlar la edad.

No olvidarse de llenar las propiedades:

- `ControlToValidate` con un control/herramienta.
- `MaximumValue` con el valor entero máximo.
- `MinimumValue` con el valor entero mínimo.
- `Type` con el tipo de dato `Integer`.

## Típico enunciado de parcial

> [!WARNING]
> Este ejercicio se entrega.
> 
> - Hacer screenshot de la parte del cliente
> - Hacer screenshot de la parte del servidor
> 
> santiago.sabato@uai.edu.ar

Se necesita saber el efuerxo de un proyecto de desarrollo de sofware a través de la función de PUTNAM

L + Ck * Kˆ1/3 tdˆ4/3

El despeje de esta ecuación quedaría:

K = Lˆ3 / (Ckˆ3 * tdˆ4)

Ingresar por cliente:

- L = 33000 (líneas de código)
- Ck = 11000 (constante tecnológica de desarrollo) -- Poner un range validator Ck no puede ser > a 11000
- td = 2 (duración del proyecto en años)

Mostrar en un form:

- El valor de K.

La ecuación en C# sería:

```CSharp
double K = Math.Pow(L, 3) / (Math.Pow(Ck, 3) * Math.Pow(td, 4));
```

semana que viene traer apuntes porque vamos a hacer un simulacro. Ejercicio practico de 45 minutos

diferencia entre get y post

probelma de estado, cual es?
