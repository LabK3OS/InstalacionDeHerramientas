# Instalación de herramientas de K3OS

## 1. Creación de imagen de Raspbian
Descargar Raspberry Pi Imager en https://www.raspberrypi.org/downloads/ e instalar la version por defecto de Raspbian en la microSD 


## 2. Instalación de herramientas

### Actualizar
```
sudo apt update
```
### Instalación de SonicPI: 
```
sudo apt install sonic-pi
pip3 install python-osc
pip install python-sonic // Pendiente por verificar
    
```
### Instalación de Edublocks: 
```
curl -sSL get.edublocks.org | bash
cd /opt/
sudo chmod 777 -R edublocks-desktop/
```   
   
### Instalación de Processing: 
```
pip3 install p5
sudo apt-get install libglfw3

```

### Habilitar cámara y periféricos:
 
```
sudo raspi-config
Navegar en el menu, y activar la camara
```
### Instalación de Minecraft
TODO  minecraft + libreria minecraft


## 3. Instalación de dependencias


### Actualizar e instalar dependencias de compilación de dlib
```
sudo apt update
sudo apt full-upgrade
sudo rpi-update
sudo apt install build-essential cmake
sudo apt install libboost-all-dev
sudo apt install libgtk-3-dev
```
### Cambiar tamaño del swap:
```
sudo nano /etc/dphys-swapfile
```
Cambiar CONF_SWAPSIZE=1024 por CONF_SWAPSIZE=100, guardar con ctrl+o, Enter, salir con ctrl+x
```
sudo /etc/init.d/dphys-swapfile restart
```
### Instalar dlib:
```
mkdir -p dlib
git clone -b 'v19.6' --single-branch https://github.com/davisking/dlib.git dlib/
cd ./dlib
sudo python3 setup.py install --compiler-flags "-mfpu=neon"
```
### Cambiar tamaño del swap de nuevo:
```
sudo nano /etc/dphys-swapfile
```
Cambiar CONF_SWAPSIZE=1024 por CONF_SWAPSIZE=100, guardar con ctrl+o, Enter, salir con ctrl+x
```
sudo /etc/init.d/dphys-swapfile restart
```

### Instalar libreria face
```
sudo pip3 install face_recognition
sudo apt install libatlas-base-dev
```

### Instalar libreria de Matriz de leds
	pip3 install RPimax7219

## 4. Modificar EduBlocks
    Remplazar main.js del repositorio en /opt/edublocks-desktop/ui/dist.
    Remplazar en.js del repositorio en /opt/edublocks-desktop/ui/blockly/msg/js
    Remplazar carpeta script-includes en /opt/edublocks-desktop
	Crear carpeta /home/pi/Desktop/.Extras/ y copiar en su interior el archivo "Memorial Lane.otf"