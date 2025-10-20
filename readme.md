# Evaluación módulo 1 proceso explicado:

## Esructura:

- Creamos tres variables, una será una lista de diccionarios, otra un diccionario con otro diccionario como valor y otra un float al que damos resultado 0.

## Funciones:

#### 1. agregar_producto (nombre, precio,cantidad)

1. ¿Qué nos piden?

   - Comprobar si el producto ya está en el inventario.
   - Si el producto está, actualizar la cantidad.
   - Si el producto no está previamente, incluirlo.

2. ¿Qué necesitamos?

   - Usaremos un bucle  for paa movernos por el diccionaario en busca de la coincidencia.
   - Crearemos condiciones para actuar en caso de que esté o no previamente en inventarrio.
   - Crearemos una variable para establecer los parametros del nuevo producto ¡Si el bucle for no encontró coincidencias!
   - Introducimos el producto en el diccionario con un append.
   - Retornaremos mensajes en caso de coincidencia en inventario y actualización de cantidad o para avisar de que el nuevo producto ya ha sido añadido a inventario.

3. ¿Como usarlo?
      
    - Escribiemos por ejemplo: 
      - **agregar_producto("bolso", 25.5, 10)** 
        
     donde agregaremos en el paréntesis el nombre del producto nuevo entre comillas seguido de coma, el precio seguido de coma y por último la cantidad.
    
    - IMPORTANTE: Recuerda que si se quierre introducir un precio con decimales deberá usarse un punto en vez de coma para escribirlo como en el ejemplo.

#### 2. ver_inventario

1. ¿Qué nos piden?

    - Imprimir el inventario con detalle de $ frente al precio.

2. ¿Qué necesitamos?

   - Crearemos una variable nueva para volcar la nueva lista junto con los string que nos piden, en este caso introducir $ fente al precio.
   
   - De nuevo recorremos el diccionario con un bucle for.

   - Creamos una nueva variable que contenga el precio junto al string.

   - Usamos un .append para introducir en la variable vacía todos los parámtros incluyendo el precio con $ en el formato que previamente nos pidieron.

   - Por ultimo devolvemos el print de la nueva variable que será lo que nos han pedido.

3. ¿Como usarlo?

   - Solo hay que introducir en nuestro cuadro de código la función **ver_inventario()**

   - IMPORTANTE: No olvidar nunca los paréntesis tras la función aunque estén vacíos.

#### 3. producto(nombre)

1. ¿Qué nos piden?
    
    - Buscar un producto  en el inventario
      
      - Si se encuentra en diccionario: mostrar sus detalles de la forma que nos lo están pidiendo, coon string & frente a precio.
      - Si no devolver un mensaje de que no está en el inventario.

2. ¿Qué necesitamos?

    - Un bucle for para recorrer el inventario en busca del producto.

    - Una condición if dentro del for para buscar la coincidencia.

    - Dentro del if, en caso de que sí esté dentro haremos un return creando una variable para contener los datos junto con el string como en el ejercicio anteior.

    - Si el for no encuentra coincidencia, fuera de él pondremos un else para retornar el mensaje de prroducto no encontrado

    - IMPORTANTE: El else debe estar fuera del bucle for para funcionar solo si el bucle no encoontro la coincidencia.

3. ¿Como usarlo?

   - Deberemos escribir en un cuadro de codigo **producto(nombre)** Donde nombre será el artículo que queremos buscar y deberá ir enre comillas"".

4. A nivel aclaratorio:

He introducido otra manera de  hacer la función suponiendo  que se introduce el producto pero no completo o con algun error usando .lower, no es demasiado util pero si lo fusionamos  con el otro como ocurre en el ultimo ejemplo podria  ayudar en según qué ocasiones.

#### 4. actualizar_stock(nombre, cantidad)

1. ¿Qué nos piden?

   - Introducir un artículo y una cantidad 
     
     - Si el artículo está en inventario:
       
       Actualizar stock
     - Si no está:

        incluir articulo nuevo y stock

2. ¿Qué necesitamos? 

   - De nuevo un for para buscar en el inventario

   - if para establecer la condicion de coincidencia y en ese caso le diremos que sumela cantidad nueva con el stock previo. Devolver mensaje de stock actualizado

   - Situamos else FUERA del bucle for para que devuelve mensaje de producto añadido.


3. ¿Como usarlo?

   - Deberemos escribir en un cuadro de codigo  **actualizar_stock(nombre, cantidad)**  
   donde dentro del paréntesis escribiremos entre comillas el producto a actualizar y seguido de coma el stock con un número entero.

He introducido una 

#### 5. eliminar_producto(nombre)

