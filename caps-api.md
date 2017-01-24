## Response structure 
#### Success response example 
```
{
    "status": "success",
    "data": [
        {
            "entity_id": "1",
            "entity_type_id": "4",
            "attribute_set_id": "4",
            "type_id": "simple",
            "sku": "sdcsdc",
            "has_options": "0",
            "required_options": "0",
            "created_at": "2016-12-22 15:06:34",
            "updated_at": "2016-12-22 15:06:34"
        }
    ]
}	
```

#### Error response example 
```
{
    "status": "error",
    "data": null,
    "error": "Invalid user token"
}	
```

## API Methods
> **Note:**
> 
>  All requests except login and register must be send with **_token** field
>  
>  All requests with image must be  encoded as **"multipart/form-data"**

#### **Register User**

* **URL:**   `/api/user/register`

* **Method:** `POST`
  
*  **Params:**
 
  - `firstname [string]` 
  - `lastname [string]`
  - `email [string]`
  - `password [string]`

***
#### **Login User**

  Login User and get access token

* **URL:** ` /api/user/login`

* **Method:**  `POST`
  
*  **Params:**
 
	- `email [string]`
	- `password [string]`

***

#### **Create Config**

* **URL:**  `/api/config/create`

* **Method:**  `POST`
  
*  **Params:**

	-   `json [string]`
	-   `attachment_0 [file]`
	-   ...
	-   ...
	-   `attachment_N [file]`	

***
#### **Edit Config**

* **URL:**  `/api/config/edit`

* **Method:**  `POST`
  
*  **Params:**

	-   `id [int|string]`
	-   `json [string]`
	-   `attachment_0 [file]`
	-   ...
	-   ...
	-   `attachment_N [file]`	

***
#### **Get All Configs**

Get all configs record for current user

* **URL:**  `/api/config/getList`

* **Method:**  `GET`
  
*  **Params:** no

***
#### **Delete Config**

* **URL:**  `/api/config/delete`

* **Method:**  `POST`
  
*  **Params:** 
	- `id [int|string]`

***

#### **Get Products Listing**

* **URL:**  `/api/product/getList`

* **Method:**  `GET`
  
*  **Params:** 

***

#### **Add Product to Cart**

* **URL:**  `/api/order/addToCart`

* **Method:**  `POST`
  
*  **Params:** 
	-  `product_id [int|string]`
	-  `qty [int|string]` ( not required, default 1)
	-   `attachment_0 [file]`
	-   ...
	-   ...
	-   `attachment_N [file]`
	
***

#### **Clear Cart**

* **URL:**  `/api/order/clearCart`

* **Method:**  `POST`
  	
***

#### **Get  Cart**

* **URL:**  `/api/order/getCart`

* **Method:**  `GET`
  
*  **Params:** 

***

#### ** Redirect to cart **

Redirect user to magento checkout page

* **URL:**  `/api/order/checkout?_token={token}`

* **Method:**  `GET|POST`

***

#### **Send Email**

* **URL:**  `/api/share/email`

* **Method:**  `POST`
  
*  **Params:** 
	-  `from_name [string]`
	-  `from_email [string]`	
	-  `to_email [string]`
	-  `subject [string]`
	-  `body [string]`	
	-  `attachment [FILE]`
	
***

#### **Facebook Share**

* **URL:**  `/api/share/fb`

* **Method:**  `POST`
  
*  **Params:** 	
	-  `attachment [FILE]`
	
***
