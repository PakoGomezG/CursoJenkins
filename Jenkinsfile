// Definimos path de git al no estar instalado
def git_path = "E:\\OneDrive - GFI\\Formacion\\PortableGit\\bin"
def hora = new Date().format("H").toInteger()

pipeline {
    agent any
    stages {
        stage('MostrarInfo') {
            steps {
                echo "Son las ${hora}"
                script {
                    if (hora > 0 && hora < 10) {
                        mostrarIpConfig()
                    }
                    else if (hora > 11 && hora < 15) {
                        mostrarGitVersion(git_path)
                    }
                    else if (hora > 16 && hora < 22) {
                        mostrarHora()
                    }
                    else {
                        echo "No se hace nada"
                    }
                }
            }
        }
    }
}
def mostrarGitVersion(String git_path) {
    bat """
        "${git_path}\\git.exe" --version
    """
}
def mostrarIpConfig() {
    bat "ipconfig /flushdns"
}
def mostrarHora() {
    bat "time /t"
}