# Pila-Lamp-en-dos-niveles
practica Pila Lamp en dos niveles
Empezamos metiendonos al promox y ahi creamos un directorio para que podamos trabajar ordenados.
Creamos un archivo vagrant y lo configuramos de la siguiente manera: Vagrant init(y con una nano entramos al archivo)
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/4ffeefbd-62f6-4077-b262-5ace5af9e7cc)

configuramos dos maquinas una para el apache y otra para el sql con debian 11, configurando a cada una sus respectivas ip
Levantamos las maquinas con vagrant up
para este codigo vagrant hay que añadir
 arturoapache.vm.provision "shell", path: "scriptapache.sh" 
 en la maquina apache y:
  arturosql.vm.provision "shell", path: "scriptsql.sh"

en local me funciona el mismo vagranfile que me da error en promox, asique continuare en local

 #SQL
 
entramos con vagrant ssh arturosql
realizamos un update y upgrate
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/33ec4f1c-eec2-4a04-9803-2bc93db101f1)

modificamos el fichero 50-server-cnf del directorio /etc/mysql/mariadb..conf.d poniendo nuestra ip
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/039ca1b1-429a-4ca2-88be-84e8785eecff)

y creamos usuario con privilegios
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/455ff8a4-5a2e-4827-8269-07531091f561)


clonamos https://github.com/josejuansanchez/iaw-practica-lamp.git con sudo git clone https://github.com/josejuansanchez/iaw-practica-lamp.git

#apache
luego entramos vagrant ssh arturoapache y realizamos tambien un sudo apt y upgrade
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/b228c6b8-43a5-4fdb-bf96-79f23008b0bd)

creamos carpet LDN y clonamos el github cambiandole de dueño
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/d3835f29-25a0-4712-8c93-825b19c835af)
copiamos  la carpeta src a la LDN
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/28f8e370-a148-4416-8bd8-afb0b1ecc93a)
copiamos archivo de configuracion y lo cambiamos a nuestro directorio creado
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/39528152-8e8c-4ad4-8146-858762fdfd6d)
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/1ed00256-2f8a-4ec8-aa1c-b53bdfbf0df1)
habilitamos la configuracion de a2dissite
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/725379c8-3016-43fb-8bfb-96793e2e54ec)
configuracion el sudo nano config.php de cd /var/www/LDN/
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/b1aa8941-69f2-419c-ab41-9668bf23aec5)

Instalamos el mysql-client con sudo apt install -y default-mysql-client.
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/3e691efb-723f-49d6-811c-54dae42c9a04)

la pagina lamp
![image](https://github.com/ArturoLucero28/Pila-Lamp-en-dos-niveles/assets/146435794/2a51a9bd-707d-4576-bc50-5b970bbdcec3)


