pipeline{
    agent any
    stages{
        stage('Instalando Dependências'){
            steps {
                echo 'Instalando dependências'
                sh 'yarn'
            }
        }

        stage('Build'){
            steps {
                echo 'Buildando projeto'
                sh 'yarn build'
            }
        }
        
        stage('Run'){
            steps {
                echo 'Rodando projeto'
                sh 'yarn dev'
            }
        }

    }
}