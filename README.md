# reto_12
# 1. Cantidad de vocales
```
Texto = "Texto.txt" #define la variable texto para seleccionar el archivo a abrir  

with open(Texto, 'r') as archivo:
    contenido = archivo.read() # se lee el texto 

def contar_vocales(texto):
    vocales = 'aeiouAEIOU'  # Escribimos las vocales en minúsculas y mayusculas
    contador = 0 # se inicia el recuento

    for letra in texto:  # se buscan los digitos 
        if letra in vocales:
            contador += 1

    return contador

cantidad_vocales = contar_vocales(contenido)  # se da el resultado sin imprimir aun
print("La cantidad de vocales en el texto es:", cantidad_vocales) # se imprime la cantidad encontrada  22450

```



# 2.Cantidad de consonantes
```
Texto = "Texto.txt" # se define la variable del texto a abrir

with open(Texto, 'r') as archivo: # el texto se abre y se define como archivo
    contenido = archivo.read() # el archivo se lee 

def contar_Letras(texto):  #se define la funcion a realizar 
    Letras = 'QWRTYPSDFGHJKLÑZXCVBNMqwrtypsdfghjklñzxcvbnm' # se definen los digitos a buscar tanto en minusculas como en mayusculas sin separarlas para evitar que cuente espacios ya que estos tambien se representan  
    contador = 0 # se inicia el contador 

    for letra in texto:       # se empieza a contar las letras
        if letra in Letras:
            contador += 1

    return contador


Catidad_Letras = contar_Letras(contenido)   # se da ek uso 
print("La cantidad de consonantes en el texto es:", Catidad_Letras)
```



# 3. Listado de las 50 palabras que más se repiten
```
Texto = "Texto.txt" #se define la variable

with open(Texto, 'r') as archivo: 
    contenido = archivo.read()

def contar_palabras(texto): #se define la funcion
    texto = ''.join(c if c.isalpha() or c.isspace() else ' ' for c in texto.lower()) # se usan distintas herramientas para limpiar el texto y convertirlo en minusculas para un mejor trabajo
    
    palabras = texto.split() # se corta el texto para facilitar la division entre palabras en el texto 
    
    contador = {}      # se utliza un contador para hacer el recuento de la cantidad de palabras que hay
    for palabra in palabras:
        contador[palabra] = contador.get(palabra, 0) + 1 # cada vez que aparezca una nueva palabra similiar a otra se sumaran
    

    palabras_ordenadas = sorted(contador.items(), key=lambda x: x[1], reverse=True) # se ordenan las palabras aparecidas 
    

    palabras_mas_repetidas = [palabra for palabra, _ in palabras_ordenadas[:50]] # esto se encarga de dar un limitador a la cantidad de palabras que se mostraran en pantalla
    
    return palabras_mas_repetidas

palabras_mas_repetidas = contar_palabras(contenido)

print("50 palabras más repetidas:")
for palabra in palabras_mas_repetidas:
    print(palabra)
    ```


# 4.Listado de destinatarios con cantidad de mensajes recibidos




# 5. Cantidad de mensajes enviados por cada día 
