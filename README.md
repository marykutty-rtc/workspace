# Task

1. Create a login form.
2. After successful login,
   - navigate to home page at "/seller-products"
   - display seller products from the api response (api details given below)
   - display a logout button
3. For calling gwt seler products api, you will have to pass an auth header in request.
4. The token is in the response of login endpoint
5. Pass it in the request header Authorization: Bearer { token_from_login_response }
6. Each product should display the product image, title and isDeleted as a checkbox

## Endpoints to use

1. Login - https://qa-api.quotesouk.com/api/v1/BuyerAuth/authenticateWithCredentials

Request Parameters(sample)

```
{
  "email":"jinoshajiv@gmail.com",
  "fcm_Token":"",
  "password":"Jino@123"
}
```

Response Parameters(sample)

```
{
    "succeeded": true,
    "message": "Authenticated 165ea147-cf30-47bf-84b5-07dbffce1fde",
    "errors": null,
    "data": {
        "id": "f5f072ec-125f-4249-a693-1eb6cd84cc1b",
        "fullName": "Jino Shaji",
        "email": "jinoshajiv@gmail.com",
        "phoneNumber": null,
        "roles": [
            "Buyer"
        ],
        "isVerified": true,
        "expieryDateTime": "2024-11-12T12:38:13Z",
        "jwToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxNjVlYTE0Ny1jZjMwLTQ3YmYtODRiNS0wN2RiZmZjZTFmZGUiLCJqdGkiOiIzOWU5OTgwNS05YzQ5LTQxY2UtYThhOS0wN2VmMjExZDFmMmEiLCJlbWFpbCI6Imppbm9zaGFqaXZAZ21haWwuY29tIiwidWlkIjoiZjVmMDcyZWMtMTI1Zi00MjQ5LWE2OTMtMWViNmNkODRjYzFiIiwiaXAiOiIxNjkuMjU0LjIxMC4xMTQiLCJyb2xlcyI6IkJ1eWVyIiwiZXhwIjoxNzMxNDE1MDkzLCJpc3MiOiJDb3JlSWRlbnRpdHkiLCJhdWQiOiJDb3JlSWRlbnRpdHlVc2VyIn0.xWBljt1G0nCdbIeoyNJvBhfcI-7GKsGi-QRk5STCS04",
        "refreshToken": "B9E08D1AF9E9CCC8FC5AC69EC4E31466901B8F8AEBCB2B552C9FD2E72F17F94902B9C6EBAAD67CD2",
        "loginTrackingKey": "f9e54a5a-404d-4076-6fac-08dbe445670f"
    }
}
```

2. Get all Seller Products - https://qa-api.quotesouk.com/api/v1/SellerProduct/GetAllTopSellerProducts

Request Parameters(sample): none

Response Parameters(sample)

```
{
    "totalRecords": 218,
    "pageNumber": 1,
    "pageSize": 50,
    "succeeded": true,
    "message": "Products found.",
    "errors": null,
    "data": [
          {
              "sellerProductId": "8dbee954-f204-4124-a169-08db366e3f8c",
              "userId": "e604db99-b08a-4672-8e96-3f09959c5fcb",
              "title": "Restaurant Furniture",
              "image": "https://qa-api.quotesouk.com/Resources/SellerProduct/e7748fd5-65d5-4fc5-abd8-6fa69ddbea47_4 (2).webp",
              "shortDescription": "cycle style ms powder coated base and reclaimed wood top. Chair:Metal chair with powder coat color and leatherite cushion",
              "description": "We design & delivers quality\nfurniture for your home & oce\nspaces. We also execute custom\nmade projects along with other\nready-made furniture like Sofa\nset, Dining Table sets, Wardrobe,\nSit out chairs, Hospital / Airport\nwaiting chairs etc. We are experts\nin Home interior design, Oce\nWorkstation design and Café /\nRestaurant furniture. We are one\nof the leading supplier of Zero\nGravity Massage chairs in Kerala.",
              "specifications": "Customized product with  Metal and wooden Material ",
              "rating": 4.000000,
              "isTopSellerProduct": true,
              "seoTitle": null,
              "h1Tag": null,
              "metaDescription": null,
              "sellerId": "SE-0000011-6989-34",
              "sellerName": "redChair Home Decor ",
              "categoryId": "34b503f5-0700-4107-36e5-08db5e67ce90",
              "categoryName": "FURNITURE, INTERIOR DECOR & ACCESSORIES",
              "categoryImage": "https://qa-api.quotesouk.com/Resources/Category/43fe035c-3422-41ad-afe4-6b9407461c87_Untitled-1.webp",
              "subCategoryId": "7cf2a46b-fe5f-45f9-9c28-08db5e67e84e",
              "subCategoryName": "Furniture",
              "subCategoryImage": "https://qa-api.quotesouk.com/Resources/SubCategory/4d96fe2a-2e6c-42b7-9e2a-9edd45725834_Furniture.webp",
              "createdBy": null,
              "created": "0001-01-01T00:00:00",
              "lastModifiedBy": "8bd1be6a-6f3b-4915-9e36-8dae74568573",
              "lastModified": "2023-07-05T02:59:23.7218567",
              "isDeleted": false
          },{
          "id": "f5f072ec-125f-4249-a693-1eb6cd84cc1b",
          "fullName": "Jino Shaji",
          "email": "jinoshajiv@gmail.com",
          "phoneNumber": null,
          "roles": [
              "Buyer"
          ],
          "isVerified": true,
          "expieryDateTime": "2024-11-12T12:38:13Z",
          "jwToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxNjVlYTE0Ny1jZjMwLTQ3YmYtODRiNS0wN2RiZmZjZTFmZGUiLCJqdGkiOiIzOWU5OTgwNS05YzQ5LTQxY2UtYThhOS0wN2VmMjExZDFmMmEiLCJlbWFpbCI6Imppbm9zaGFqaXZAZ21haWwuY29tIiwidWlkIjoiZjVmMDcyZWMtMTI1Zi00MjQ5LWE2OTMtMWViNmNkODRjYzFiIiwiaXAiOiIxNjkuMjU0LjIxMC4xMTQiLCJyb2xlcyI6IkJ1eWVyIiwiZXhwIjoxNzMxNDE1MDkzLCJpc3MiOiJDb3JlSWRlbnRpdHkiLCJhdWQiOiJDb3JlSWRlbnRpdHlVc2VyIn0.xWBljt1G0nCdbIeoyNJvBhfcI-7GKsGi-QRk5STCS04",
          "refreshToken": "B9E08D1AF9E9CCC8FC5AC69EC4E31466901B8F8AEBCB2B552C9FD2E72F17F94902B9C6EBAAD67CD2",
          "loginTrackingKey": "f9e54a5a-404d-4076-6fac-08dbe445670f"
    },
    //... other products
  ]
}
```

In the task, please use

1. lazy-loading feature module
2. services
3. models
4. interceptors
5. routing
