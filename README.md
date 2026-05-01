# **Cursos de git**
**Delia Maite Acosta Orellana**

## **Clase1**
## **¿Que es git?**
Es un Sistema de Control de Versiones Distribuido, este nos permite guadar archivos, registrar cambios en nuestros proyectos según las versiones que hagán. Lo podemos ver como el checkpoint de un videojuego al que puedes volver en cualquier momento.
## **¿Cómo nació Git?**

Git nace porque el creador de Linux, Linus Torvalds, recibía cambios o contribuciones de externos por correo electrónico. Él los revisaba y decidía si los usaba o no.

Este proceso era bastante agotador, por lo que Torvalds decidió utilizar BitKeeper. Sin embargo, debido a problemas con esta herramienta, dejaron de usarla.

Molesto por la situación, Torvalds se encerró durante aproximadamente dos semanas y creó Git.
## **¿Como instalar Git?**
### Pasos:
**1.** Ir a la pagina web de Git.

**2.** Seguir los pasos de instalacion segun tu Sistema Operativo.

**3.** Verificar la correcta instalacion usando el comando **git --version** en tu teminal.

## **Configuracion Básica**
**1. Nombre en tus comits**

Usamos el comando **git config --global user.name "tu nombre"** ayuda a identificar a quien hizo el commit.

**2. Correo en tus comits**

Usamos el comando **git config --global user.email "Tu correo electronico"**.

**3. Arreglar los saltos de linea**

Si eres usuario de Windows debes tener cuidado con tus saltos de linea ya que pueden causar errores a la hora de hacer un proyecto, el comando que usamos para arreglar este problema es **git config --global core.autocrlf true**.

## **Archivos importantes en un Repo**
Son 2:

**1. README.md**

Es nuestra carta de presentación, donde explicas tu proyecto. Una opcion para crear tu readme es desde la terminal usando el comando, **echo "NombreDelArchivo" README.md"** 

**2. .gitignore**

Este ignora archivos sensibles que tengas.

# **Clase 2**

# **States y Commits**
## **Estados de Git**

Son 3:

**1. Directorio de Trabajo (Modificador)**

Es la carpeta local donde trabajas tu codigo o proyecto, solo observa el progreso y cambios que realizas mas aun no los guarda.

Mientras Git los observa los cataloga en 2:

* **Untrackend.** No tiene una version previa de este archivo de este archivo, identifica que es nuevo y que no esta en el historial.
* **Modified.** Git ya lo tiene en su historial y se da cuenta que le realizaste cambios tanto al codigo o archivo como al nombre. 

**¿Para que nos sirve el comando git restore < archivo >?**

Nos srive para que el archivo modificado regrese a su estado original. debemos tener cuidado al usarlo ya que borra fisicamente los cambios realizados.

**¿Para que nos sirve el .gitignore?**

Es para que Git ignore completamente ese archivo. Para realizarlo debes entrar a nuestro archivo **.gitignore** que va a contener los archivo que no queremos subir, tambien funciona con directorios.

**2. Stage Area (Preparado)**

Es el areá de espera, es cuando seleccionas y mandas a git los cabios realizados para que pueda guardarlos y se cree ese punto de guardado para poder acceder a ellos despues.

Existen 2 formas de traer los archivos al Stage Area:
* **git add< archivo > .** Agrega el archivo < archivo > en especifico uno por uno.
* **git add .** Este agrega **todo** los cambios como lo modificado agregado o nuevo.

**¿Que pasa si subo algo por error?**

Utilizamos el comando  **git restore --staged nombreDelArchivo** este comando hace que ese archivo salga del Stage Area.

**3.Repositorio local (Confirmado)**

Es el historial de tus puntos de guardado, para acceder a ellos en cada punto cuando lo veas necesario. En este estado hacemos que todo lo que este en el stage area pasen al historial en un punto de guardado especifico. 

**¿Como creamos nuestro punto de guardado?**
 Usamos el comando **git commit -m "mensaje descirptivo de los cambios hechos"**.

 Para ver la informacion de algun punto de guardado usamos **git log** y si queremos la misma informacion pero mas resumida usamos **git log --online**.

**¿Como deshacemos el ultimo commit?**

Usamos el comando **git reset --soft HEAD~1**, debemos tener cuidado por que podemos causar algun problema si no usamos bien los parametros. 
## **Buenas Practicas**

**¿Cada cuanto debo hacer un commit?**

Lo mejor es hacer un commit cuando hagas un cambio pequeño pero que cambie la funcionalidad de tu codigo o agregues una nueva funcion. A esto le llamamos commits atomicos.

