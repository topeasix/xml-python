# XML

[Link de w3schools](https://www.w3schools.com/xml/xml_whatis.asp)

---

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

## Ejemplo de Documento XSL

```XSL
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
    <xsl:output method="html" indent="yes"/>
    <xsl:template match="/horari">
        <html>
            <style type="text/css">
                    <xsl:for-each select="colors/color">
                        .<xsl:value-of select="@codi"/>{background-color: <xsl:value-of select="."/>; padding: 15px; margin: 1px;}
                    </xsl:for-each>
                    body{
                        background-color: rgba(249,249,249,255);
                        text-align: center;
                        margin: 2px;
                        font-family: Arial, sans-serif;
                        font-size: 130%;
                    }
                    img{
                        width: 100%;
                        height: 145px;
                    }
                    table{
                        width: 100%;
                        text-align: center;
                        border-collapse: collapse;
                        font-size: 130%;
                        background-color: rgba(204,204,204,255)
                    }
                    li, a{
                        list-style-type: none;
                        padding: 6px;
                        color: rgb(0,0,0);
                    }
                    div:nth-of-type(2){
                        background-color: rgba(249,249,249,255)
                    }
            </style>
            <body>
                <img src="{@header}"/>
                <div>
                    <table>
                        <tr>
                            <xsl:for-each select="setmana/dia">
                                <th>
                                    <xsl:value-of select="@nom"/>
                                </th>
                            </xsl:for-each>
                        </tr>
                        <tr>
                        <xsl:for-each select="setmana/dia">
                            <td>
                                <xsl:for-each select="modul">
                                    <p class="{codi}">
                                        <xsl:value-of select="codi"/>
                                        &#160;
                                        <xsl:value-of select="nom"/>
                                    </p>
                                </xsl:for-each>
                            </td>
                        </xsl:for-each>
                    </tr>
                    </table>
                </div>
                <br/>
                <div>
                    <ul>
                        <h1><xsl:value-of select="links/@nom"/></h1>
                        <xsl:for-each select="links/link">
                            <xsl:sort select="nom"/>
                            <li>
                                <a href="{url}">
                                    <xsl:value-of select="nom"/>
                                </a>
                            </li>
                        </xsl:for-each>
                    </ul>
                </div>
            </body>
        </html>
    </xsl:template>
</xsl:stylesheet>
```

---

# Python

[Link de w3schools](https://www.w3schools.com/python/default.asp)

---

## Introduccion

Python es un lenguaje de programacion utilizado para crear todo tipo de programas alrededor del mundo, con una cantidad casi infinita de opciones para programar exactamente lo que quieres que tu codigo ejecute. En el mundo del XML, se puede utilizar la libreria *minidom* para convertir la informacion de un documento XML a un documento HTML. Se podria decir que el uso de esta libreria es una alternativa al uso del lenguaje XSL.

![fotoPython](https://cdn01.zoomit.ir/2021/1/python-programming.jpg)

## Elementos y funciones basicas

- **Bucles:** Mediante las funciones `for` y `where`, es posible crear bucles que recorran un objeto en especifico o de acuerdo a que una condicion se continue cumpliendo, respectivamente. Ejemplos: for - `for entrada in llista:` | where - `where intentos > 0:`
- **Operaciones aritmeticas:** No solo es posible almacenar numeros dentro de variables, sino que tambien se pueden utilizar para ejecutar operaciones matematicas, tales como sumas `(50 + 295)`, restas `(455 - numero)`, multiplicaciones `(20 * 3)`, divisiones `(numero / 30)` o porcentajes `(1000 % 50)`. 
- **Listas y diccionarios:** Al definir una variable como `[]` o `{}`, es posible crear una lista de valores o un diccionario con multiples datos por valor, respectivamente. Ejemplos: Lista - `Numeros1al10 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` | Diccionario - `EstudiantesProgramacion = [{'nombre' : 'Carlos', 'edad' : 22, 'cursos': ['Python', 'Django', 'JavaScript']}, {'nombre' : 'Mariano', 'edad' : 20, 'cursos': ['C', 'C++', 'Django']}]`
- **Lectura y escritura de archivos:** Para manipular archivos editables, primero es necesario abrir el archivo deseado con `open(?, archivo.extension)`, remplazando **?** con una de las siguientes opciones:
    - *r*: Lee el archivo especificado, pero **devuelve un error si este archivo no existe**.
    - *a*: Abre el archivo especificado y permite escribir lineas a partir del final del documento existente. **Devuelve un error si este archivo no existe**.
    - *w*: Abre el archivo especificado y permite escribir lineas, sobrescribiendo todo el documento. **Si el archivo no existe, lo crea**.
    - *x*: Crea el archivo con el nombre especificado, pero **devuelve un error si este archivo ya existe**.
Una vez creado o abierto el archivo, es posible cambiar su contenido por otro de nuestro eleccion o añadir contenido nuevo junto al que ya existe:
    - *read()*: Lee todo el documento. Dentro del `()`, se puede definir el numero de caracteres que el codigo debe leer en vez de todo el documento.
    - *readline()*: Lee las lineas del documento en orden. En su primera ejecucion, devolvera la primera linea; en la segunda ejecucion, devolvera la segunda; etc.
    - *readlines()*: Lee todas las lineas del documento y las añade a una *lista*.
    - *write()*: Añade una nueva linea con contenido especificado dentro del `()`. La primera linea se encontrara al final del documento o al principio del documento sobrescribido, dependiendo tanto de la opcion que se haya utilizado previamente como del archivo en cuestion.

## Ejemplo de Documento Python con minidom

```Python 3
from xml.dom import minidom

docxml = minidom.parse("UF2A2-XmlProva.xml");

llista_person=docxml.getElementsByTagName("person")

file = open("UF2A2-XmlProva.html", "w")

file.write("<html>\n    <head>\n        <title>Diaris DOM</title>\n    </head>\n    <body>\n")

for person in llista_person:
    personAtt=person.getAttribute("id")
    nomNode=person.getElementsByTagName("name")[0]
    nom=nomNode.firstChild.data
    nomAtt=nomNode.getAttribute("gender")
    edat=person.getElementsByTagName("age")[0].firstChild.data
    naixement=person.getElementsByTagName("naixement")[0].firstChild.data
    file.write(f"        <h2>{personAtt} - {nom}</h2>\n")
    file.write(f"        <ul>\n            <li>age - {edat}</li>\n            <li>sex - {nomAtt}</li>\n            <li>naixement - {naixement}</li>\n        </ul>\n")

#print(docxml.toxml())

file.write("    </body>\n</html>")

file.close()
```
