pipeline{
    

    agent any
    stages{
        stage('Curl'){
            steps {
                echo 'Baixando versão 14 do node'
                sh 'curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -'
                sh 'sudo apt-get install -y nodejs'
            }
        }
        

        stage('Atualizando NPM'){
            steps {
                echo 'Baixando versão 14 do node'
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