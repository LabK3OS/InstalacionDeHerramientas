# Instalación de herramientas de K3OS

## 1. Creación de imagen de Raspbian


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
