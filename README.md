# Pila-Lamp-en-dos-niveles
practica Pila Lamp en dos niveles
Empezamos metiendonos al promox y ahi creamos un directorio para que podamos trabajar ordenados.
Creamos un archivo vagrant y lo configuramos de la siguiente manera: Vagrant init(y con una nano entramos al archivo)
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/4ffeefbd-62f6-4077-b262-5ace5af9e7cc)
configuramos dos maquinas una para el apache y otra para el sql con debian 11, configurando a cada una sus respectivas ip
Levantamos las maquinas con vagrant up

en local me funciona el mismo vagranfile que me da error en promox, asique continuare en local

entramos con vagrant ssh arturosql
realizamos un update y upgrate
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/8345d12c-116d-485e-a533-2f2fda4d87e0)

luego entramos vagrant ssh arturoapache
