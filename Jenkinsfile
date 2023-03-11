pipeline{

    agent any
    stages{
        stage('Atualizando Node'){
            steps {
                echo 'Baixando versão 14 do node'
                sh 'sudo apt-get install -y nodejs'
                sh 'sudo apt-get install -y npm'
            }
        }

        stage('Instalando Dependências'){
            steps {
                echo 'Instalando dependências'
                sh 'yarn install'
            }
        }

        stage('Build'){
            steps {
                echo 'Buildando projeto'
                sh 'next build'
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