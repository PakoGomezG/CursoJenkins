def clima = 'Frio Invernal'
def ciudad = 'Vitoria-Gasteiz'
def habitantes = 250000
pipeline {
    agent any
    stages {
        stage('MostrarClima') {
            steps {
                echo "Clima: $clima"
            }
        }
        stage('MostrarHabitantes') {
            steps {
                echo "Poblacion actual: $habitantes"
            }
        }
        stage('MostrarPoblacionNeta') {
            steps {
				calcularPoblacionNeta(habitantes)
            }
        }
    }
}
def calcularPoblacionNeta(Integer poblacion) {
    def poblacionNeta = poblacion / 2
    echo "Poblacion neta: $poblacionNeta"
}
