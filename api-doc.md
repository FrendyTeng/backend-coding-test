**Delivery**


> get info

* **URL**

    /

* **Method:**
  
    `GET`
  
*  **URL Params**

    `none`

*  **Req Header**

    `none`

* **Data Params**

    `none`

* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
    ```
    {
        "code": 1,
        "message": "ok",
        "data": null
    }
    ```

> Create Delivery Info

* **URL**

    /rides

* **Method:**
  
    `POST`
  
*  **URL Params**

    `none`

*  **Req Body**

```json
    {
        "start_lat": "double", 
        "start_long": "double", 
        "end_lat": "double", 
        "end_long": "double",
        "rider_name": "string",
        "driver_name": "string", 
        "driver_vehicle": "string"
    }
```
`sample: `

```json
    {
        "startLat": -6.121435,
        "startLong": 106.774124,
        "endLat": -6.17311,
        "endLong": 106.829361,
        "riderName": "Jack",
        "driverName": "John",
        "driverVehicle": "Cargo",
    }
```

* **Success Response:**
  
  * **Code:** 201 <br />
    **Content:** 
    ```
    [
        {
            "rideID": 1,
            "startLat": -6.121435,
            "startLong": 106.774124,
            "endLat": -6.17311,
            "endLong": 106.829361,
            "riderName": "Jack",
            "driverName": "John",
            "driverVehicle": "Cargo",
            "created": "2020-11-21 07:08:09"
        }
    ]
    ```
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** 
    ```
    {
        "code": 0,
        "message": "End latitude and longitude must be between -75 to 75 and -195 to 195 degrees        respectively",
        "data": null
    }
    ```
    ```
    {
        "code": 0,
        "message": "Rider name must be a non empty string",
        "data": null
    }
    ```
    ```
    {
        "code": 0,
        "message": "Unknown error",
        "data": null
    }
    ```



> Delivery Info (Find All)

* **URL**

    /rides

* **Method:**
  
    `GET`
  
*  **URL Params**

    `none`

*  **Req Body**

    `none`

* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
    ```
    [
         {
            "rideID": 1,
            "startLat": -6.121435,
            "startLong": 106.774124,
            "endLat": -6.17311,
            "endLong": 106.829361,
            "riderName": "Jack",
            "driverName": "John",
            "driverVehicle": "Cargo",
            "created": "2020-11-21 07:08:09"
        },
        {
            "rideID": 2,
            "startLat": -6.121435,
            "startLong": 106.774124,
            "endLat": -6.17311,
            "endLong": 106.829361,
            "riderName": "Dan",
            "driverName": "Jay",
            "driverVehicle": "Cargo",
            "created": "2020-11-21 07:36:26"
        },
        {
            "rideID": 3,
            "startLat": -6.121435,
            "startLong": 106.774124,
            "endLat": -6.17311,
            "endLong": 106.829361,
            "riderName": "Cam",
            "driverName": "Mitch",
            "driverVehicle": "Cargo",
            "created": "2020-11-21 07:38:34"
        }
    ]
    ```
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** 
    ```
    {
        "code": 0,
        "message": "Unknown error",
        "data": null
    }
    ```
    ```
    {
        "code": 0,
        "message": "Could not find any rides",
        "data": null
    }
    ```


> Delivery Info (Find By Id)

* **URL**

    /rides/:id

* **Method:**
  
    `GET`
  
*  **URL Params**

    id=[integer]

*  **Req Body**

    `none`

* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
    ```
    [
        {
            "rideID": 1,
            "startLat": -6.121435,
            "startLong": 106.774124,
            "endLat": -6.17311,
            "endLong": 106.829361,
            "riderName": "Jack",
            "driverName": "John",
            "driverVehicle": "Cargo",
            "created": "2020-11-21 07:08:09"
        }
    ]
    ```
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** 
    ```
    {
        "code": 0,
        "message": "Unknown error",
        "data": null
    }
    ```
    ```
    {
        "code": 0,
        "message": "Could not find any rides",
        "data": null
    }
    ```