Add Plugin -> falla:
  1- Hacer un git clon
  2- Hacer el Add plugin localmente, apuntando a la carpeta.


Emulate android -> no pasa nada, tampoco da error:
	1- para poder emularlo en el celu modificar estos archivos:
			A- phaser_cordova/ritmo/platforms/android/cordova/lib/device.js (linea 101):
				var cmd = 'adb -s ' + resolvedTarget.target + ' install -r "' + apk_path + '"';
			B- phaser_cordova/ritmo/platforms/android/cordova/lib/emulator.js (linea 311)
				return exec('adb -s ' + resolvedTarget.target + ' install -r "' + apk_path + '"', os.tmpdir())
			(es decir en ambos borrar el -d)
			(mas info: https://github.com/luc0/proyectos/commit/0e3a65449e8d47b6d12fdfc7f05a07ca0fc9a1f2)


Otros:
  Nuevo proyecto Cordova:
    -	puede llamarse com.empresa.nombrejuego
    - no puede llamarse com.test.test (hacerlo bien porque despues es mas lio)
