GitHub
The developers commit and push their code to the GitHub repository
and linked to the CircleCI platform. GitHub triggers the CircleCI platform when code is pushed to the repository.

CircleCI
CircleCI reads the .circleci/config.yml file 
and .circleci/config.yml tells the service what has to be done. 
there are 2 jobs (frontend & api) to be run by CircleCI.

Frontend: 
npm run build script given in the package.json file. Then uses AWS CLI to upload assets to S3.

api: 
npm run build script, exports all environment variables from CircleCI configuration to a .env file, 
then runs the archive script.