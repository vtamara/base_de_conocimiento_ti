# Criptominado en piscina

Autor: Vladimir Tamara

Actualizaciones: Daniel Cardona Nogueira, Sebastian Cabrera

## 1. Introducción
En el CINEP/PPP desde la Oficina TI con autorización de dirección, estamos investigando el minado de criptomonedas 
desde los sistemas de fuentes abiertas (Linux y adJ) con participación voluntaria de los usuarios interesados.

Por el momento la investigación se concentra en:

1. Minar en una piscina pública con buen historial, la criptomoneda Monero hasta lograr tener algo en la billetera del 
   CINEP/PPP (se ha visto que el mínimo para recibir un pago son 30 centavos de Monero)

2. Minar suficiente en piscina pública para lograr hacer alguna transacción (se ha visto en sitios de cambio que 
   la transacción mínima es con 1 centavo de Bitcoin (0.01 BTC) que corresponde aproximadamente a 1.60 moneros --XMR).

3. Minar bien en una piscina propia del CINEP o bien en una donde pueda distinguirse la contribución de 
   cada persona para distribuir pagos a quienes minen de acuerdo a políticas por establecer con dirección.

Elegimos Monero porque tiene buen valor en el mercado y es fácil de minar con hardware no especializado.  Para todo el 
proceso empleamos programas de fuentes abiertas por seguridad, pues pueden ser auditados, nosotros mismos 
compilamos buscando garantizar que no se trate de malware y que maneje con transparencia y honestidad lo que se mina.

## 2. Estado de la investigación

La investigación comenzó a finales de 2017, a finales de semana santa de 2018 se completó la primera fase.  Los  
resultados de la primera fase pueden verse en el sitio de la primera piscina que usamos  <https://monero.crypto-pool.fr>, 
en el campo "Your Stats & Payment History"  poner la dirección pública de la billetera del CINEP, y presionar el botón 
Lookup a la derecha de tal campo.

Para la segunda fase hemos cambiado a una piscina más veloz, que requiere menos comisión y que permite ver de manera 
separada la contribución de cada computador individual del CINEP (al igual que en la primera fase todo computador que 
mine en CINEP debe hacerlo a la billetera de la Oficina TI).

Puede ver el estado del minado dividido de acuerdo a los computadores que están minando en 
<https://www.supportxmr.com/#/dashboard>

Presione en la parte superior You, en la parte inferior donde dice Enter Payment Addres ponga la dirección de la billetera 
del CINEP y presione TRACK LIVE STATS

En preparación para la tercer fase estamos revisando con periodicidad  
<https://www.bestchange.com/monero-to-bitcoin.html>  donde se comparan cambiadores de monera a bitcoin (entre otros) e
históricos del intercambio.



## 3. Minado desde Linux

Si ya tiene instalado su minero, abra una terminal (desde el dash escribir terminal y elegir) y en esta escriba:

      cd ~/comp/monero/xmrirg/build

      ./xmrig

De este manera comenzará a minar usando 3 núcleos del procesador de su computador.



## 4. Instalación en Linux 

El siguiente procedimiento permite descargar y compilar un minero que emplea la CPU y que por omisión usará la piscina 
pool.supportxmr.com:3333  y la billetera de la Oficina TI.

Usa un minero disponible en  <https://github.com/vtamara/xmrig> que se ha modificado para:

* Permitir compilación en adJ
* Utilizar la piscina indicada y la billetera de la Oficina TI

Para instalar desde la terminal

         sudo apt update; sudo apt dist-upgrade;

         sudo apt install git cmake libuv1-dev libssl-dev libmicrohttpd-dev build-essential libhwloc-dev
         mkdir -p ~/comp/monero
         cd ~/comp/monero
         git clone https://github.com/vtamara/xmrig
         cd xmrig
         git checkout cinep
         cd build
         vi config.json

  Con el editor de preferencia cambiar en la linea

         passw: "creo"

  "creo" por el nombre del equipo 
      
         cmake ..
         make 


Para actualizar en Linux lo más sencillo es borrar el directorio `comp/monero/xmrig` y volver a seguir el procedimiento de instalación.

## 5. Instalación y uso en adJ
      
         doas pkg_add cmake

         mkdir -p ~/comp/monero
         cd ~/comp/monero
         git clone https://github.com/vtamara/xmrig
         cd xmrig
         git checkout cinep

         cd build
         cmake .. -DWITH_ASM=OFF -DWITH_HWLOC=OFF
         make

         vi config.json

Con el editor de preferencia cambiar en la linea

         passw: "creo"

En adJ hemos tenido problema con versiones recientes de xmrig en tiempo de ejecución, se están investigando en el momento de este escrito.
