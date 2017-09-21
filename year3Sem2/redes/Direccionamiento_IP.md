##Clasificacion de IP
#Clase A
Rango: 0 - 126
Rango Privado: 10.0.0.0 - 10.255.255.255

#Clase B
Rango: 128 - 191
Rango Privado: 172.16.0.0 - 172.31.255.255

#Clase C
Rango : 192 - 223
Rango Privado: 192.168.0.0 - 192.168.255.255

#Clase D
Multicast
Rango:224.0.0.0 - 239.255.255.255


#Putty
*Pasos de inicio cuando se conecta al router
*Conectar al puerto serial en el puerto 16 COM1
*Putty se conecta y hace un reconocimiento con el programa boostrap
*luego intenta buscar el sistema operativo en la flash del router.
*Si no lo encuentra lo busca en un servidor ftp o con parametros minimos.
*Busca el archivo de configuracion en la NVRAM ( non volatile ram ) y lo carga.
*Si no lo encuentra, le pide al usuario que lo introduzca por teclado

*Se coloca en el modo usuario ( Se imprime Router> )
Ver comando en el modo usuario "?" ---> Router>?
Modo Privilegiedo
comando : enable  ---->Router#
Modo de Configuracion Global
comando: configure terminal ---> Router(config)#
Modo de Configuracion de interface
comando interface s0 ----> Router(config-if)#
Crtl + z regresa al modo privilegiado
comando sh run: muestra la configuracion en la memoria
Password importantes:
"cisco"
"class"


Configracion de password
Password priviligiado
Entrar al modo de configuracion global
luego commando : enable secret cisco
Password modo uusario
Entrar al modo de configuracion global
luego comando: line console 0
comando: password class
comando: login

configurar puerto
Entrar al modo ded config global
comando: interface serial 0
comando: ip address "ip" "mascara"
comando :no shutdown

Configurar nombre del router
comando: hostname "nombre router"

Password remoto
comando : line vty 0 4
comando :password cisco
comando : login

Mostrar configuracion en la nvram
comando: show startup-config

Guardar a la nvram
comando :copy running-config startup-config
registro por defaul de configuracion: 0x2102
El profe lo comabio al 0x2142 para evitar dolores de cabeza en el laboratorio
