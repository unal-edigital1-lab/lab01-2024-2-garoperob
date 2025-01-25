# Sumador de 1 bit 
## Gustavo Adolfo Ropero Bastidas

## Código 

Para la realización de la primera práctica se tomó el siguiente código:
```
`include "/home/volplet/Escritorio/digital1v2/lab01-2024-2-garoperob/src/sum1bcc_TB.v"
module sum1bcc (A, B, Ci,Cout,S);

  input  A;
  input  B;
  input  Ci;
  output Cout;
  output S;

  reg [1:0] st; 
  assign S = st[0];
  assign Cout = st[1];

  always @ ( * ) begin
  	st  = 	A+B+Ci;
  end
  
endmodule
``` 
Donde las palabras "module" y "endmodule" son usadas para crear un archivo en verilog, cada modulo se puede combinar para producir distintos programas. Sin embargo, sólo un archivo .v puede ser el archivo de comando principal. La declaración de las variables a usar se debe hacer en el module. Por otro lado, las palabras input y output son usadas para generar asignar las entradas y salidas, respectivamente, a partir de las variables que se tengan. Continuando con el código, se encuentra el comando "reg" que se usa para declarar registros, estos no son necesarios declararlos en module; despues, la palabra "assign"; se usa para asignarle un valor a una variable de salida. Finalmente, la línea "always @ ( * ) begin" crea un bloque funcional que se mantenie permanentemente en ejecución. Cabe aclarar, que la mayoria de las funciones de verilog encierran los procesos entre las palabras "begin" y "end".

El proceso que se lleva a cabo dentro de "always" es la suma de dos números de 1 bit y un carry de entrada. Este valor se esta asignado al regitro st, donde, el bit menos significativo se añade a la salida S, mientras que el más significativo se asigna al carry de salida. Esto se hace porque la suma produce un número de 2 bits, el cual no se puede representar con la salida de 1 bit. 
## Simulación

## Implementación
