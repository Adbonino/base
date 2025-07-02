…or create a new repository on the command line
```
echo "# base" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Adbonino/base.git
git push -u origin main
```
…or push an existing repository from the command line
```
git remote add origin https://github.com/Adbonino/base.git
git branch -M main
git push -u origin main
```

|Nro|Tarea|Descripción|Observacion|
|---|---|---|---|
|1|Instalación física|Instalar fisicamente 4 SAN switches G720, los equipos ya fueron instalados en los racks indicados por el cliente|Queda pendiente cableado eléctrico y red|
|2|Relevar la configuración actual|Realizar relevamiento de las configuraciones existentes es las Fabrics A y B||
|3|Presentar informe para zonas actuales para filtrado|El cliente recibe un listado de las zonas con observaciones encontradas y da su aprobación a las zonas que deberán ser migradas a la nueva configuraci+on como también las que serán descartadas. En esta sección también el cliente define nomenclatura a utilizar para sus configuraciones de zonas||
|4|Elaboracion de playbooks de ansible|Elaborar playbooks de ansible para la creacion de las configuraciones necesrias en los nuevos equipos como también para el uso en tareas comunes de operación con SAN swithces||
|5|Implementacion de configuraciones|Preparar los Weitces SAN para la configuración de funcionamiento en fabrics y crear las configuraciones requeridas segpun lo apribado por el cliente. Estas configuraciones se crearán vía ansible||
|6|Migrar conexiones del switch SAN actual hacia los nuevos equipos|Las conexiones de fibra que van al switch actual brocade6510 & G610 se migrara hacia los nuevos equoipos|Esto se hará en ventana y la configuración de zonas ya deberá estar cargada en los equipos según lo mensionado en el punto 5|
|7|Validaciones|Validar la operatividad de los equipos luego del camino de conexiones al SAN G702||
|8|Migracion fisica al sitio contingencia|Se deberá llevar el equipo desmontado en matriz al sitio de contingencia|Esto se hará en ventana. Para este punto desde el banco deberán prever las conexiones inter-sitio qeu pasa por el multiplexor para conectar el SAN G720 con el G610 que se instalará en contingencia|
|9|Validaciones|Validar la conexión de los swithces entre sitios y opratividad de los equipos||