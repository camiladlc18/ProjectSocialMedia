# coding-project-template
const uri =  "mongodb://mongodb:27017";
mongoose.connect(uri,{'dbName':'SocialDB'});

docker build . -t socialapp

docker-compose up

curl  -X POST  -H 'Content-Type: application/json'  -d '{
    "username":"coopercoote",
    "email":"ccoote@gmail.com",
    "password":"cg123"}' -k 'http://localhost:3000/register'

curl  -X POST  -H 'Content-Type: application/json'  -d '{
    "username":"coopercoote",
    "password":""}' -k 'http://localhost:3000/login'
