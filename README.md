# grub-themes

Pasos para aplicar el tema de grub (Lo aplique en Debian, aun no pruebo las demas distros pero creo que te deberia de ir bien)

1- Clona el repositorio

git clone https://github.com/MaxPepsis/grub-themes.git

2- Crea el directorio para guardar temas de grub (recomendado, pero si lo tienes salta este paso)

sudo mkdir -p /boot/grub/themes/

3- Mueve el tema a directorio recien creado (o donde tu indiques)

sudo mv ~/grub-themes/midnight-anime /boot/grub/themes/

4- Entra a la configuración de grub

sudo nano /etc/default/grub

5- Añade o edita esta línea en la configuración

GRUB_THEME="/boot/grub/themes/midnight-anime/theme.txt"

6- Guarda el archivo y aplicas los cambios

Si usas el editor nano, usa la combinación Ctrl+O para guardar los cambios y posteriormente Ctrl+X para salir de editor

7- Aplica el tema

sudo update-grub

Y listo! Para que puedas echarle un vistazo a tu nuevo tema, tendrias que reiniciar tu equipo o mas bien usando el comando

sudo reboot

Y si el grub arranca rápido y no te da tiempo de ver te recomiendo aumentar los segundos de temporizador en /etc/default/grub
esos 60 son segundos, si tu quieres poner 4 minutos en el temporizador de grub tendrias que convertir minutos a segundos, que en 4 minutos serian 240

GRUB_TIMEOUT=60

En 4 minutos serian

GRUB_TIMEOUT=240

Gracias por ver!
