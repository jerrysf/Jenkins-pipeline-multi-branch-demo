pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
                bat 'echo make' 
            }
        }
        
        stage('Static Analysis'){
            parallel {
                stage('Sonar analysis'){
                    steps {
                        bat 'echo test in win'
                    }
                }
                stage('Blackduck analysis'){
                    steps {
                        bat 'echo test in lix'
                    }
                }
                stage('Klocwork analysis'){
                    steps {
                        bat 'echo test in lix'
                    }
                }
                }
        }
        
        stage('Test'){
            parallel {
                stage('Test in Windows'){
                
                stages {
                    stage('Pre Test in Windows'){
                        steps {
                        bat 'echo'
                        }
                    }
                    stage('Start Test in Windows'){
                    steps {
                        bat 'echo test in win'
                    }
                    }
                }
                }
                stage('Test in Linux'){
                    steps {
                        bat 'echo test in lix'
                    }
                }
                }
        }
        
        stage('Deploy to Dev') {
            steps {
                bat 'echo make publish'
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                bat 'echo make publish'
            }
        }
        
        stage('Deploy to Prod') {
            steps {
                bat 'echo make publish'
            }
        }
    }
}
