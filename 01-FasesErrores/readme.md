1) gcc -E hello2.c -o hello2.i

Genera archivo .i producto del preprocessing del archivo hello2.c

Dentro de su contenido tiene declaraciones de tipos de datos incluidos dentro del "stdio.h". A su vez, elimina el comentario ingresado en el codigo.

2) int printf(const char *format, ...) la semantica de esta sentencia es la de enviar formateado el output de nuestro programa al stdout.

3) gcc -E hello3.c -o hello3.i

Genera archivo .i producto del preprocessing del archivo hello3.c

Dentro de su contenido, a diferencia del hello3.c, elimina el comentario ingreso en el codigo, y agrega algunos comentarios del preprocessing.

4) gcc -S -save-temps hello3.c
Obtuve archivo .s de hello3, sin ensamblar.

5)  gcc -E hello4.c -o hello4.i
Genera archivo .i producto del preprocessing del archivo hello4.c

gcc -S -save-temps hello4.c

Genera el .s con las sentencias mov, entre otras, en codigo assembler.

6) Para ensamblar hello4.s en hello4.o use

gcc -c hello4.s -o hello4.o

Me genero el archivo .o pero sin vincular

7) gcc hello4.o -o hello4

Me da el siguiente error: "Undefined reference to 'prontf'"

8) Corrijo en hello5.c, cambiando prontf por printf

gcc -E hello5.c -o hello5.i

gcc -S -save-temps hello5.c -> al ejecutar esta linea me da un warning de que format'%d' espera un int como argumento.

gcc -c hello5.s -o hello5.o

gcc hello5. -o hello5 -> me genera el ejecutable

9) hello6 no hace falta ya que me funciona correctamente

10) hello7 funciona ya que se le pasa al printf el argumento int que espera, esta definida la libreria estandar.


