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
whereis go
/usr/bin/go version
go build -o main main.go
'''
   stage 'Docker build'
   sh '''#!/bin/bash
   docker build -t gotest:$BRANCH_NAME ./
   '''
}
