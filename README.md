# **Actividad I**  

### **¿Qué es GitHub?**  
GitHub es una plataforma en línea que permite almacenar, gestionar y compartir código fuente mediante el sistema de control de versiones Git. También facilita la colaboración entre desarrolladores en proyectos de código abierto o privados, proporcionando herramientas como control de versiones, seguimiento de problemas, integración continua y más.  

### **¿Cómo crear un repositorio en GitHub?**  
Para crear un repositorio en GitHub, sigue estos pasos:  
1. Inicia sesión en GitHub.  
2. Haz clic en el botón con el símbolo `+` en la esquina superior derecha y selecciona **"Nuevo repositorio"**.  
3. Completa los datos del repositorio:  
   - **Nombre del repositorio**  
   - **Descripción (opcional)**  
   - **Visibilidad** (público o privado)  
   - Opcionalmente, puedes agregar un archivo `README.md`, un `.gitignore` y una licencia.  
4. Haz clic en **"Crear repositorio"**.  

---

### **¿Cómo crear una rama en Git?**  
Para crear una nueva rama en Git, usa el siguiente comando:  
```bash
git branch [nombre-de-la-rama]
```  
Esto creará una nueva rama a partir de la rama actual.  

### **¿Cómo cambiar a una rama en Git?**  
Para cambiar de rama en Git, usa el siguiente comando:  
```bash
git checkout [nombre-de-la-rama]
```  
O con Git moderno (versión 2.23 en adelante):  
```bash
git switch [nombre-de-la-rama]
```  

### **¿Cómo fusionar ramas en Git?**  
Para fusionar una rama en Git, usa el siguiente comando desde la rama en la que quieres aplicar los cambios:  
```bash
git merge [nombre-de-la-rama]
```  
Si hay conflictos, Git te pedirá que los resuelvas antes de completar la fusión.  

---

### **¿Cómo crear un commit en Git?**  
Antes de hacer un commit, debes asegurarte de que hay cambios en tu código. Luego, sigue estos pasos:  
1. Añade los archivos modificados al área de preparación:  
   ```bash
   git add .
   ```  
2. Crea el commit con un mensaje descriptivo:  
   ```bash
   git commit -m "Descripción del cambio"
   ```  

### **¿Cómo enviar un commit a GitHub?**  
Para enviar los cambios al repositorio remoto en GitHub:  
```bash
git push origin [nombre-de-la-rama]
```  
Si es la primera vez que haces push a una nueva rama, usa:  
```bash
git push --set-upstream origin [nombre-de-la-rama]
```  
Antes de hacer `push`, asegúrate de haber configurado la conexión con el repositorio remoto.  

---

### **¿Qué es un repositorio remoto?**  
Un repositorio remoto es una versión del repositorio almacenada en un servidor en línea, como GitHub, GitLab o Bitbucket. Permite a múltiples desarrolladores trabajar en el mismo código desde diferentes ubicaciones.  

### **¿Cómo agregar un repositorio remoto a Git?**  
Para enlazar un repositorio local con un repositorio remoto en GitHub:  
```bash
git remote add origin [URL-del-repositorio]
```  

### **¿Cómo empujar cambios a un repositorio remoto?**  
Para subir los cambios desde tu repositorio local al remoto:  
```bash
git push origin [nombre-de-la-rama]
```  

### **¿Cómo traer cambios de un repositorio remoto?**  
Para descargar los últimos cambios de la rama remota y fusionarlos con la rama actual:  
```bash
git pull origin [nombre-de-la-rama]
```  

---

### **¿Qué es un fork de repositorio?**  
Un fork es una copia de un repositorio en tu cuenta de GitHub que te permite hacer cambios sin afectar el repositorio original. Es útil para colaborar en proyectos de código abierto.  

### **¿Cómo crear un fork de un repositorio?**  
1. Ve al repositorio en GitHub.  
2. Haz clic en el botón **"Fork"** en la esquina superior derecha.  
3. Elige tu cuenta o una organización donde deseas crear el fork.  

### **¿Cómo enviar una solicitud de extracción (pull request) a un repositorio?**  
1. Desde tu fork, crea una nueva rama y haz los cambios deseados.  
2. Sube los cambios (`git push`).  
3. En GitHub, ve a la pestaña **"Pull Requests"** del repositorio original.  
4. Haz clic en **"New pull request"**.  
5. Selecciona la rama de tu fork y la rama del repositorio original donde quieres fusionar los cambios.  
6. Escribe una descripción y haz clic en **"Create pull request"**.  

### **¿Cómo aceptar una solicitud de extracción?**  
El propietario del repositorio revisa los cambios, resuelve posibles conflictos y puede aceptar la solicitud haciendo clic en **"Merge pull request"**.  

---

### **¿Qué es una etiqueta en Git?**  
Una etiqueta (`tag`) en Git se usa para marcar versiones específicas de un código. Se usa comúnmente en lanzamientos de software.  

### **¿Cómo crear una etiqueta en Git?**  
Para crear una etiqueta, usa el siguiente comando:  
```bash
git tag -a v1.0.0 -m "Versión 1.0.0"
```  
Para enviar la etiqueta al repositorio remoto:  
```bash
git push origin v1.0.0
```  

---

### **¿Qué es el historial de Git?**  
El historial de Git muestra todos los commits realizados en el proyecto.  

### **¿Cómo ver el historial de Git?**  
Para ver el historial de commits:  
```bash
git log
```  
Si deseas un historial más compacto:  
```bash
git log --oneline
```  

### **¿Cómo buscar en el historial de Git?**  
Para buscar un commit con una palabra clave en el mensaje de commit:  
```bash
git log --grep="palabra-clave"
```  

### **¿Cómo borrar el historial de Git?**  
Git no permite eliminar el historial de commits fácilmente, pero puedes reiniciar un repositorio con:  
```bash
rm -rf .git
git init
```  
⚠️ **Esto eliminará todo el historial, úsalo con precaución.**  

---

### **¿Qué es un repositorio privado en GitHub?**  
Un repositorio privado es un repositorio en GitHub que solo puede ser accedido por los usuarios autorizados.  

### **¿Cómo crear un repositorio privado en GitHub?**  
1. Sigue los mismos pasos para crear un repositorio.  
2. En la sección de visibilidad, selecciona **"Privado"**.  

### **¿Cómo invitar a alguien a un repositorio privado en GitHub?**  
1. Ve a la configuración del repositorio (**Settings**).  
2. En la sección **"Manage access"**, haz clic en **"Invite collaborators"**.  
3. Ingresa el nombre de usuario o correo del colaborador y envía la invitación.  

---

### **¿Qué es un repositorio público en GitHub?**  
Un repositorio público es accesible por cualquier persona en GitHub. Se usa generalmente para proyectos de código abierto.  

### **¿Cómo crear un repositorio público en GitHub?**  
1. Sigue los mismos pasos para crear un repositorio.  
2. En la sección de visibilidad, selecciona **"Público"**.  

### **¿Cómo compartir un repositorio público en GitHub?**  
Para compartirlo, simplemente proporciona la URL del repositorio:  
```text
https://github.com/usuario/repositorio
```  

