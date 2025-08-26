### Install


Clonar repositorio:
```bash
git clone https://github.com/ZakXero/Config_Custom_Parrot_OS
```


Mover Scripts_IPs/ al $PATH /usr/local/bin para su correcto funcionamiento:
```bash
mv ./Scripts_IPs/ /usr/local/bin
```


Añadir al Panel de MATE por cada script que quieras añadir, seleccionar la opción de [comando/command] y añadir la ruta del script:
```bash
cat /usr/local/bin/Scripts_IPs/target
cat /usr/local/bin/Scripts_IPs/ip_htb
cat /usr/local/bin/Scripts_IPs/ip_propia
```


### Usage


Usage target:
```bash
# Usage target normal
target <nombre> <ip>

# Eliminar archivo temporal
target -c o --clear 
```

