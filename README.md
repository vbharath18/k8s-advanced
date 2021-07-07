# k8s-advanced

echo -n TAITest987$ | base64

VEFJVGVzdDk4NyQ=

kubectl run -it --rm --image=mysql --restart=Never mysql-client -- mysql --host mysql --password=TAITest987$

CREATE DATABASE flaskapi;
USE flaskapi;
CREATE TABLE users(user_id INT PRIMARY KEY AUTO_INCREMENT, user_name VARCHAR(255), user_email VARCHAR(255), user_password VARCHAR(255));

--POST
curl -H "Content-Type: application/json" -d '{"name": "vbharath", "email": "vb@athena.com", "pwd": "pass"}' http://127.0.0.1:5000/create

--GET
curl 127.0.0.1:5000/users

--GET
curl 127.0.0.1:5000/user/1

--POST
curl -H "Content-Type: application/json" -d '{"name": "vbharath", "email": "vb@athena.com", "pwd": "fail", "user_id": 1}' 127.0.0.1:5000/update

curl 127.0.0.1:5000/delete/1