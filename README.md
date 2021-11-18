# MERN CART API's:

@Author: Swapnil Chute
@Copyright: 2021

# User Authenticatino:

Base URL: https://node-merncart.vercel.app/

SR => Feature => Type => URL => Headers => Required => Fields

#User

1.  Register => [POST] => [/user/register] => null [email as username, password]
2.  Login => [POST] => [/user/login] => null => [email as username, password]
3.  Profile => [GET] => [/user/profile] => [token] => null
4.  Update Profile => [POST] => [user/profile] =>[token] => [name, phone]
5.  Update Addresses => [POST] => [user/address] => [email, address: [{key: value}]]
    address object keys {title: string, addressLine1: string, addressLine2: string, city:sting, zip:string, state:string}
6.  Remove Address => [DELETE] => [user/address/:id] => [token]

#Product

1. Get Products => [GET] => [/product] => [token]
2. Add Product => [POST]=> [/product] => [token] => {title, price,description,category,image,rating:{rate, count}}
3. Get Single Product => [GET]=>[/product/:id] => [token]
4. Update Product => [POST]=>[/product/:id] => [token] => {title, price,description,category,image,rating:{rate, count}} any
5. Delete Product => [DELETE]=>[/product/:id] => [token]

#Cart

1. Get Cart Items => [GET] => [/cart] => [token]
2. Add Cart Item => [POST]=> [/cart] => [token] => {quantity,title,price,description,category,image}
3. Delete Single Cart Item => [DELETE]=>[/cart/:id] => [token]
4. Empty cart => [DELETE]=>[/cart] => [token]
