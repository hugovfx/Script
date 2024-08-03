# Script
# Arriba las chivas

mostrar_menu(){
	sudo clear
	echo -e '\033[0;34mMenu \033[1;37m'
	echo '1.- Mostrar ruta actual'
	echo '2.- Dar permisos a u archivo'
	echo '0.- Salir del script'
}

mostrar_ruta(){
	sudo clear
	echo -e '\033[0;34mRuta actual \033[1;37m'
        sudo pwd
	read -p 'Presiona Enter para continuar...'
}

dar_permisos(){
	sudo clear
	echo -e '\033[0;34mDar permisos a un archivo \033[1;37m'
	read -p 'Ingrese la ruta del archivo: ' ruta
	read -p 'Ingrese los permisos: ' permisos
	sudo chmod $permisos $ruta
}

while true; do
	mostrar_menu
	read -p 'Seleccionar opcion: ' opcion
	case $opcion in
	    1)
		mostrar_ruta
		;;
	    2)
		dar_permisos
		;;
	    0)
		echo 'saliendo...'
		exit 0
		;;
	    *)
		sudo clear
		echo 'Opcion invalida . Por favor, selecciona una opcion valida.'
		read -p 'Presiona Enter para continuar...'
		;;
	esac
done



