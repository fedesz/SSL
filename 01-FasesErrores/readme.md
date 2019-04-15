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

6) 

