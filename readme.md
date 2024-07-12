# INTRODUCCIÓN

## CSS COMO LO HEMOS VENIDO USANDO
La forma más usada generando un archivo externo y lo llamamos mediante:
```html
<link rel="stylesheet" href="./style.css>
```

## DESVENTAJAS CSS PLANO

- lectura o ubicación de elementos muy complicado en proyectos muy grandes.
- Al generar varios css y llamarlos de manera individual resta performance y posicionamiento.
- No permite hacer escalable el CSS.
- No podemos automatizar y reutilizar.
- El trabajo no se puede hacer modular y dificulta el trabajo en equipo.

## QUÉ ES UN PROCESADOR

Un procesador CSS es una herramienta que escala las capacidades del CSS plano.

## VENTAJAS DE PROCESADOR

- Permite convertir un CSS plano a escalable.
- Mejoran la productividad y mantenimiento del código CSS.
- Estructurar CSS usando la modularidad.
- Reduce el tema de sobreescritura.
- Permite usar valores reutilizables.
- Administrar guías de estilos mediante variables.

## QUÉ ES SASS

Es un lenguaje que extiende las capacidades del CSS estándar, usa arquitectura y nomenclatura CSS. SASS usa un compilador. Es decir todo lo que escribamos en SASS se traducira en CSS para que el navegador lo interprete.

## VARIABLES
Contenedor que permite guardar valores que se pueden reutilizar en todo nuestro proyecto CSS.

```scss
        $color-titulo-principal: #3498db;
        
        h1 {
            color: $color-titulo-principal;
        }
```

## SCOPE

Se refiere al alcance o ámbito de una variable

 ```scss
        $color-subtitulos: #cd0606;

        h2 {
            color: $color-subtitulos;
        } 
        
        .color-sass {
            $color-subtitulos: #0f5920;
            color: $color-subtitulos;
        }
```


## ANIDAMIENTO

Nos permite escribir CSS de forma estructurada y con jerarquía estableciendo un mejor entendimiento de la relación de padre e hijo entre selectores mediante el anidado (uno dentro de otro).

 ```scss
        p {
            b {
                color: blue;
            }
        }
  ```  

## AMPERSAN PADRE

El uso de & en SASS se usa para referirse al selector padre dentro de un anidamiento de manera eficiente y mantener el código CSS más organizado y fácil de entender.

 ```scss
         .boton {
            background-color: #9927c2;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 4px;
            transition: background-color 0.3s ease;
          
            &:hover {
              background-color: #2941b9;
            }
          }
 ```  

## IMPORT

Se usa para dividir (modular) css en varios archivos (parches) pero como al final se compilará sólo uno debe anteponerse a los archivos parches el "_", estos serán llamados al archivo principal mediante @import

 ```scss
Este archivo parche será llamado mediante import en index.html : @import 'maindata';
```
