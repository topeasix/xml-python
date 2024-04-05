# XML

[Web](https://www.w3schools.com/xml/xml_whatis.asp)

## Introduccion

XML, o *Extensible Markup Language*, es un lenguaje que permite almacenar datos en un formato legible, estructurado y autodescriptivo. Permite la gestion y estructuracion de documentos de todo tipo de tamaños y la integracion con bases de datos, con tal de facilitar el intercambio de informacion que este lenguaje provee. Por otro lado, XSL, o *Extensible Stylesheet Language*, permite mostrar la informacion guardada en un documento XML, dandole formato a este ultimo.

![fotoXML](https://cdn2.slideserve.com/4949059/slide1-n.jpg)

## Elementos de sintaxis basicos

- **Elementos:** Son fundamentales en cualquier documento XML a la hora de estructurar informacion. Los elementos siempre se marcan por etiquetas de apertura y cierre. Ejemplo: `<elemento></elemento>`.
- **Texto:** La informacion visible que es almacenada y representada dentro de los elementos XML. Ejemplo: `<usuario>peña4198</usuario>`.
- **Atributos:** Dentro de las etiquetas de apertura de un elemento, es posible representar informacion adicional mediante atributos. Ejemplo: `<usuario id="43">peña4198</usuario>`.
- **Comentarios:** Se utilizan para agregar comentarios dentro del documento XML, idealmente para marcar cambios a realizar o para describir la funcionalidad de un elemento o atributo. Ejemplo: `<!-- La etiqueta <usuario> almacena un nombre de usuario unico con su respectiva ID almacenada como atributo. -->`.

## Ejemplo de Documento XML

```XML
<?xml version="1.0" encoding="UTF-8"?>
<selva>
    <animal>
        <nombre>Werthers</nombre>
        <tipo>Pantera</tipo>
        <color>Negro</color>
        <edad>12</edad>
        </animal>
    <animal>
        <nombre>Bun</nombre>
        <tipo>Leon</tipo>
        <color>Marron</color>
        <edad>15</edad>
    </animal>
</selva>
```
