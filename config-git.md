#CONFIGURAR GIT Y DESCARGAR REPOSITORIO
primero validar que git en nuestro ordenador este conectado a nuestra cuenta de github
# Generar una clave SSH
ssh-keygen -t ed25519 -C "tuemail@example.com"

# Agregar la clave SSH al agente SSH
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# Copiar la clave SSH al portapapeles
cat ~/.ssh/id_ed25519.pub

# Navegar a la carpeta de tu proyecto
cd /ruta/a/tu/proyecto

# Inicializar un repositorio Git
git init

# Añadir archivos al área de preparación
git add .

# Realizar un commit
git commit -m "Descripción del primer commit"

# Agregar la URL del repositorio remoto con SSH
git remote add origin git@github.com:tuusuario/tu-repositorio.git

# Subir los cambios al repositorio remoto
git push -u origin master
