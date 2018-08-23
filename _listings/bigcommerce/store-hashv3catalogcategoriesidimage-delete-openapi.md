---
swagger: "2.0"
x-collection-name: BigCommerce
x-complete: 0
info:
  title: BigCommerce Delete a category image
  description: ""
  version: 1.0.0
host: api.bigcommerce.com
basePath: /stores
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{store-hash}/v3/catalog/products/{id}/images:
    get:
      summary: Retrieve images for a single product
      description: GET request for retrieving images associated with a product
      operationId: V3CatalogProductsImagesByStoreHashAndIdGet
      x-api-path-slug: storehashv3catalogproductsidimages-get
      parameters:
      - in: path
        name: id
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - Imagesa
      - Single
      - Product
    post:
      summary: Upload a new product image to a single product
      description: Adds a new product image from a publicly accessible URL. May fail
        if the hosting website is forcing HTTPS connections with TLS 1.0 (as this
        has been deprecated).
      operationId: V3CatalogProductsImagesByStoreHashAndIdPost
      x-api-path-slug: storehashv3catalogproductsidimages-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Upload
      - New
      - Product
      - Image
      - To
      - Single
      - Product
  /{store-hash}/v3/catalog/products/{id}:
    get:
      summary: Retrieve a single product with expanded sub-resources
      description: Request a single product with expanded variant information
      operationId: V3CatalogProductsByStoreHashAndIdGet
      x-api-path-slug: storehashv3catalogproductsid-get
      parameters:
      - in: path
        name: id
      - in: query
        name: include
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - Single
      - Product
      - Expanded
      - Sub-resources
    put:
      summary: Update a product in the catalog
      description: Updates a single product's information in the catalog
      operationId: V3CatalogProductsByStoreHashAndIdPut
      x-api-path-slug: storehashv3catalogproductsid-put
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Product
      - In
      - Catalog
    delete:
      summary: Delete a single product by ID
      description: Deleting a single product from the catalog by product ID
      operationId: V3CatalogProductsByStoreHashAndIdDelete
      x-api-path-slug: storehashv3catalogproductsid-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Single
      - Product
      - By
      - ID
  /{store_hash}/v3/catalog/products/{id}/videos/{id}:
    get:
      summary: Retrieve a video on a product
      description: ""
      operationId: V3CatalogProductsVideosIdByStoreHashAndIdGet
      x-api-path-slug: store-hashv3catalogproductsidvideosid-get
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - Video
      - "On"
      - Product
    put:
      summary: Updates an video on a product
      description: ""
      operationId: V3CatalogProductsVideosIdByStoreHashAndIdPut
      x-api-path-slug: store-hashv3catalogproductsidvideosid-put
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - S
      - Video
      - "On"
      - Product
    delete:
      summary: Delete a video on a product
      description: ""
      operationId: V3CatalogProductsVideosIdByStoreHashAndIdDelete
      x-api-path-slug: store-hashv3catalogproductsidvideosid-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Video
      - "On"
      - Product
  /{store_hash}/v3/catalog/products/variants:
    get:
      summary: Retrieve variant with parameters
      description: Returns a `Variant` object list from the BigCommerce Catalog.
      operationId: V3CatalogProductsVariantsByStoreHashGet
      x-api-path-slug: store-hashv3catalogproductsvariants-get
      parameters:
      - in: query
        name: sku
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - Variant
      - Parameters
  /{store_hash}/v3/catalog/products/{id}/videos:
    get:
      summary: Retrieve all videos for a single product
      description: ""
      operationId: V3CatalogProductsVideosByStoreHashAndIdGet
      x-api-path-slug: store-hashv3catalogproductsidvideos-get
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - ""
      - Videosa
      - Single
      - Product
    post:
      summary: Add a video to a product using a video ID from Youtube
      description: Creates an video on a product using a video ID from Youtube
      operationId: V3CatalogProductsVideosByStoreHashAndIdPost
      x-api-path-slug: store-hashv3catalogproductsidvideos-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Video
      - To
      - Product
      - Using
      - Video
      - ID
      - From
      - Youtube
  /{store_hash}/v3/catalog/categories/{id}:
    get:
      summary: Retrieve a single category
      description: ""
      operationId: V3CatalogCategoriesByStoreHashAndIdGet
      x-api-path-slug: store-hashv3catalogcategoriesid-get
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - Single
      - Category
    put:
      summary: Update a category
      description: Update a `Category` in the BigCommerce Catalog
      operationId: V3CatalogCategoriesByStoreHashAndIdPut
      x-api-path-slug: store-hashv3catalogcategoriesid-put
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Category
    delete:
      summary: Delete a single category
      description: ""
      operationId: V3CatalogCategoriesByStoreHashAndIdDelete
      x-api-path-slug: store-hashv3catalogcategoriesid-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Single
      - Category
  /{store_hash}/v3/catalog/brands/{id}/image:
    post:
      summary: Upload an image for a brand
      description: ""
      operationId: V3CatalogBrandsImageByStoreHashAndIdPost
      x-api-path-slug: store-hashv3catalogbrandsidimage-post
      parameters:
      - in: path
        name: id
      - in: formData
        name: image_file
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Upload
      - Imagea
      - Brand
    delete:
      summary: Delete a brand image
      description: Delete a `Brand` image the BigCommerce Catalog
      operationId: V3CatalogBrandsImageByStoreHashAndIdDelete
      x-api-path-slug: store-hashv3catalogbrandsidimage-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Brand
      - Image
  /{store-hash}/v3/catalog/products:
    get:
      summary: Retrieve all products with expanded sub-resources
      description: Shows full product data with a single GET request
      operationId: V3CatalogProductsByStoreHashGet
      x-api-path-slug: storehashv3catalogproducts-get
      parameters:
      - in: query
        name: include
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - ""
      - Products
      - Expanded
      - Sub-resources
    post:
      summary: Create a new product with variants
      description: Sample request for creating a new product with variants through
        V3 Catalog API
      operationId: V3CatalogProductsByStoreHashPost
      x-api-path-slug: storehashv3catalogproducts-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - New
      - Product
      - Variants
    delete:
      summary: Delete multiple products
      description: Deletes products that aren't marked as visible using a filter parameter
      operationId: V3CatalogProductsByStoreHashDelete
      x-api-path-slug: storehashv3catalogproducts-delete
      parameters:
      - in: query
        name: is_visible
      - in: path
        name: store-hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Multiple
      - Products
  /{store_hash}/v3/catalog/summary:
    get:
      summary: Returns a lightweight inventory summary
      description: Returns a lightweight inventory summary from the BigCommerce Catalog.
      operationId: V3CatalogSummaryByStoreHashGet
      x-api-path-slug: store-hashv3catalogsummary-get
      parameters:
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Returns
      - Lightweight
      - Inventory
      - Summary
  /{store_hash}/v3/catalog/products/{id}/options:
    get:
      summary: Retrieve an array of product options
      description: ""
      operationId: V3CatalogProductsOptionsByStoreHashAndIdGet
      x-api-path-slug: store-hashv3catalogproductsidoptions-get
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Retrieve
      - Array
      - Of
      - Product
      - Options
    post:
      summary: Create a product option
      description: ""
      operationId: V3CatalogProductsOptionsByStoreHashAndIdPost
      x-api-path-slug: store-hashv3catalogproductsidoptions-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Product
      - Option
  /{store_hash}/v3/catalog/categories/{id}/image:
    post:
      summary: Create an image for a category
      description: ""
      operationId: V3CatalogCategoriesImageByStoreHashAndIdPost
      x-api-path-slug: store-hashv3catalogcategoriesidimage-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Imagea
      - Category
    delete:
      summary: Delete a category image
      description: ""
      operationId: V3CatalogCategoriesImageByStoreHashAndIdDelete
      x-api-path-slug: store-hashv3catalogcategoriesidimage-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: store_hash
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Category
      - Image
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---