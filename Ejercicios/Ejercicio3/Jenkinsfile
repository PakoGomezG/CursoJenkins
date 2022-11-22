def top5movies = ['El club de la lucha','Pulp Fiction','Snatch','El lobo de Wall Street','La vida de Brian']
def comidaFav = 'Pizza'
def signoZodiaco = 'Piscis'
def puestoActual = 'Tecnico Sistemas'
def salBruto = 1500
pipeline {
    agent any
    stages {
        stage('MostrarPeliculas') {
            steps {
                script {
    				echo "Top 5 movies:"
    				for (item in top5movies) {
    					echo " - $item"
    				}
                }
            }
        }
        stage('MostrarComidaFax') {
            steps {
                echo "Comida favorita: $comidaFav"
            }
        }
        stage('MostrarSignoZod') {
            steps {
				echo "Signo del zodiaco: $signoZodiaco"
            }
        }
        stage('MostrarPuesto') {
            steps {
				echo "Puesto actual: $puestoActual"
            }
        }
        stage('MostrarSalario') {
            steps {
				echo "Salario bruto: $salBruto"
                script {
				    calcularSalarioNeto(salBruto)
                }
            }
        }
    }
}
def calcularSalarioNeto(Integer salario) {
    script {
        def salNeto = 0
    	if (salario > 1000) {
    		salNeto = salario * 0.8
    	}
    	else {
    		salNeto = salario
    	}
        echo "Salario neto: $salNeto"
    }
}