**¿Como escribir buenos commits?**
 Un buen comit cumple con lo siguiente:

 **1. Es descriptivo.** Describe a detalle el cambio que se realizo.
 **2. Usa verbos imperativos.** Este tipo de verbos se usan para dar ordenes y nos ayudaran mas con la descripcion de nuestro commit.**Ejemplo:** Add(Agrega), Change (Cambia),Fix(arreglar un bug), Remove(elimina).

 **2. No uses puntos suspensivos o punto final.**

 Esto es mas que todo por que es innecesario usar signos e puntuacion mas allá de las comas.

 **3. Usa como maximo 50 caracteres**

 Debes ser consiso y directo con los cambios realizados, si es que debs explicar mucho probablemente ya no sea un commit atomico y tengas muchos cambio.

 **4. Usa un prefijo para tus commits.**

 Para que nuestro commit sea mas legible y se entienda lo mejor posible los cambios realizados.

**5. Añade el contexto necesario en el cuerpo del commit**

Realizamos esto cuando tenemos una funcion tan grande que no podemos describirla en 50 carecters. Usamos el siguiente comando **git commit**, Con el cuerpo de **Titulo del commit + Descripcion**.
# **Clase 3**
## **GitHub y SSH**
## **¿Que es github?**
GitHub es una plataforma en la nube que funciona como una red social para desarrolladores. Permite alojar, gestionar y colaborar en proyectos utilizando Git.
## **Git vs GitHub**
Git y Github no son lo mismo a pesar de que GitHub usa Git, Sus diferencias son:
* **GitHub:**

1. Plataforma remota.
2. Almacena repositorios
3. Permite colaboración.
* **Git**
1. Sistema de control de versiones.
2. Maneja cambios y commits.
3. Funciona de forma local.
## **¿Como crear una cuenta en GitHub?**
Pasos:
1. Ir a github.com
2. Registrarse con email o Google.
3. Elegir un username único.

Debemos tomar en cuenta que el user name es **permanente** y es aconsejable no usar un correo institucional ya que puede acabar al terminar la carrera.
 ## **Diferencia entre nombre y usuario** 
 * **Username.** Se usa en GitHub, este te identifica en la plataforma.
 * **user.name** Se muestra en Git, este se muestra en tus commits como autor.
 ## **SSH vs HTTPS**
 * **HTTPS**
 1. Pide autenticación constantemente.
2. Puede requerir token.
3. Resulta incómodo.
* **SSH**
1. Usa una clave única (key).
2. No pide credenciales cada vez.
3. Más práctico y recomendado.

 Es muy recomendable usar siempre SSH.
 ## **Configuracion SSH**
Pasos:

**1.** Generamos la clave, En la teminal si es dede linux o desde git bash ejecutamos el comando **ssh-keygen -t ed25519 -C "tu_correo@gmail.com"**.

**2.** Optenemos la clave publica con el comando **cat ~/.ssh/id_ed25519.pub**

**3.**  **Para GitHub**
* Ir a Settings (Configuraciones).
* SSH and GPG Keys.
* New SSH Key.
* Pegamos la clave.
* Guardar.

**4.** Para verificar la conexión usamos el comando **ssh -T git@github.com** e.
## **¿Como crear un repositorio en GitHub?**
Seguimos los siguientes pasos:
1. Ir al apartado de repositorios
2. Clickeamos "New".
3. Le damos un nombre al repositorio.
4. Le damos una descripcion al repositorio (Opcional).
5. Click en ""Create Repository"".
## **Conectar un repositorio local de Git existente con uno en Github** 
Para empezar debemos haber ejecutado git init y tener por lo menos un commit.
 
 Usamos los siguientes comandos:

 **git remote add origin git@github.com:TuUser/TuRepo.git**

**git branch -M main**

**git push -u origin main**

¿Que hace cada uno?

**remote:** conexión al repositorio remoto.

**origin:** nombre por defecto del repositorio remoto.

**push:** subir cambios.

## **¿Como clonamos un repositorio en Git?**
 Usamos el comando **git clone “git@github.com:TuUser/TuRepo.git"**.

En caso de haber usado por error lo hiciste en https, lo corriges usando el comando **git clone “https://github.com/TuUser/TuRepo.git”**

Para cambiar el puntero de GitHub y no te pida autetificación cada vez, usamos el comando **git remote set-url origin “git@github.com:TuUser/TuRepo.git”**.

Verificamos la conexion remota con el comando **git remote -v**.
## **Cambios**
* **Subir cambios.**
Usamos el comando **git push origin < rama>**

