leeMe.txt CapasRecordSet muestra la organización de una arquitectura por capas.
			Arquitectura ModeloVistaControlador
			Renderiza en lista o tabla un RecordSet de datos de una tabla en base de datos.

Contenido
	─Descripción.
	─Actualización.
	─Ejecución.
	─Glosario.
	─Referencias.   
		
Descripción.
	Muestra como organizar una aplicación web en carpeta-raiz para:
	
		/app: contiene conjunto de carpetas destinadas al soporte de la aplicación, sólo para el desarrollador.
		/public: contiene carpetas destinadas al consumo de datos para el usuario.
		.htacces archivo de texto; contiene script para ser interpretado por el servidor, el script conduce la
		ejecución de la navegación.

	Muestra como implementar y organizar en capetas una arquitectura por capas.
	
	CapasRecordSet
	  /app
		├─controladores
		├─libs
		├─modelos
		├─vistas
		├─.htaccess
		└─inicio.php
		
	Donde:
		
		  Carpeta 		    Capa						Descripción
		  
		controladores	 Controlador 		Contiene es la clase que toda clase debe tener un index.
											Gestiona el transito de datos entre el modelo principal y la vista principal.
		modelos			 Modelo				Gestiona una interfaz para el RecordSet.						
		vistas			 Vista				Renderiza en una UI del navegador, el RecorSet de la petición URL por omisión.
		
		/app							
		└─.htaccess							Configura/conduce el acceso/disponibilidad de recursos en directorio app/ 
		
		libs								Contiene archivos de soporte para la gestion de comunicacniones entre capas
		├─Contol.php						Define al controlador por omisión. Desgloza la url.						
		├─Controlador.php					Contiene a metodos para fabricar modelos y vistas 
		└─MySQLdb.php					    Contiene la interfaz para gestionar bd, retorna un RecordSet. 
		
		/app							
		└─inicio.php						Cargar clases en memoria de trabajo.
		
Actualización.

	Debe ser actualizada la ruta de ejecución del archivo public/.htaccess con:  
		
			/app/.htaccess 
                    └─ RewriteBase /ProyectoCb47/CapasRecordSet/public
				
	Debe ser creada la base de datos, en le gestor phpMyAdmin: 
	Base de datos:
			libreria 
	
	importar archivo:
	phpMyAdmin
	  ░ libreria
	  ├─nueva
	  └─libros.sql
			├─Columnas
			└─índices
			
	Actualizar path en el archivo: defineConstantes.php
	con la ruta de la: i) carpeta del proyecto, ii) aplicacion.
		/ProyectoCb47/CapasRecordSet/


Ejecución.

	Desde:
		xammp/htdocs/ProyectoCb47/CapasRecordSet/ 
	
	Abrir en barra de navegación:
	
		http://localhost/ProyectoCb47/CapasRecordSet/libros/
		
		
		
Glosario.

Recordset
		Un objeto Recordset representa los registros de una tabla base o los registros que son el resultado de ejecutar una consulta.
		
		
Referencias.

Objeto Recordset (DAO)
	Disponible en:https://learn.microsoft.com/es-es/office/client-developer/access/desktop-database-reference/recordset-object-dao
	Consultado: 21Julio24
	
Funcionalidad Básica de Apache	
	Disponible en:https://httpd.apache.org/docs/trunk/es/mod/core.html#options
	Consultado: 21Julio24.

ASCII table , ascii codes.	
	Disponible en:https://theasciicode.com.ar/#google_vignette	
	Consultado: 21Julio24.
	
Arce Anguiano Francisco Javier.
Crear un patrón MVC con php y MySQL.
	Disponible:https://www.udemy.com/course/crear-un-patron-mvc-con-php-y-mysql/
	Consultado:11julio24.
	
Guía para escribir documentos HTML Versión 1.8.21
Ejemplos de tablas
	Disponible:https://www.uv.es/jac/guia/tablaeje.htm
	Consultado: 21Julio24.