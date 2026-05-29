# \# DNS maestro/esclavo - sistema.test

# 

# \## Descripción

# Configuración de un servidor DNS maestro (tierra) y esclavo (venus) 

# usando BIND9 sobre máquinas virtuales Debian con Vagrant.

# 

# \## Red

# \- Red: 192.168.57.0/24

# \- tierra.sistema.test (maestro): 192.168.57.103

# \- venus.sistema.test (esclavo): 192.168.57.102

# \- mercurio.sistema.test: 192.168.57.101

# \- marte.sistema.test: 192.168.57.104

# 

# \## Cómo ejecutarlo

# 1\. Instalar Vagrant y VirtualBox

# 2\. Clonar el repositorio

# 3\. Ejecutar: vagrant up

# 4\. Pasar los tests con: test.bat 192.168.57.103

# 

# \## Transferencia de zona

# La transferencia de zona se produce automáticamente al arrancar venus.

# Se puede verificar con el siguiente comando desde cualquiera de las máquinas:

# 

# &#x20;   dig @192.168.57.102 -t AXFR sistema.test

# 

# \## Alias configurados

# \- ns1.sistema.test → tierra.sistema.test

# \- ns2.sistema.test → venus.sistema.test

# \- mail.sistema.test → marte.sistema.test