El **push** es para empujar mis commits

* **Bajar o traer los cambios hechos.** Usamoa el comando **git pull origin < rama>**.

El **pull** para traer los commits del Servidor.
 
 (Buenas Auxi, comentarle que no pude subir mis apuntes de la clase 3 a tiempo debido a que estuve ayudando con el marco decorativo para la Flisol toda la tarde junto con la miembro Candy, por la mañana tuve 2 examenes, por la noche tuve clases y llegue directo para la clase de hoy, espero tenga comprension, muchas gracias.)

 # **Clase 4**
## **Remote, SSH multiple y Checkout**

## **Git Remote**
Git remote es el comando que nos permite gestionar las conexiones con repositorios remotos. Básicamente le indica a Git local a dónde debe enviar los cambios o de dónde debe obtenerlos.

**Comandos importantes:**

**git remote -v:** Muestra las URLs configuradas (para push y fetch).

**git remote add:** Vincula el repositorio local con uno remoto.

**git remote set-url:** Cambia la URL del repositorio remoto.

**Múltiples SSH**

Cuando se tienen varias cuentas de GitHub (por ejemplo personal y trabajo), no se puede usar una sola clave SSH para todas. Cada cuenta necesita su propia clave, como si cada puerta tuviera su propia llave.

Una clave SSH funciona como un “túnel” entre tu computadora y GitHub, por lo que cada cuenta debe tener su propio acceso independiente.
## **CONFIGURAR MULTIPLES SSH**
Seguimos los siguientes pasos:

**1. Crear una nueva clave.** Usamos el comando **ssh-keygen -t ed25519 -C "correo@gmail.com" -f ~/.ssh/id_nombre** .

**2. Crear archivo config:**
Se crea manualmente un archivo:
**~/.ssh/config**

**Conceptos importantes:**

* **Host:** Alias o nombre que le das a la conexión.
* **HostName:** Dirección real (siempre github.com).
* **User:** Siempre es git.
* **IdentityFile:** Ruta de la clave SSH que se usará.

**3. Verificar conexión.**
Usamos el comando **ssh -T git@github-miname**
## **Configuraciones locales**

Las configuraciones locales tienen prioridad sobre las globales y
estas solo funcionan para el repositorio en el que se aplican.
Para realizarlas se hace el mismo procedimiento que las globales pero sin el **flag --global** .

## **Git checkout**
Nos permite moverse entre distintos puntos de la historia del repositorio o entre ramas.

**Sirve para:**

* Ver versiones anteriores del código.
* Recuperar archivos.
* Probar cambios sin afectar la rama principal.
* Cambiar de rama.

## **El Estado "Detached HEAD"**

Cuando haces checkout a un commit específico, entras en estado detached HEAD.

Esto quiere decir que:
* No es una rama, puede ver lo que hacemos pero no tiene cuerpo.
* Podemos perder los cambios que hagas si no los guardas.
* Tenemos una vista al pasado.

## **Como ir y volver de un commit**

Ir a un commit anterior:

**git checkout < hash-antiguo>**

Ir al ultimo de la rama:

**git checkout < rama>**

Si hiciste algo aca (como un commit) desaparece
salvo que hagas:

**git checkout < hash_commit_creado>**

**git checkout -b rama_nueva**

## **Buenas prácticas con checkout**

* Hacer commit antes de moverse entre commits.
* No trabajar directamente en detached HEAD.
* Usarlo principalmente para inspeccionar el pasado.
* Si vas a trabajar, crear una rama.

Recordar que Git no te dejará cambiar de commit si tienes cambios sin guardar.

(Buenas noches Auxi, otra vez con una entrega tardia, hoy estuve gran parte del díá en la FLISOL desde las 8:30am a 13:40pm ayudando, por la tarde tuve que arreglar asuntos personales y tengo una clase en la noche con el ing Jhonatan de Calculo I, debido a ello llegue bastante tarde a casa y pude completar mis apuntes, espero pueda tomarme en cuenta y lamento que se haya repetido, gracias de antemano.)

## Aclaracion sobre mi trabajo 
Estimado Auxi:

Buenas noches. Quería comentarle una situación respecto a mi repositorio de Git.

He estado trabajando en el proyecto durante estos días, pero recién este lunes subí el repositorio a GitHub. Al revisarlo, noté que solo aparece un commit, lo cual me preocupó bastante, ya que no refleja el trabajo real realizadoni en general ni en ese commit debido a que el en ese commit hay mas de 2 lineas y se muestra solo 2.

