## Repositorio remoto

Un repositorio remoto en Git es una versión del repositorio de Git que está alojada en un servidor diferente al del repositorio local. Los repositorios remotos son comúnmente utilizados para colaborar con otros desarrolladores, mantener copias de seguridad del código y desplegar el código a servidores de producción.

- Agregar un repositorio remoto:
```console
git remote add origin https://github.com/usuario/repositorio.git
```

- Cambiar url del repositorio remoto en caso de ser necesario:
```console
git remote set-url origin https://github.com/usuario/repositorio.git
```