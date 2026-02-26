Componente mm-textfield
Resumen
Permite al usuario ver y elegir fechas de un widget de calendario o escribir manualmente la fecha en el campo de texto, como lo indica el texto en placeholder (día/mes/año).
  selector
 <mm-datepicker>

Propiedades
Nombre
Tipo
Descripción
label	String	Establece el label de componente
value	String | object New Date()	Establece la fecha/hora por defecto. Si el atributo date-range esta presente separar las fechas con guión. Ej: "31/07/2020 - 31/08/2020" o dentro de un Array.
disabled	boolean	Atributo que deshabilita el input
error-message	boolean	Muestra el mensaje de error
mandatory	boolean	Establece si es obligatorio completar la información
cancel	boolean	Establece la opción de cancelar
close-on-outside	boolean	Activa el cierre clickando fuera de él
max-results	number	Número máximo de resultados
helper-icon	string	Muestra el icono de información con tooltip
helper-info	string	Muestra el texto de ayuda
hidden-input	boolean	Añade un input type="hidden" para poder pasarle un value diferente al input que se muestra al usuario. Para acceder al input oculto y poder modificarle el valor, hay que utilizar el id="hiddenInput".
regex	string	Bloquea la entrada de caracteres no numéricos
Clases Fecha
Nombre
Valor
size-s	120px
size-m	200px
Clases Fecha (Rango)
Nombre
Valor
size-m	200px
size-l	280px
Clases Hora
Nombre
Valor
size-s	120px
Atributos Data-*
Con el atributo data-week obtenemos el número de la semana seleccionado. Podemos acceder a traves de la propiedad dataset.value Solo funciona con Fecha simple.

Componente mm-datepicker
Propiedades
Nombre
Tipo
Descripción
type	String	Establece el tipo de componente
disabled	boolean	Atributo que deshabilita el input
placeholder	string	Añade el texto provisional dentro del input
date-range	boolean	Establece el componente para seleccionar un rango de fechas (solo tipo date)
options	Object	Establece opciones custom de Flatpickr
min-date	string	Establece fecha mínima. Formato : "dd/mm/aaaa"
max-date	string	Establece fecha máxima. Formato : "dd/mm/aaaa"
today-selector	boolean	Asigna un botón de selección de día actual
open	boolean	Abre el calendario inicialmente
open-inline	boolean	Permite despleglar el componente
allow-month-select	boolean	Habilita la selección por mes. Solo funciona en Fecha simple
allow-week-select	boolean	Habilita la selección por semana. Solo funciona en Fecha simple
weekSelected	read-only	Devuelve el número de la semana que se ha seleccionado. Solo funciona en Fecha simple
blurCallback	function	Función callback que se lanza dentro del evento onblur del input. Esto es debido a que el evento blur se cancela debido a las multiples llamadas al evento onchange en la librería que se utiliza. Se le pasa como parámetro el evento.
path	string	Establece atributo 'name' al elemento input nativo
id-input	string	Establece atributo 'id' al elemento input nativo
Métodos públicos
Nombre
Parámetro
Descripción
setValue(value)	value: string | number | Date	Establece el valor de la fecha seleccionada en el datepicker, actualizando tanto la instancia del calendario como el campo de entrada de texto asociado.
openDatepicker()	-	Abre el calendario datepicker para permitir la selección de fecha.
getDate()	-	Devuelve la fecha seleccionada. En modo rango devuelve un array, en modo selección de mes devuelve formato localizado, de lo contrario devuelve el valor del input.
setDate(date)	date: string	Establece una fecha específica en formato "dd/mm/aaaa" en el input del datepicker.
clearDate()	-	Limpia completamente el valor del datepicker, reseteando tanto el calendario como el input.
getMonthDate()	-	Devuelve la fecha del mes seleccionado. Solo funciona cuando la opción allow-month-select está habilitada.
Eventos
Nombre
Descripción
change	Emitido al cambiar el valor de los datpicker que no sean de tipo time
timeChange	Emitido en el onblur de los datepickers de tipo time
Buenas prácticas en Angular
Las siguientes recomendaciones aplican cuando mm-datepicker se usa en Angular (Reactive Forms o Template-driven). El componente emite eventos nativos input y sincroniza su value , por lo que Angular puede enlazarlo como si fuera un form control estándar.

Requisitos previos
Colocar el formControlName en mm-datepicker (no en mm-textfield ).
Si no tienes un ControlValueAccessor propio, añade el atributo ngDefaultControl al mm-datepicker .
Si usas un formulario y usas ngDefaultControl añade (ngSubmit)="onSubmitSimple()" al formulario.
