#[ NO LO RECOMIENDO ]
# Acra + Cloudant ( bug reporter ):

### 1. Seguir estos pasos para cloudant:
http://www.toptal.com/android/automated-android-crash-reports-with-acra-and-cloudant

(Acordarse de generar los keys y reemplazarlos en el comando del siguiente paso)

### 2. Instalar plugin cordova de Acra
    cordova plugin add https://github.com/sawatani/Cordova-plugin-acra.git --variable TOAST_TEXT='Error' --variable URL="https://luco.cloudant.com/acra-secuence/_design/acra-storage/_update/report" --variable USERNAME="ceseriescroathestabsects" --variable PASSWORD="JhVDcAd4KQvdta4gPvxTsTtX"

### 3. Configurar plugin instalado Acra:

agregar al tag aplication del manifest:
    android:name="org.fathens.cordova.acra.AcraApplication"

### 4. Enviar error a la DB desde js:
plugin.acra.handleSilentException('( ERROR ) - ')

### 5. Ver errores graficamente:
https://luco.cloudant.com/acralyzer/_design/acralyzer/index.html#/dashboard/secuence
