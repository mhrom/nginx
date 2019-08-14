pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		sh 'cd nginx-1.16.1 && ./configure --builddir=nginx-1.16.1 --with-pcre=../pcre-8.42 --with-zlib=../zlib-1.2.11 --with-openssl=../openssl-1.1.0h --with-debug'
                sh 'cd nginx-1.16.1 && make' 
            }
        }
    }
}
