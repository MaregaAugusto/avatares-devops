pipeline {
    agent any
    
    stages {
        stage('Building images') {
            parallel {
                stage('Building api') {
                    steps {
                        script {
                            // Compile App1
                            dir('api') {
                                docker.build('xlmriosx/avatar-api')
                            }
                        }
                    }
                }
                
                stage('Building web') {
                    steps {
                        script {
                            // Compile App2
                            dir('web') {
                                docker.build('xlmriosx/avatar-web')
                            }
                        }
                    }
                }
            }
        }
        stage('Deploying apps') {
            parallel {
                stage('Building api') {
                    steps {
                        script {
                            // Compile App1
                            dir('api') {
                                docker.build('xlmriosx/avatar-api')
                            }
                        }
                    }
                }
                
                stage('Building web') {
                    steps {
                        script {
                            // Compile App2
                            dir('web') {
                                docker.build('xlmriosx/avatar-web')
                            }
                        }
                    }
                }
            }
        }
        
        
    }
    
    post {
        success {
            echo 'Both applications compiled successfully!'
        }
        failure {
            echo 'One or more applications failed to compile.'
        }
    }
}
