pipeline{
    agent any
    stages{
        stage('Instalando Dependências'){
            steps {
                echo 'Baixando versão 14 do node'
                sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash'
                sh 'source ~/.bashrc'
                sh 'nvm install 14'

            }
        }

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