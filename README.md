# login_jwt
an example login program with java web token tech


## Run UserServiceApplication
springboot patter


## Post request localhost:8080/api/login
### Body  
{  
"username": john,  
"password": 1234  
}  

### Response 
{  
"access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJqb2huIiwicm9sZXMiOlsiUk9MRV9VU0VSIl0sImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6ODA4MC9hcGkvbG9naW4iLCJleHAiOjE2NTIzODkwMzd9.VLg4i_ghciBlGU1PyMFI0UX6R32chtho6DipoyXRa9Q",  
"refresh_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJqb2huIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL2FwaS9sb2dpbiIsImV4cCI6MTY1MjM5MDIzN30.WoojcJzYtfCmNN8PUeX3w_P-zPAxVsgg8COSjszw6Hk"  
}  


## GET request localhost:8080/api/users
### Headers
{  
"Authorization": "Bearer xxxxxx(access_token)"  
}  

### Response  
[  
{  
"id": 5,  
"name": "John Travolta",  
"username": "john",  
"password": "$2a$10$9P7q1qt99k9.0QChqWGE7uUqvK5Ed9ra20zpdurib6B.mnV3W.hAe",  
"roles": [  
{  
"id": 1,  
"name": "ROLE_USER"  
}  
]  
},  
]  


## GET request localhost:8080/api/token/refresh
refresh token