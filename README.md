[# coding-project-template](url)

# Python
python3 manage.py createsuperuser <br/>
python3 manage.py runserver 8002

# Deploy sentiment analysis
https://sentianalyzer.1nczfjaexwyc.us-south.codeengine.appdomain.cloud

cd xrwvm-fullstack_developer_capstone/server/djangoapp/microservices

docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer
docker push us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer
ibmcloud ce application create --name sentianalyzer --image us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer --registry-secret icr-secret --port 5000

# Deploy Dockerfile 
docker build -t us.icr.io/$MY_NAMESPACE/dealership .
docker push us.icr.io/$MY_NAMESPACE/dealership

# MongoDB
cd /home/project/xrwvm-fullstack_developer_capstone/server/database
docker build . -t nodeapp
docker-compose up

# Frontend rebuild
cd /home/project/xrwvm-fullstack_developer_capstone/server/frontend
npm install
npm run build


# Delete dearship project from repository image
ibmcloud cr image-rm us.icr.io/sn-labs-leechoontay/dealership:latest && docker rmi us.icr.io/sn-labs-leechoontay/dealership:latest


# Git clone repository and set up
git init
export ORIGIN=https://github.com/christinetay/gkpbt-css-circle.git
git clone https://github.com/christinetay/xrwvm-fullstack_developer_capstone.git
git config --global user.email "christinetay22@gmail.com"
git config --global user.name "christinetay"

# Create new branch(B) based on the previous branch(A)
git checkout -b <B> = [git branch + git checkout in local]
git merge <A> = [A data will merge into B in local]
git push --set-upstream origin <B> = [B data will push to repository]
OR
git push origin <A>:<B> = [From branch A to branch B in repository only]

# push changes after created the branch and first commit
git add .
git commit -m "new changes"
git push --set-upstream origin <B>
git pull origin <b> --rebase

# pull changes from repository to local
git pull origin <B>

# Python commands (in server folder)
python3 manage.py runserver

# Frontend command (in frontend folder)
npm run build