1. ¿Qué nos piden?

   - Eliminar un producto del inventario por lo que primero endemoss que buscar si el producto está previamene en inventario.
     
     - Si está, lo eliminamos.
     - si no está, devolvemos mensaje de producto no encontrado.

2. ¿Qué necesitamos? 

   - De nuevo un bucle for para recorrer inventario en busca de coincidencias y la condicional para establecer el criterio de coincidencia.

   - Dentro del bucle usamos un .remmove para eliminar el producto y devolvemos mensaje de producto eliminado.

   - fuera del for un else y un eturn con producto no encontrado.

3. ¿Como usarlo?

   - Deberemos escribir en un cuadro de codigo **eliminar_producto(nombre)** 
   donde dentro del parentesis escribiremos entre comillas el producto que deseamos eliminar.

#### 6. calcular_valor_inventario()

1. ¿Qué nos piden?

   - Calcular el valor del inventario 

2. ¿Qué necesitamos?

   - Bucle for para recorrer el diccionario y una variable donde hacer la suma. también un print o un return para devolver el valor del inventario.

3. ¿Como usarlo?

   - Deberemos escribir en un cuadro de codigo **calcular_valor_inventario()** 
   y ejecutar la celda.

#### 7. realizar_compra()

1. ¿Qué nos piden? 

   - Preguntar al cliente dándole a elegir de una lista  qué productos desea comprar y qué cantidad.

   - Una vez elegidos actualizar stock y mostrar al cliente su carrito y el precio de lo que ha comprado.

2. ¿Qué necesitamos? 

      - Primero dos variables vacias donde introduciremos los productos que el cliente desea y el precio total de su compra.

      - Usareos  un bucle while para recorrer el inventario tantas veces como el cliente necesite hasta realizar sus compras.

    - un bucle for con un print que usaremos para imprimir el inventarrio actualizado para que el cliente decida qué comprar.

    - una variable con un imput para interaccionar con el cliente y guardar momentaneamente su elección.
    
    - Varias condiciones if para los distintos bucles.

    - Utilizamos un try y except para subsanar errores

    - Un round para redondear al segundo decimal en el precio total.


3. ¿Como usarlo?

   - Deberemos escribir en un cuadro de codigo 
   ***realizar_compra()*** Y simplemente contestar a las preguntas de elección de artículo y cantidad.



## Ejercicios bonus:

#### 1. procesar_pago()


1. ¿Qué nos piden?

   - Pedir al cliente que escriba la cantidad que debe pagar y la que está pagando. Comprobar si el pago es suficiente y en caso afirmativo mostrar un mensaje de confirmación y cuanto le debe ser devuelto. En caso negativo indicar al cliente cuanto más debe abonar.
   - Subsanar errores de tecleo.

2. ¿Qué necesitamos?

   - Dos variables para introducir un imput y guardar las cantidades a pagar y lo que se ha pagado.

   - Condicionales is, elif y else para interaccionar con el cliente mediante print e informarle de si su pago es o no correcto y cuanto se le devuelve..

   - try except para subsanar errores si el cliente introduce una respuesta no válida como por ejemplo si introduce el string & junto al precio o si pone , en vez de . para los decimales (las cantidades negativas las subsanamos con un if <>).


3. ¿Como usarlo?

   - Deberemos escribir en un cuadro de codigo 
   ***procesar_pago()*** Y simplemente contestar a las preguntas de elección de artículo y cantidad.


#### 2. agregar_cliente(nombre, email)

1. ¿Qué nos piden?

   - Agregar un cliente al diccionario **clientes** introduciendo SOLO las variables ***nombre** y **email** con la complicación de que no introducimos la variable **compras** que es también una lista.

2. ¿Qué necesitamos?

   - Usaremos un if para ver si el nombre ya está en el diccionario **clientes**.

      - si está: devolvemos un mensaje de cliente ya está en **inventario**

      - Si no: else.

    - Dentro del else usaremos un .update en la variable **clientes** para volcar el nuevo cliente allí.

    - IMPORTANTE : dejaremos la variable **compras** vacía en la función [] para decirle que la incluya como lista vacía.


### 3. ver_clientes()

1. ¿Qué nos piden?

   - Que mostremos un diccionario de clientes en la que aparezca nombre: email, con la complicación de que la key email está como producto dentro de otro diccionario, hay que sacarla para trabajar con ella.

2. ¿Qué necesitamos?

   - Cear un diccionario vacío donde volcar los clientes y los emails.
   
   - Un bucle for para recorrer el diccionario y para obtener las keys usaremos un .items

   - introducimos en el diccionario los nombres y los emails.

   - Por último imprimimos el diccionario que hemos creado previamente