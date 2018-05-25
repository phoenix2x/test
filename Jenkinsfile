pipeline {
    agent {
        docker 'node:8.11.1'
    }

    parameters {
        booleanParam (
            defaultValue: false,
            description: '',
            name : 'FORCE_FULL_BUILD')
    }

    stages {
//        stage('Install') {
//            steps {
//                sh 'yarn'
//            }
//        }
//        stage('Build') {
//            steps {
//                sh 'yarn build'
//            }
//        }
        stage('Publish') {
//            environment {
//                NPMRC = credentials('NPMRC')
//            }
            steps {
//                sh 'echo $NPMRC > .npmrc'
                sh 'echo ${params.FORCE_FULL_BUILD}'
//
//                sh 'npm --no-git-tag-version version prerelease'
//                sh 'npm publish'
//                sh 'git -c "user.name=Jenkins" -c "user.email=Jenkins" commit --no-verify -m "Jenkins version bump" package.json'
//                sh 'git push https://${BITBUCKET_USR}:${BITBUCKET_PSW}@stash.consumer.org/scm/cro/global-navigation-ui.git HEAD:$BRANCH_NAME'
//                sh '''#!/bin/bash
//                    urlencode() {
//                        old_lc_collate=$LC_COLLATE
//                        LC_COLLATE=C
//
//                        local length="${#1}"
//                        for (( i = 0; i < length; i++ )); do
//                            local c="${1:i:1}"
//                            case $c in
//                                [a-zA-Z0-9.~_-]) printf "$c" ;;
//                                *) printf '%%%02X' "'$c" ;;
//                            esac
//                        done
//
//                        LC_COLLATE=$old_lc_collate
//                    }
//                    echo $(urlencode "@")
//                    '''
//                script {
//                    withCredentials([sshUserPrivateKey(credentialsId: "test_ssh", keyFileVariable: 'SSH_KEY')]) {
//                        sh 'git -c "user.name=Jenkins" -c "user.email=Jenkins" commit -m "Jenkins version bump" package.json'
//                        sh 'echo ssh -i $SSH_KEY -l git -o StrictHostKeyChecking=no \\"\\$@\\" > run_ssh.sh'
//                        sh 'chmod +x run_ssh.sh'
//                        sh 'GIT_SSH=./run_ssh.sh git push ssh://git@172.18.0.1:7999/test/test-repo.git HEAD:$BRANCH_NAME'
//                    }
//                }
            }
        }
    }
}