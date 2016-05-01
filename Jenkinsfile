node {
   stage 'Set variables'
    if(env.BRANCH_NAME == null){
      echo "ISNULL"
      env.BRANCH_NAME = DEFAULT_BUILD_BRANCH
   }
   echo "DEFAULT_BRANCH: '${DEFAULT_BUILD_BRANCH}'"
   echo "CURRENT_BRANCH: '${env.BRANCH_NAME}'"
}
