# xml-python-francisco

Python y XML
En este repositorio encontrarás información sobre cómo trabajar con XML en Python.

Introducción
Python es un lenguaje de programación versátil que proporciona bibliotecas y herramientas para trabajar con diversos formatos de datos, incluido XML.

¿Qué es XML?
XML (Extensible Markup Language) es un lenguaje de marcado que se utiliza para almacenar y transportar datos de manera legible tanto para humanos como para máquinas. Permite estructurar la información mediante etiquetas que describen los datos.

Trabajando con XML en Python
Python proporciona varias bibliotecas y módulos para trabajar con XML, entre los cuales se destacan:

xml.etree.ElementTree: Este módulo permite analizar y manipular documentos XML de una manera sencilla y eficiente.
xml.dom: Proporciona una interfaz para el Modelo de Objetos de Documento (DOM) de XML, que permite acceder y manipular el contenido de un documento XML como una estructura de árbol.

Ejemplos de Uso
A continuación, se muestran algunos ejemplos básicos de cómo trabajar con XML en Python utilizando la biblioteca xml.etree.ElementTree:



import xml.etree.ElementTree as ET

# Analizar un archivo XML
tree = ET.parse('archivo.xml')
root = tree.getroot()

# Acceder a elementos y atributos
for child in root:
    print(child.tag, child.attrib)

# Obtener el texto de un elemento
for elem in root.iter('elemento'):
    print(elem.text)

# Crear un nuevo elemento y añadirlo al árbol
nuevo_elem = ET.Element('nuevo_elemento')
nuevo_elem.text = 'Contenido del nuevo elemento'
root.append(nuevo_elem)

# Escribir el árbol XML modificado de vuelta al archivo
tree.write('archivo_modificado.xml')


Recursos Adicionales
Documentación oficial de Python sobre XML
https://docs.python.org/3/library/xml.html

Tutorial de W3Schools sobre XML
https://www.w3schools.com/xml/
