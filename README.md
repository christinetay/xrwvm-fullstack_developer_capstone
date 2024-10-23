[# coding-project-template](url)

# Python
python3 manage.py createsuperuser <br/>
python3 manage.py runserver 8002

# Deploy sentiment analysis
https://sentianalyzer.1nczfjaexwyc.us-south.codeengine.appdomain.cloud <br/>
cd xrwvm-fullstack_developer_capstone/server/djangoapp/microservices <br/>
docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer <br/>
docker push us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer <br/>
ibmcloud ce application create --name sentianalyzer --image us.icr.io/${SN_ICR_NAMESPACE}/senti_analyzer --registry-secret icr-secret --port 5000

# Deploy Dockerfile 
docker build -t us.icr.io/$MY_NAMESPACE/dealership . <br/>
docker push us.icr.io/$MY_NAMESPACE/dealership <br/>

# MongoDB
cd /home/project/xrwvm-fullstack_developer_capstone/server/database <br/>
docker build . -t nodeapp <br/>
docker-compose up

# Frontend rebuild
cd /home/project/xrwvm-fullstack_developer_capstone/server/frontend <br/>
npm install <br/>
npm run build


# Delete dearship project from repository image
ibmcloud cr image-rm us.icr.io/sn-labs-leechoontay/dealership:latest && docker rmi us.icr.io/sn-labs-leechoontay/dealership:latest


# Git clone repository and set up
git init <br/>
export ORIGIN=https://github.com/christinetay/gkpbt-css-circle.git <br/>
git clone https://github.com/christinetay/xrwvm-fullstack_developer_capstone.git <br/>
git config --global user.email "christinetay22@gmail.com" <br/>
git config --global user.name "christinetay"

# Create new branch(test-B) based on the previous branch(test-A)
git checkout -b \<test-B\> = [git branch + git checkout in local] <br/>
git merge \<test-A\> = [test-A data will merge into test-B in local] <br/>
git push --set-upstream origin \<test-B\> = [test-B data will push to repository] <br/>
OR  <br/>
git push origin \<test-A\>:\<test-B\> = [From branch test-A to branch test-B in repository only] <br/>

# push changes after created the branch and first commit
git add . <br/>
git commit -m "new changes" <br/>
git push --set-upstream origin <B> <br/>
git pull origin \<test-B\> --rebase <br/>

# pull changes from repository to local
git pull origin \<test-B\>

# Python commands (in server folder)
python3 manage.py runserver

# Frontend command (in frontend folder)
npm run build

