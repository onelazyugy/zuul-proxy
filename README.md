### A Zuul proxy/gateway to your microservices
* tutorial can be found here: https://spring.io/guides/gs/routing-and-filtering/
- This Zuul proxy serves 2 microservices
    1. productservice
    - GET 
        - http://localhost:8111/zuul/productservice/product/api/v1/product
    - POST 
        - http://localhost:8111/zuul/productservice/product/api/v1/save-product
        - request body
        <code>
            {
                "product": {
                    "id": 1,
                    "name": "jacket",
                    "color": "pink",
                    "category": "clothing"
                }
            }
        </code>
        - response body
        <code>
        {
            "success": true,
            "message": "success",
            "product": {
                "id": 1,
                "name": "jacket",
                "color": "pink",
                "category": "clothing"
            }
        }
        </code>
    2. bookservice
    - GET
        - http://localhost:8111/zuul/bookservice/book/api/v1/book
    - POST 
        - http://localhost:8111/zuul/bookservice/book/api/v1/save-book
        - request body
        <code>
            {
                "book": {
                    "id": 1,
                    "name": "jacket",
                    "color": "pink",
                    "category": "clothing"
                }
            }
        </code>
        - response body
        <code>
        {
            "success": true,
            "message": "success",
            "book": {
                "id": 1,
                "name": "jacket",
                "color": "pink",
                "category": "clothing"
            }
        }
        </code>