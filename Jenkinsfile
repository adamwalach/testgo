node {
   stage 'Set variables'
   echo "CURRENT_BRANCH: '${env.BRANCH_NAME}'"
   sh '''
     whoami
     ls -l
     pwd
   '''
   stage 'Checkout'
   checkout scm
   stage 'Project build'
   sh '''
ls -l
env
go version
go build main.go -o main
'''
   stage 'Docker build'
   sh '''
   docker -t gotest .
   '''
}
