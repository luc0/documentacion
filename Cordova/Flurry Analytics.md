(Info: https://github.com/jfpsf/flurry-phonegap-plugin)

# Flurry ( analytics ):

### 1. Instalar

- Instalar: El plugin automaticamente agrega una referencia a google play services y android v4 support lib:
  cordova plugin add https://github.com/jfpsf/flurry-phonegap-plugin.git
  (si tira error clonarlo localmente y agregarlo localmente apuntando a la carpeta)

- Debería instalar flurry antes del Admob, no es necesario, pero es mejor seguir estos pasos.

- Copiar el archivo "FlurryAnalytics-5.5.0.jar" (de alguno de mis proyectos) (creo que se consigue en la pagina de flurry tambien) copiarlo a: "platforms\android\libs"

- Listo!. Cuando instale Admob me va a saltar un error ver solucion: https://github.com/luc0/documentacion/blob/master/Cordova/Admob.md


  (Si da error. Fijarse que no haya un google play services instalado, sino desintalarlo. puede haber uno en plugins y otro en android, depende.)



### 2. Iniciar
- flurry.startSession('SGPM7RH64NHH2JCZXQR4', flurrySuccess, flurryError);


### 3. Modo de uso

  //Eventos
  window.plugins.flurry.logEvent(event, successCallback, failureCallback)

	//Eventos con parametros (max 10)
	// los parametros se escriben asi: {id:"4", price: "471", location: "New York"}
	window.plugins.flurry.logEventWithParameters(event, parameters, successCallback, failureCallback);

	// Eventos con contador de tiempo
	// timed tiene que ser true o false.. que despues lo convierte en 'Yes' o 'No' porque es objetive-c
	window.plugins.flurry.logTimedEvent(event, timed, successCallback, failureCallback)
	window.plugins.flurry.endTimedEvent(event, successCallback, failureCallback)

	// Eventos con parametros y contador de tiempo
  // timed tiene que ser true o false.. que despues lo convierte en 'Yes' o 'No' porque es objetive-c
	window.plugins.flurry.logTimedEventWithParameters(event, parameters, timed, successCallback, failureCallback)
	window.plugins.flurry.endTimedEventWithParameters(event, parameters, successCallback, failureCallback)

	// Errores que quiera loguear
	window.plugins.flurry.logError(errorID, message, successCallback, failureCallback)

	// Visitas en pagina
	window.plugins.flurry.logPageView(successCallback, failureCallback)