Al verificar mi repositorio local, también observé que únicamente se registró ese commit. Intenté buscar en otras carpetas por si accidentalmente había trabajado en otro repositorio, pero no encontré ningún historial adicional en mi equipo, lo que significa que subi mal mis commits y por ello no se guardaron.

Esto me generó bastante frustración, ya que sí estuve avanzando progresivamente en el proyecto, incluso me comunique con ustede cuando iba a subir tarde mi commit por que estaba ayudando en la FLisol. Entiendo que esto puede generar dudas, pero quería explicarle lo sucedido antes de la entrega.

De igual manera, estoy adjuntando el repositorio con el contenido completo del trabajo realizado.

Lamento los inconvenientes y quedo atenta a cualquier observación.

Saludos,
Delia Acosta

# **Clase 5**
# **Ramas y GitFlow Básico**
## **¿Que son las ramas?**

Se puede decir que una rama es una bifurcación del código, es decir, una copia del estado actual desde un commit, que crea un nuevo camino para seguir trabajando sin afectar el original.

Las ramas nos ayudan en bastantes cosas como trabajar en equipo sin conflicto, probar nuevas funciones sin afectar a las que ya excisten.

## **¿Que es Git Branch?**
Es un comando **"git branch"** que nos permite gestionar las ramas, es el comando principal para poder trabajar con ramas, de este nacen comandos como:

**1. git branch.** Te permite hacer una lista de las ramas y muestra el estado actual del HEAD.

**2. git branch < rama>.** Crea una rama desde la rama en la que estamos posicionados.

**3. git branch -D < rama>.** Este nos permite borrar la rama.

**GIT CHECKOUT enfocado en ramas**

* **git checkout < rama>.** Este comando se ua para cambiar de rama, para usarlo no debemos tener nada en modified o staged.

* **git checkout -b < rama>.** Este comando crea la rama y te mueve a el directamente.

## **Checkout vs Switch**
Para empezar Git switch se creo porque checkout estaba “sobrecargado” y podía causar errores.

* **git checkout.** Nos sirve para demasiadas cosas (ramas, commits, archivos)
* **git switch.** Solo sirve para ramas, por lo que es más seguro usarlo.

## **GitFlow Básico**
GitFlow nos ayuda a trabajar de manera ordenada nuestras ramas, versiones y permite la adaptacion para que se puedan unir a nuestro proyecto nuevos coperadores.
## **¿Como funciona GitFlow?**
* **Main.** El propósito de esta
rama es contener el código
que se encuentra en
producción.
* **develop.** Esta rama es la rama de "pre-producción”, esta contiene las caracteristicas que se estan probandos pero que aun no fueron validadas del todo.
* **Ramas de apoyo.** Nos permitiran escribir codigo y pueden ser:
* **Feature.** Se usan para nuevas caracteristicas en el proyecto, se crean desde develop y una vez que acabas se unen nuevamente para posteriormente ser eliminadas en develop.
* **Release.** Usadas para la preparacion de una nueva version, son creadas en develop y se fucionan con develop o main.
* **Hotfix.** Las uasamos para trabajar cambios, imprevistos o corregir fallos en producción. Se craean desde la rama main por que desde una rama develop no se puede dar solución, se fuciona con main o develop.

# **Clase 6**
## **¿Qué es git merge?**

Nos permite unir dos ramas en una sola para que ambas tengan sus commits.

 **1. Merge normal (fast forward).**
* Une las ramas directamente.
* No deja registro visual de que hubo una rama.
* No sabes cuándo se hizo el merge.

**2. Merge --no-ff**

Usamos el comando **git merge --no-ff nombre_rama**
* Mantiene el historial.
* Crea un commit de merge, lo que nos deja un registro en el historial.
* Nos permite ver que hubo una rama.
* Es recomendable si se trabajara en equipo.
## **¿Qué es git fetch?**
Comando que nos permite ver si hay cambios en el repositorio remoto, solo ns deja ve si hay cambios no los trae.
## **¿Qué es git pull?**
Con el comando **git pull origin rama** traemos los cambios del repositorio remoto al local y actualiza la rama.
## **¿Qué es git push?**
**git push origin rama** Este nos permite subir los cambios del repo local (tu maquina) al repositorio remoto.
* **Primer push**
En caso de no ser nuestro repo usamos **git push -u origin rama** para crear la rama y no tener que solicitar permisos.
## **Flujo de trabajo**
* **Sin pull requests**

git checkout develop

git fetch

git pull origin develop

