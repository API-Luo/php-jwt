# php-jwt

use Co\JWT\JWT;    

$key = "test_key";    
$token = [    
    "iss" => "https://www.baidu.com",    
    "aud" => "https://www.qq.com",    
    "iat" => 1356999524,    
    "nbf" => 1357000000    
];    
$jwt = new JWT();    
$encode = $jwt->encode($token, $key);  
$decode = $jwt->decode($encode, $key, ['HS256']);    

print_r($decode);  
