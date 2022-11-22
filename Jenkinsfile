// Plugin utilizado build user vars plugin Versión 1.9
def date = new Date()
def java_path = "C:\\temp\\jdk-17.0.5\\bin"
pipeline {
    agent any
    stages {
        stage('MostrarInfo') {
            steps {
                wrap([$class: 'BuildUser']) {
                    script {
                        USER = "${BUILD_USER}"
                        USER_ID = "${BUILD_USER_ID}"
                    }
                }
                echo "Usuario: ${USER}"
                echo "Usuario ID: ${USER_ID}"
                mostrarVersionJava(java_path)
            }
        }
    }
}
def mostrarVersionJava(String java_path) {
    //bat '"$java_path" -version'
    bat """
        "${java_path}\\java.exe" -version
    """
}
