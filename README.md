## - ¿Qué comando utilizaste en el paso 11? ¿Porqué?

	git reset --hard HEAD~1
	
*se utiliza reset para deshacer commits y con el atributo de --hard le dice que no mantenga los cambios del working copy*

##- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

	git reflog
	git reset --hard 751dd73
*utilicé el comando reflog para localizar el identificador del commit que queremos rehacer de nuevo, después se usa el comando reset --hard "identificador" para rehacer ese commit, y reset nos permite mantenernos en la misma rama ya que mueve el apuntador de la rama.*

##- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
*No causo ningun conflico porque la rama a ser absorbida no tenia caracteristicas o cambios nuevos que la rama styled, styled ya contenía los commits de master y por eso el resultado fue "Already up-to-date", por tanto styled nunca agregó cambios de master y por ende se encuentra actualizada.*

##- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
*Si, porque el archivo git-nuestro.md en cada una de las ramas styled y htmlify tiene diferentes modificaciones en las mismas lineas provocando asi conflictos ya que git no piensa por nosotros si elegir el styled ó htmlify, por tanto git solo avisa e indica que cambios son de que cosa para que el usuario decida que elegir.*

##- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
*No, porque en la rama situada("master") sólo absorbió ó obtuvo los cambios nuevos de la rama "styled", y como "master" no tenía cambios nuevos diferentes a los que contiene la rama "styled" por eso no causó conflicto.*
##- ¿Qué comando o comandos utilizaste en el paso 25?
	git log --graph
##- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
*Si, porque "title" es una ramificacion de "master", y los cambios nuevos de "title" pueden ser absorbidos por "master", git en fast-forward lo que hace es mover el puntero de "master" al de "title" y asi de ésta forma absorbe sus commits.*
##- ¿Qué comando o comandos utilizaste en el paso 27?
	git reset HEAD~1

*para deshacer el merge sin perder los cambios agregados de "title"*
##- ¿Qué comando o comandos utilizaste en el paso 28?
	git checkout -- git-nuestro.md
	git status
*para descargar los cambios*
	
*para validar que no hay cambios nuevos en el working copy*
##- ¿Qué comando o comandos utilizaste en el paso 29?
	git branch -D title
*elimina la rama "tittle"*
	git branch
*para validar que se haya eliminado la rama "title"*
##- ¿Qué comando o comandos utilizaste en el paso 30?
	git reflog
	git reset --hard 3c723ae
	git log --graph
*para buscar el identificador del merge borrado en su bitácora de git.*
	
*se mueve el puntero de master al identificador del merge deshecho pero que existe en git.*
	
*por último para validar que en el diagrama del log ya existe de nuevo el merge Rehecho.*
##- ¿Qué comando o comandos usaste en el paso 32?
	git reflog
	git checkout f545e81
*para buscar el identificador del commit inicial.*

*para ir al commit iniciar moviendo el puntero HEAD.*
##- ¿Qué comando o comandos usaste en el punto 33?
	git reflog
	git checkout 8c36532
*para buscar el identificador del commit cuando se crea el titulo del poema.*

*se mueve al commit para crear el titulo del poema.*

###Image:
git reflog final:
 
![alt text](http://i1122.photobucket.com/albums/l540/Lapicher_j/Captura%20de%20pantalla%202016-06-19%20a%20las%201.38.03.png)
