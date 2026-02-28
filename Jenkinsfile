pipeline{
    agent any

    environment{
        VERCEL_TOKEN = credentials('VERCEL_TOKEN')
    }

    stages{
        stage('INSTALL DEPENDENCIES'){
            steps{
                bat 'npm install'
            }
        }
        stage('TEST'){
            steps{
                echo 'Skipping tests...'
            }
        }
        stage('BUILD'){
            steps{
                bat 'npm run build'
            }
        }
        stage('DEPLOY'){
            steps{
                bat 'npx vercel --prod --yes --token = %VERCEL_TOKEN%'
            }
        }
    }
}