---
layout: page
title: Usuario
parent: Gestión de Canciones
permalink: canciones/usuario
nav_order: 1
---
## Gestión de canciones: _**Usuario**_
La plataforma admite varios tipos de acceso,  `Usuario`, `Editor` y `Administrador`. Estas aqui porque eres `Usuario` y quieres saber que puedes hacer con la plataforma. 

Con tu rol, puedes proponer canciones. Estas canciones no se podran usar para nada hasta que un `Editor` la apruebe.

### ¿Cómo propongo una canción?
Para proponer una canción tienes que estar logueado con tu usuario y dirigirte a esta seccion:

![usuario_cancion1](images/proposal_start.png)

La siguiente pantalla es una pantalla de verificación para intentar que no haya canciones repetidas en la plataforma debido a un fallo en la escritura del nombre. Nos pedira que busquemos la cancion que queremos meter. 

![song_check](images/song_check_not_exist.png)

Si la canción que queremos meter no esta en la lista, simplemente clicamos el boton azul grande de abajo. Si esta en la lista, tendremos que hablar con un editor para que la edite con su cuenta.

Se nos desplegaran todos los campos de una canción, primero los comunes y luego los especificos de tu version, de tu parroquia.

![proposal_common](images/proposal_common_part.png)

Campos genericos:
- **Nombre/Titulo***: El titulo de la canción
- **Autor***: El autor de la canción
- **Momento***: El momento dentro de la misa donde comunmente se canta esta cancion. Es simplemente orientativo, no bloquea esta cancion a este momento especifico.
- **Tiempo liturgico**: El tiempo liturgico.
- **Url de Youtube**: La url de youtube para poder aprender la cancion, si es que tiene.

![proposal_common](images/song_version_part.png)

Mas abajo vemos los campos especificos de la versión, y por tanto de tu parroquia:
- **Etiquetas**: Es un campo donde poner otros titulos o nombres por los que en tu parroquia conoceis a la canción. (_ej:_ _**"Amaos"**_ tambien se conoce como _**"Como el padre me amó"**_)
- **Cejilla**: La cejilla con que tocais esa canción en tu parroquia.
- **Ritmo**: El ritmo con el que la tocais. (_ej:_ 4x4)
- **Letra**: Este es el campo mas importante. Por defecto te viene rellando con un ejemplo para que veas como se meten los acordes y los estribillos.

  > _**¡Importante!**_ Si metes los acordes de esta manera, el sistema los reconocerá y se podrá cambiar de tono la canción.
  
  Para añadir los acordes es tan sencillo como meterlos dentro de la frase entre corchetes `[`,`]`. 
  > _**Nota**_ En la columna de ayuda de la derecha, puedes ver los acordes que pueden ser reconocidos. 
  
  Por ejemplo, para la canción "Vine a alabar a Dios", este codigo:

  ```
    {start_of_chorus}
    [SOL]Vine a ala[RE]bar a [mim]Dios,
    [DO]vine a ala[lam]bar a [RE]Dios.
    [SOL]Vine a ala[RE]bar su [mim]nombre,
    [DO]vine a ala[RE]bar a [SOL]Dios.[SOL7]
    {end_of_chorus}

    [DO]Él vino a mi [RE]vida
    en un [SOL]día muy espe[mim]cial,
    cam[DO]bió mi cora[RE]zón
    por un [SOL]nuevo cora[SOL7]zón
    y [DO]ésta es la ra[RE]zón
    por [SOL]la que digo [mim]que...
    [DO]vine a ala[RE]bar a [SOL]Dios[RE] (bis)
  ```
  ... se convertira en esto:

  ![vine_alabar_dios](images/vine_alabar_dios.PNG)

  Aunque conforme vayais escribiendo en el cuadro de texto, vereis que se va actualizando.

Una vez puesta la canción como quieres, simplemente hay que darle a **guardar**, en el boton azul, arriba de la pagina.

Si todo ba bien, te redirigirá a la pagina de la canción:

![proposal_done](images/proposal_done.PNG)

### ¿Cómo veo las propuestas y edito las mias?

Una vez hecha la propuesta, y hasta que un editor la apruebe, puedes editarla. Para ello ve a la seccion `Canciones > Propuestas` y clicka en el lapicero del final de la linea. Llegaras a la pagina de edicion (_apartado anterior_).

![proposals](images/proposal_edit_start.png)

