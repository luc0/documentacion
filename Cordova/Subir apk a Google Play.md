
# CORDOVA 5.1.1: Generar APK (signed & aligned) como Google Play dicta:

## 1. OBTENER UNA PRIVATE KEY
		en consola dentro del proyecto (dentro de platforms/android) poner esto y rellenar (NameOfAplication y YourAlias) :
		`keytool -genkey -v -keystore NameOfAplication.keystore -alias YourAlias -keyalg RSA -keysize 2048 -validity 10000`

		[ mas info: (http://developer.android.com/tools/publishing/app-signing.html#cert) -> en la parte de "Signing Your App Manually" ]
		va a generar la private key, en donde este parado, deberia ser en platforms/android

		(OJO! ultimo paso por las dudas poner el mismo password, es decir apretar enter sin escribir nada)

## 2. CONFIGURACION DE LAS KEYS Y ALIAS
		Crear archivo release-signing.properties en platforms/android/ con el path al keystore y el alias name (segun lo configurado anteriormente):
		`storeFile=/ritmoApp.keystore
		storeType=jks
		keyAlias=test`

		### Opcional (para que no te pregunte password por cada build):
		`keyPassword=your-key-password
		storePassword=your-store-password`

## 3. ir al proyecto y ejecutar (esto supuestamente ademas pone la firma digital en base a la config anterior):
		`cordova build android --release`

## 4. Verificar si la app esta firmada (se puede saltear)
		`jarsigner -verify -verbose -certs android-release.apk`

## 5. Zipalign es obligatorio por google para optimizar la apk (primero el apk unaligned y el segundo es el output):
		el comando se puede ejecutar desde: d:program files/android/android-sdk/build-tools/22.0.1 (ahi esta el zipalign.exe), desde ahi ejecutar esto en consola:
		`zipalign -v 4 D:/xampp/htdocs/proyectos/phaser_cordova/ritmo/platforms/android/build/outputs/apk/android-release-unsigned.apk D:/xampp/htdocs/proyectos/phaser_cordova/ritmo/platforms/android/build/outputs/apk/myapp.apk`


## 6. subir archivo generado a google play!!
