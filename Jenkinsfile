pipeline{
    agent any
    stages{
        stage('Instalando Dependências'){
            steps {
                echo 'Indo até o diretório frontend'
                sh 'cd frontend'

                echo 'Instalando dependências'
                sh 'yarn install'

                sh 'ls'
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
                sh 'yarn start'
            }
        }

    }
}