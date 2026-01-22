pipeline {
    agent any

    environment {
        APP_NAME   = "S-Mart-0.0.1-SNAPSHOT.jar"
        APP_DIR    = "/home/ubuntu/S_Mart-Ecommerce-Website-Java-Project"
        USER       = "ubuntu"
        PRIVATE_IP = "172.31.18.109"
        PORT       = "8080"
    }

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'my-new-branch',
                    url: 'https://github.com/Samruddhipansare2211/S_Mart-Ecommerce-Website-Java-Project.git'
            }
        }

        stage('Build & Test') {
            steps {
                sh 'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        // =============================
        // DEPLOY STAGE (COMMENTED)
        // =============================
        
stage('Deploy to EC2') {
    steps {
        sshagent(['ec2-ssh-key']) {
            sh '''
            ssh -o StrictHostKeyChecking=no ubuntu@172.31.18.109 << EOF
              pkill -f S-Mart-0.0.1-SNAPSHOT.jar || true
              mkdir -p /home/ubuntu/S_Mart-Ecommerce-Website-Java-Project
              exit
            EOF

            scp target/S-Mart-0.0.1-SNAPSHOT.jar \
            ubuntu@172.31.18.109:/home/ubuntu/S_Mart-Ecommerce-Website-Java-Project/

            ssh ubuntu@172.31.18.109 << EOF
              nohup java -jar /home/ubuntu/S_Mart-Ecommerce-Website-Java-Project/S-Mart-0.0.1-SNAPSHOT.jar \
              > /home/ubuntu/S_Mart-Ecommerce-Website-Java-Project/app.log 2>&1 &
              exit
            EOF
            '''
        }
    }
}

        
    }

    post {
        success {
            echo "✅ Build & Package Successful!"
        }
        failure {
            echo "❌ Pipeline Failed!"
        }
    }
}

