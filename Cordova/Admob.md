(Info: https://github.com/floatinghotpot/cordova-admob-pro)

# Admob ( Ads ):

### 1. Instalar

  cordova plugin add cordova-plugin-admobpro

### 2. Copiar y pegar archivo Admob.js de algun proyecto mio.

### 3. Configurar key si es necesario.

### 4. Comentar Linea

  Va a dar error el "com.google.android.gms" si quiero compilar. Para arreglarlo comentar esta linea "#cordova.system.library.1=com.google.android.gms:play-services-ads:+" en "\platforms\android\project.properties"

( Ver proyecto github por si cambio algo )
