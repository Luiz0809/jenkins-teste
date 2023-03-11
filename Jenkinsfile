pipeline{
    

    agent any
    stages{
        stage('Curl'){
            steps {
                echo 'Baixando versão 14 do node'
                sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | source ~/.bashrc'
            }
        }
        

        stage('Atualizando Node'){
            steps {
                echo 'Baixando versão 14 do node'
                sh 'nvm install 14'
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