git checkout rama # Agregas -b *si estás creando la rama*

git merge develop *Solo si hubo cambios en develop*

*Trabajas en tu rama*

git push origin rama # *Agregas -u si es la primera vez que subes cambios al repositorio remoto*

git checkout develop

git fetch

git pull origin develop

git merge –no-ff rama

*Resuelves manualmente los archivos fallidos y sus conflictos*

git add .

git commit

* **Con pull requests**

La diferencia aca es que despues de todo ese flujo de trabajo, posteriormente de hacer el commit lo que debes hacer es:

**git branch -D rama**

**git push origin develop**

(Buenas noche auxi, para notificar el commit tardio se debe a que hoy me encontraba con 2 examenes y uno fue de noche por lo que no alcance a subirlo en hora, gracias por su comprension y una disculpa por los inconvenientes.)

# **Clase 7**
## **Pull Requests y trabajo en equipo**
 **Problema del trabajo sin Pull Request:**

* Dependemos demasiado del factor humano.
* Cualquiera puede hacer merge sin revisión.
* Puede haber errores, malas prácticas e incluso código malicioso.
## **¿Qué es un Pull Request?**
Un Pull Request es una solicitud para unir cambios de una rama a otra. Es como pedir permiso para poder subir nuestros cambios.
 
 Y nos permite:
* Revisar código antes de hacer merge.
* Dar feedback.
* Aprobar o rechazar cambios.
* Evitar errores o problemas en el repositorio.
# **Ventajas del Pull Request**
* Nos permite ver los cambios realizados antes de unirlos a nuestra rama main o developer.
* Aumenta la seguridad en tu proyecto.
* Reduce errores humanos.
* Nos obliga a trabajar realmente en equipo.
# **Configuracion importantes**

## **¿Donde hago mis configuarciones?**
En GitHub seguimos los siguientes pasos:
* Ir a tu repositorio.
* Ir a Settings.
* Entrar a Branches.
* Crear una nueva regla.

## **¿Para qué sirven estas reglas?**

* Evita merges sin revisión.
* Obligar el uso de Pull Request.
* Controla quién puede aprobar o aceptar cambios.
* Aumentar la seguridad del repositorio.

## **¿Donde aplicamos?**
 Aplicamos en las ramas **main** y **developer**
## **Reglas**
* **Regla principal**

**Pull Request despues antes del merge**

Esto para evitar errores y nos permita revisar si es que hay errores en nuestro codigo por que una vez mergeado se mezcla y si tiene errores ya afectamos al equipo.
* **Aprobaciones**
Debemos definir cuantas personas aprueban el PR, es recomendable la mitad del equipo mas uno, asi aseguramos que no solo una persona revise y desida todo y que el equipo revise y sea mas conciente de los cambios que se van a aceptar.
* **Regla de seguridad**
Si alguien aprueba el PR y luego tú haces cambios nuevos, GitHub elimina la aprobación anterior. Esto evita que algun integrante obtenga aprobacion y luego cambie el codigo sin revision.
* **Rechazo del pr**
Basta con que una persona so oponga a los cambios para que se rechace y se tenga que revisar y arreglar los cambios para subirlo.
# **Clase 8**
## **Git stash**
* El comando **git stash -m "mensaje"** ermite guardar temporalmente nuestros cambios en vez de hacer un commit, al hacerlo ya nos permite movernos de la rama en que estamos a cualquier otra.
* **git stash list** Nos deja ver lalista de cambios guardados.
* **git stash pop** Podemos traer nuestro cambios de regreso.
## **Git diff**
Este comando nos sirve para ver las diferencias en el codigo.
* **git diff --staged** Para ver los cambios en Stage.
* **git diff rama1 rama2** muestra las diferencias entre las ramas, lo eliminado y lo agregado.
## **Problemas al mergear**
Puede pasarnos que hacemos cambios de los archivo otra persona modifica el mismo archivo y aprueban primero su PR, en ese caso nuestro PR entra en conflicto, Git nos mostrara que hay **merge conflicts** y no te dejara hacer merge directamente.
## **¿Como solucionamos esto?**
Seguimos los siguientes pasos:

1. Debemos ir a develop y hacer los comandos:

**git checkout develop**

**git fetch**

**git pull origin develop**

2. debemos volver a nuestra rama
podemos usar: 
**git switch tu-rama**

**git checkout tu-rama**

3. Traer cambios de develop

Usamos **git merge develop**
4. Resolver conflictos manualmente si es que hay, es necesario por que tu codigo ya no esta actualizado con respecto al repo.