pipeline{
    agent any

    environment{
        VERCEL_TOKEN = credentials('VERCEL_TOKEN')
    }

    stages{
        stage('INSTALL DEPENDENCIES'){
            steps{
                sh 'npm install'
            }
        }

        stage('TEST'){
            steps{
                echo 'Skipping tests...'
            }
        }

        stage('BUILD'){
            steps{
                sh 'npm run build'
            }
        }

        stage('DEPLOY'){
            steps{
                sh 'npx vercel --prod --yes --token=$VERCEL_TOKEN'
            }
        }
    }
}