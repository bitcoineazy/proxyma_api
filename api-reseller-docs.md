{
    "openapi": "3.0.0",
    "info": {
        "title": "API Reseller Documentation",
        "description": "Получить свой API KEY, вы можете в шапке профиля личного кабинета пользователя.\n        Все запросы к методам Proxyma API должны содержать header заголовок api-key \n\n        Пример на PHP:\n \n        CURLOPT_HTTPHEADER => array(\n            'api-key: YOUR API KEY',\n            'Content-Type: application/json'\n        )",
        "version": "1.0.0"
    },
    "paths": {
        "/api/isp/packages": {
            "get": {
                "tags": [
                    "ISP"
                ],
                "summary": "Get all packages",
                "operationId": "0d5f3d67c9ad0bd862acf958f32475c0",
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "data": {
                                            "type": "array",
                                            "items": {
                                                "properties": {
                                                    "id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "order_id": {
                                                        "type": "integer",
                                                        "example": "123"
                                                    },
                                                    "status": {
                                                        "type": "string",
                                                        "example": "active"
                                                    },
                                                    "duration_days": {
                                                        "type": "integer",
                                                        "example": 30
                                                    },
                                                    "purpose_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "package_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "coutnry": {
                                                        "type": "string",
                                                        "example": "RU"
                                                    },
                                                    "login": {
                                                        "type": "string",
                                                        "example": "proxymaoffice"
                                                    },
                                                    "password": {
                                                        "type": "string",
                                                        "example": "12345678"
                                                    },
                                                    "ip_count": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "ip_list": {
                                                        "type": "array",
                                                        "items": {
                                                            "type": "string"
                                                        }
                                                    },
                                                    "expires_at": {
                                                        "type": "string",
                                                        "example": "2024-08-01 00:00:00"
                                                    },
                                                    "auto_update": {
                                                        "type": "boolean",
                                                        "example": true
                                                    },
                                                    "created_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    },
                                                    "updated_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    }
                                                },
                                                "type": "object"
                                            }
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/isp/packages/{package}": {
            "get": {
                "tags": [
                    "ISP"
                ],
                "summary": "Get package by id",
                "operationId": "ed943991bdf26e0190c6625db0b944b2",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "data": {
                                            "type": "array",
                                            "items": {
                                                "properties": {
                                                    "id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "order_id": {
                                                        "type": "integer",
                                                        "example": "123"
                                                    },
                                                    "status": {
                                                        "type": "string",
                                                        "example": "active"
                                                    },
                                                    "duration_days": {
                                                        "type": "integer",
                                                        "example": 30
                                                    },
                                                    "purpose_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "package_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "coutnry": {
                                                        "type": "string",
                                                        "example": "RU"
                                                    },
                                                    "login": {
                                                        "type": "string",
                                                        "example": "proxymaoffice"
                                                    },
                                                    "password": {
                                                        "type": "string",
                                                        "example": "12345678"
                                                    },
                                                    "ip_count": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "ip_list": {
                                                        "type": "array",
                                                        "items": {
                                                            "type": "string"
                                                        }
                                                    },
                                                    "expires_at": {
                                                        "type": "string",
                                                        "example": "2024-08-01 00:00:00"
                                                    },
                                                    "auto_update": {
                                                        "type": "boolean",
                                                        "example": true
                                                    },
                                                    "created_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    },
                                                    "updated_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    }
                                                },
                                                "type": "object"
                                            }
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            },
            "delete": {
                "tags": [
                    "ISP"
                ],
                "summary": "Delete package by id",
                "operationId": "d429702f8c4c2f99de467af2e118d491",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/isp/plans": {
            "get": {
                "tags": [
                    "ISP"
                ],
                "summary": "Get all plans",
                "operationId": "bde5a6811b985b43642b87fada41ce23",
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "data": {
                                            "type": "array",
                                            "items": {
                                                "type": "string"
                                            }
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/isp/plans/{plan}": {
            "get": {
                "tags": [
                    "ISP"
                ],
                "summary": "Get plan by id",
                "operationId": "6ce69202df768eb9767989adac6e6501",
                "parameters": [
                    {
                        "name": "plan",
                        "in": "path",
                        "description": "ID of the plan",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "data": {
                                            "type": "array",
                                            "items": {
                                                "type": "string"
                                            }
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/isp/packages/{package}/auto-update": {
            "put": {
                "tags": [
                    "ISP"
                ],
                "summary": "Set auto update package",
                "operationId": "b700eb562878728d66952e10dbaa7586",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "requestBody": {
                    "required": true,
                    "content": {
                        "application/json": {
                            "schema": {
                                "properties": {
                                    "auto_update": {
                                        "type": "boolean"
                                    }
                                },
                                "type": "object"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "data": {
                                            "type": "array",
                                            "items": {
                                                "properties": {
                                                    "id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "order_id": {
                                                        "type": "integer",
                                                        "example": "123"
                                                    },
                                                    "status": {
                                                        "type": "string",
                                                        "example": "active"
                                                    },
                                                    "duration_days": {
                                                        "type": "integer",
                                                        "example": 30
                                                    },
                                                    "purpose_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "package_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "coutnry": {
                                                        "type": "string",
                                                        "example": "RU"
                                                    },
                                                    "login": {
                                                        "type": "string",
                                                        "example": "proxymaoffice"
                                                    },
                                                    "password": {
                                                        "type": "string",
                                                        "example": "12345678"
                                                    },
                                                    "ip_count": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "ip_list": {
                                                        "type": "array",
                                                        "items": {
                                                            "type": "string"
                                                        }
                                                    },
                                                    "expires_at": {
                                                        "type": "string",
                                                        "example": "2024-08-01 00:00:00"
                                                    },
                                                    "auto_update": {
                                                        "type": "boolean",
                                                        "example": true
                                                    },
                                                    "created_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    },
                                                    "updated_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    }
                                                },
                                                "type": "object"
                                            }
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/isp/packages/{package}/update": {
            "post": {
                "tags": [
                    "ISP"
                ],
                "summary": "Update package by id",
                "operationId": "944d7edda8d081257a1a133530c3ccaa",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "requestBody": {
                    "required": false,
                    "content": {
                        "application/json": {
                            "schema": {
                                "properties": {
                                    "promo": {
                                        "type": "string"
                                    }
                                },
                                "type": "object"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "data": {
                                            "type": "array",
                                            "items": {
                                                "properties": {
                                                    "id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "order_id": {
                                                        "type": "integer",
                                                        "example": "123"
                                                    },
                                                    "status": {
                                                        "type": "string",
                                                        "example": "active"
                                                    },
                                                    "duration_days": {
                                                        "type": "integer",
                                                        "example": 30
                                                    },
                                                    "purpose_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "package_id": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "coutnry": {
                                                        "type": "string",
                                                        "example": "RU"
                                                    },
                                                    "login": {
                                                        "type": "string",
                                                        "example": "proxymaoffice"
                                                    },
                                                    "password": {
                                                        "type": "string",
                                                        "example": "12345678"
                                                    },
                                                    "ip_count": {
                                                        "type": "integer",
                                                        "example": 1
                                                    },
                                                    "ip_list": {
                                                        "type": "array",
                                                        "items": {
                                                            "type": "string"
                                                        }
                                                    },
                                                    "expires_at": {
                                                        "type": "string",
                                                        "example": "2024-08-01 00:00:00"
                                                    },
                                                    "auto_update": {
                                                        "type": "boolean",
                                                        "example": true
                                                    },
                                                    "created_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    },
                                                    "updated_at": {
                                                        "type": "string",
                                                        "example": "2024-02-10 18:22:53"
                                                    }
                                                },
                                                "type": "object"
                                            }
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/isp/packages/{package}/swap-ip": {
            "get": {
                "tags": [
                    "ISP"
                ],
                "summary": "Swap IP of the package",
                "operationId": "a65cb92d745cc3d7b5c122d125531adc",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/isp/packages/{package}/ip-auth": {
            "post": {
                "tags": [
                    "ISP"
                ],
                "summary": "Add authorized IP for the package",
                "operationId": "2fa4d766320b6d15a5bc8027bc944b6e",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successful response",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/packages": {
            "get": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Получение данных о приобретенных пакетах Residential Unlim пользователя",
                "operationId": "c72a69c5f9dbe99ebc8cb0b6099299bc",
                "responses": {
                    "200": {
                        "description": "Успешное получение данных о пакетах Residential Unlim пользователя",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "packages": [
                                        {
                                            "id": 1,
                                            "name": "string",
                                            "price": 1,
                                            "speed_limit": 1,
                                            "duration_days": 1,
                                            "status": "string",
                                            "created_at": "string",
                                            "updated_at": "string"
                                        }
                                    ]
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            },
            "delete": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Удалить пакеты",
                "operationId": "16ae890291f599263f760834c2da3bd5",
                "requestBody": {
                    "required": true,
                    "content": {
                        "application/json": {
                            "schema": {
                                "required": [
                                    "order_ids"
                                ],
                                "properties": {
                                    "order_ids": {
                                        "description": "Массив ид заказов пакетов",
                                        "type": "string",
                                        "example": [
                                            "1234534",
                                            "4564"
                                        ]
                                    }
                                },
                                "type": "object"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Успешное удаление пакетов",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "required": [
                                        "success"
                                    ],
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/packages/{package}": {
            "get": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Получение данных о приобретенном пакете Residential Unlim пользователя",
                "operationId": "6f91ccabf63d2603e71c55d123afe3aa",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "ID пакета",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Успешное получение данных о пакете Residential Unlim пользователя",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "packages": [
                                        {
                                            "id": 1,
                                            "name": "string",
                                            "price": 1,
                                            "speed_limit": 1,
                                            "duration_days": 1,
                                            "status": "string",
                                            "created_at": "string",
                                            "updated_at": "string"
                                        }
                                    ]
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "422": {
                        "description": "Ошибка валидации",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "The given data was invalid."
                                        },
                                        "errors": {
                                            "properties": {
                                                "field_name": {
                                                    "type": "array",
                                                    "items": {
                                                        "type": "string",
                                                        "example": "The field_name field is required."
                                                    }
                                                }
                                            },
                                            "type": "object"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            },
            "delete": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Удалить пакет",
                "operationId": "6a2868f86198583eccc274707be9af00",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID пакета",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Успешное удаление",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "required": [
                                        "success"
                                    ],
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/{package}/renew": {
            "post": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Продлить пакет",
                "operationId": "1b74b86743ddc972fc98a2e11477fa2e",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID пакета",
                        "required": true
                    }
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "properties": {
                                    "promo": {
                                        "type": "string"
                                    }
                                },
                                "type": "object"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Успешное продление тарифа",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "required": [
                                        "success",
                                        "message"
                                    ],
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "message": {
                                            "type": "integer",
                                            "example": "Успешно",
                                            "nullable": true
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "402": {
                        "description": "Недостаточно средств",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string"
                                        },
                                        "error": {
                                            "type": "string"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/{package}/auto-update": {
            "post": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Включение/выключение автообновления",
                "operationId": "532059ca4b323bf2dff6890c1cc01c37",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID пакета",
                        "required": true
                    }
                ],
                "requestBody": {
                    "required": true,
                    "content": {
                        "application/json": {
                            "schema": {
                                "required": [
                                    "auto_update"
                                ],
                                "properties": {
                                    "auto_update": {
                                        "type": "boolean",
                                        "example": true
                                    }
                                },
                                "type": "object"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Успешное включение/выключение автообновления",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "required": [
                                        "success"
                                    ],
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/{package}/upgrade": {
            "get": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Опции апгрейда пакета",
                "operationId": "c376d904c06b3586ed7f474efa28d7bb",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Upgrade Residential Unlim packages and prices",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "data": {
                                            "properties": {
                                                "id": {
                                                    "type": "integer"
                                                },
                                                "price": {
                                                    "type": "number"
                                                },
                                                "speed_limit": {
                                                    "type": "number"
                                                },
                                                "duration_days": {
                                                    "type": "number"
                                                },
                                                "name": {
                                                    "type": "string"
                                                }
                                            },
                                            "type": "object"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            },
            "post": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Апгрейд пакета",
                "operationId": "a5ca62fb5b20ca5425cd29096c329996",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "properties": {
                                    "tariff_id": {
                                        "type": "integer"
                                    }
                                },
                                "type": "object"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Успешный апгрейд тарифа",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "required": [
                                        "success",
                                        "message"
                                    ],
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "message": {
                                            "type": "string"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/{package}/usage": {
            "get": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Метрики пакета",
                "operationId": "e2c416e49d913263e90d9d301a669bfd",
                "parameters": [
                    {
                        "name": "package",
                        "in": "path",
                        "description": "ID of the package",
                        "required": true
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Метрики пакета",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "required": [
                                        "success",
                                        "message"
                                    ],
                                    "properties": {
                                        "success": {
                                            "type": "boolean"
                                        },
                                        "message": {
                                            "type": "string"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/locations": {
            "get": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Локации для Residential Unlim",
                "operationId": "ba91707603ec71396c256bf8e2f6a45a",
                "responses": {
                    "200": {
                        "description": "Доступные локации",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "data": {
                                            "type": "object"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/reseller/residential-unlim/locations": {
            "get": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Локации для Residential Unlim",
                "operationId": "406d5c7f72fbb45c25efced36e4bc327",
                "responses": {
                    "200": {
                        "description": "Доступные локации",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "data": {
                                            "type": "object"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Не авторизован",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "message": {
                                            "type": "string",
                                            "example": "Unauthenticated."
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/residential-unlim/countries": {
            "get": {
                "tags": [
                    "Residential Unlim"
                ],
                "summary": "Страны для Residential Unlim",
                "operationId": "5d523c5d3cac732306952f543a1613e6",
                "responses": {
                    "200": {
                        "description": "Доступные страны",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "properties": {
                                        "data": {
                                            "properties": {
                                                "id": {
                                                    "type": "integer"
                                                },
                                                "name": {
                                                    "type": "string"
                                                },
                                                "iso2": {
                                                    "type": "string"
                                                },
                                                "cities": {
                                                    "type": "array",
                                                    "items": {
                                                        "properties": {
                                                            "name": {
                                                                "type": "string"
                                                            },
                                                            "code": {
                                                                "type": "string"
                                                            }
                                                        },
                                                        "type": "object"
                                                    }
                                                }
                                            },
                                            "type": "object"
                                        }
                                    },
                                    "type": "object"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/reseller/get/packages": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "resellerGetPackages",
                "parameters": [
                    {
                        "name": "start_date",
                        "in": "query",
                        "description": "Start date of range",
                        "required": false,
                        "schema": {
                            "type": "string"
                        }
                    },
                    {
                        "name": "end_date",
                        "in": "query",
                        "description": "End date of range",
                        "required": false,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            },
            "delete": {
                "tags": [
                    "Residential"
                ],
                "operationId": "deleteProxyList",
                "parameters": [
                    {
                        "name": "list_id",
                        "in": "query",
                        "description": "List ID",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/update/package": {
            "put": {
                "tags": [
                    "Residential"
                ],
                "operationId": "resellerUpdatePackage",
                "parameters": [
                    {
                        "name": "package_key",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/countries": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getCountries",
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/geolocation": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getAllGeolocation",
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/regions": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getRegions",
                "parameters": [
                    {
                        "name": "country_code",
                        "in": "query",
                        "description": "Country code",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/cities": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getCities",
                "parameters": [
                    {
                        "name": "country_code",
                        "in": "query",
                        "description": "Country code",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    },
                    {
                        "name": "region_name",
                        "in": "query",
                        "description": "Region name",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/lists": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getLists",
                "parameters": [
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/lists/reseller": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getListsReseller",
                "parameters": [
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/proxy": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getProxy",
                "parameters": [
                    {
                        "name": "list_name",
                        "in": "query",
                        "description": "List name",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    },
                    {
                        "name": "list_id",
                        "in": "query",
                        "description": "List id",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    },
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/proxy/reseller": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getProxyReseller",
                "parameters": [
                    {
                        "name": "list_name",
                        "in": "query",
                        "description": "List name",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    },
                    {
                        "name": "list_id",
                        "in": "query",
                        "description": "List id",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    },
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/create/proxy": {
            "post": {
                "tags": [
                    "Residential"
                ],
                "operationId": "createProxy",
                "parameters": [
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/create/proxy/reseller": {
            "post": {
                "tags": [
                    "Residential"
                ],
                "operationId": "createProxyReseller",
                "parameters": [
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/tariffs": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getTariffs",
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "data": [
                                            {
                                                "tariff_id": 1,
                                                "name": "string",
                                                "price": "string",
                                                "traffik": "string"
                                            }
                                        ]
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/get/balance": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getBalance",
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/info/package": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "infoPackage",
                "parameters": [
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/info/package/reseller": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "infoPackageReseller",
                "parameters": [
                    {
                        "name": "packagekey",
                        "in": "query",
                        "description": "Package key",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/buy/package": {
            "post": {
                "tags": [
                    "Residential"
                ],
                "operationId": "buyPackage",
                "parameters": [
                    {
                        "name": "package_id",
                        "in": "query",
                        "description": "Package id",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/buy/package/reseller": {
            "post": {
                "tags": [
                    "Residential"
                ],
                "operationId": "resellerBuyPackage",
                "parameters": [
                    {
                        "name": "traffik",
                        "in": "query",
                        "description": "Traffik volume",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        },
        "/api/reseller/tools": {
            "get": {
                "tags": [
                    "Residential"
                ],
                "operationId": "getTools",
                "parameters": [
                    {
                        "name": "package",
                        "in": "query",
                        "description": "Package",
                        "required": true,
                        "schema": {
                            "type": "string"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {},
                                "example": {
                                    "result": {
                                        "status": 200,
                                        "message": "string"
                                    }
                                }
                            }
                        }
                    }
                },
                "security": [
                    {
                        "api_key": []
                    }
                ]
            }
        }
    },
    "components": {
        "schemas": {
            "GetPackageResponse": {
                "title": "GetPackageResponse",
                "properties": {
                    "expired_at": {
                        "type": "string"
                    },
                    "is_suspended": {
                        "type": "boolean"
                    },
                    "traffic_limit_common": {
                        "type": "number",
                        "format": "float"
                    },
                    "traffic_usage_common": {
                        "type": "number",
                        "format": "float"
                    },
                    "package_key": {
                        "type": "string"
                    },
                    "package_status": {
                        "type": "string"
                    }
                },
                "type": "object"
            },
            "Alert": {
                "title": "Alert",
                "required": [
                    "id",
                    "is_active",
                    "name",
                    "type",
                    "description",
                    "created_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "is_active": {
                        "type": "integer",
                        "example": 1
                    },
                    "name": {
                        "type": "string",
                        "example": "Название алерта"
                    },
                    "type": {
                        "type": "string",
                        "example": "Тип алерта warning/error/info"
                    },
                    "description": {
                        "type": "string",
                        "example": "Описание алерта"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-08-01 00:00:00"
                    }
                },
                "type": "object"
            },
            "FaqByCategory": {
                "title": "FaqByCategory",
                "required": [
                    "id",
                    "title",
                    "faqs",
                    "created_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "title": {
                        "type": "string",
                        "example": "Title"
                    },
                    "faqs": {
                        "type": "array",
                        "items": {
                            "$ref": "#/components/schemas/Faq"
                        }
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-08-01 00:00:00"
                    }
                },
                "type": "object"
            },
            "Faq": {
                "title": "Faq",
                "required": [
                    "id",
                    "is_active",
                    "children",
                    "title",
                    "content",
                    "created_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "is_active": {
                        "type": "integer",
                        "example": 1
                    },
                    "children": {
                        "type": "array",
                        "items": {
                            "$ref": "#/components/schemas/Faq"
                        }
                    },
                    "title": {
                        "type": "string",
                        "example": "Mой вопрос"
                    },
                    "content": {
                        "description": "Контент ответа в виду html",
                        "type": "string",
                        "example": "<h1>Мой ответ</h1>"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-08-01 00:00:00"
                    }
                },
                "type": "object"
            },
            "InfaticaPackage": {
                "title": "InfaticaPackage",
                "required": [
                    "id",
                    "user_id",
                    "tariff_id",
                    "package_key",
                    "status",
                    "expired_at",
                    "renew",
                    "del",
                    "auto_update",
                    "created_at",
                    "updated_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "user": {
                        "$ref": "#/components/schemas/User"
                    },
                    "tariff": {
                        "$ref": "#/components/schemas/Tariff"
                    },
                    "package_key": {
                        "type": "string",
                        "example": "323ewfsd4523"
                    },
                    "status": {
                        "type": "string",
                        "example": "active"
                    },
                    "expired_at": {
                        "type": "string",
                        "example": "2024-08-01 00:00:00"
                    },
                    "renew": {
                        "type": "integer",
                        "example": 1
                    },
                    "del": {
                        "type": "integer",
                        "example": 0
                    },
                    "auto_update": {
                        "type": "integer",
                        "example": 0
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    },
                    "updated_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "PricePoint": {
                "title": "PricePoint",
                "required": [
                    "traffic",
                    "price"
                ],
                "properties": {
                    "traffic": {
                        "type": "integer",
                        "example": 1
                    },
                    "price": {
                        "type": "number",
                        "format": "float",
                        "example": 10.5
                    }
                },
                "type": "object"
            },
            "NotificationSetting": {
                "title": "NotificationSetting",
                "required": [
                    "id",
                    "type",
                    "settings"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "type": {
                        "type": "string",
                        "example": "package"
                    },
                    "settings": {
                        "type": "array",
                        "items": {
                            "properties": {
                                "name": {
                                    "type": "string",
                                    "example": "package_buy_notification"
                                },
                                "channels": {
                                    "type": "array",
                                    "items": {
                                        "properties": {
                                            "channel": {
                                                "type": "string",
                                                "example": "database"
                                            },
                                            "enabled": {
                                                "type": "boolean",
                                                "example": true
                                            }
                                        },
                                        "type": "object"
                                    }
                                }
                            },
                            "type": "object"
                        }
                    }
                },
                "type": "object"
            },
            "Notification": {
                "title": "Notification",
                "required": [
                    "id",
                    "status",
                    "type",
                    "status",
                    "tariff_name",
                    "expired_at",
                    "created_at",
                    "package_key"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "type": {
                        "type": "string",
                        "example": "App\\Notifications\\PackageBuyNotification"
                    },
                    "notifiable_type": {
                        "type": "string",
                        "example": "package"
                    },
                    "data": {
                        "type": "object",
                        "example": {
                            "key": "value"
                        }
                    },
                    "read_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    },
                    "updated_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "Order": {
                "title": "Order",
                "required": [
                    "id",
                    "merchant",
                    "amount",
                    "status",
                    "system_name",
                    "currency_name",
                    "created_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "merchant": {
                        "type": "string",
                        "example": "EnotAPI"
                    },
                    "amount": {
                        "type": "number",
                        "format": "float",
                        "example": 1.34
                    },
                    "status": {
                        "type": "string",
                        "example": "Успешно"
                    },
                    "crypto_amount": {
                        "type": "number",
                        "format": "float",
                        "example": 2.38
                    },
                    "system_name": {
                        "type": "string",
                        "example": "TRON"
                    },
                    "currency_name": {
                        "type": "string",
                        "example": "TRON"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "PrivateProxyPackage": {
                "title": "PrivateProxyPackage",
                "required": [
                    "id",
                    "user_id",
                    "tariff_id",
                    "uuid",
                    "status",
                    "duration_days",
                    "speed_limit",
                    "location_id",
                    "proxy_ip",
                    "expires_at",
                    "login",
                    "password",
                    "del",
                    "created_at",
                    "updated_at",
                    "usage"
                ],
                "properties": {
                    "id": {
                        "description": "Transform the resource into an array.",
                        "type": "integer",
                        "example": 1
                    },
                    "user": {
                        "$ref": "#/components/schemas/User"
                    },
                    "tariff": {
                        "$ref": "#/components/schemas/Tariff"
                    },
                    "order_id": {
                        "type": "integer",
                        "example": "123"
                    },
                    "status": {
                        "type": "string",
                        "example": "active"
                    },
                    "duration_days": {
                        "type": "integer",
                        "example": 30
                    },
                    "purpose_id": {
                        "type": "integer",
                        "example": 1
                    },
                    "package_id": {
                        "type": "integer",
                        "example": 1
                    },
                    "coutnry": {
                        "type": "string",
                        "example": "RU"
                    },
                    "login": {
                        "type": "string",
                        "example": "proxymaoffice"
                    },
                    "password": {
                        "type": "string",
                        "example": "12345678"
                    },
                    "ip_count": {
                        "type": "integer",
                        "example": 1
                    },
                    "ip_list": {
                        "type": "array",
                        "items": {
                            "type": "string"
                        }
                    },
                    "expires_at": {
                        "type": "string",
                        "example": "2024-08-01 00:00:00"
                    },
                    "auto_update": {
                        "type": "boolean",
                        "example": true
                    },
                    "free_swaps": {
                        "type": "integer",
                        "example": 1
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    },
                    "updated_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "UserPackage": {
                "title": "UserPackage",
                "required": [
                    "id",
                    "status",
                    "type",
                    "status",
                    "tariff_name",
                    "expired_at",
                    "created_at",
                    "package_key"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "status": {
                        "type": "string",
                        "example": "active"
                    },
                    "type": {
                        "description": "isp или dynamic",
                        "type": "string",
                        "example": "isp"
                    },
                    "tariff_name": {
                        "type": "string",
                        "example": "Startuna"
                    },
                    "package_key": {
                        "type": "string",
                        "example": "12312312",
                        "nullable": true
                    },
                    "auto_update": {
                        "type": "string",
                        "example": true,
                        "nullable": true
                    },
                    "expired_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53",
                        "nullable": true
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "ProxyPlaneUnlimPackage": {
                "title": "ProxyPlaneUnlimPackage",
                "required": [
                    "id",
                    "user_id",
                    "tariff_id",
                    "uuid",
                    "status",
                    "duration_days",
                    "speed_limit",
                    "location_id",
                    "proxy_ip",
                    "expires_at",
                    "login",
                    "password",
                    "del",
                    "created_at",
                    "updated_at",
                    "usage"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "user": {
                        "$ref": "#/components/schemas/User"
                    },
                    "tariff": {
                        "$ref": "#/components/schemas/Tariff"
                    },
                    "uuid": {
                        "type": "sting",
                        "example": "dasd8aday123-dasdasd12-dasdasd3"
                    },
                    "status": {
                        "type": "string",
                        "example": "active"
                    },
                    "duration_days": {
                        "type": "integer",
                        "example": 30
                    },
                    "speed_limit": {
                        "type": "integer",
                        "example": 100
                    },
                    "location_id": {
                        "type": "integer",
                        "example": 1
                    },
                    "proxy_ip": {
                        "type": "string",
                        "example": "244.178.44.111"
                    },
                    "expires_at": {
                        "type": "string",
                        "example": "2024-08-01 00:00:00"
                    },
                    "login": {
                        "type": "string",
                        "example": "proxymaoffice"
                    },
                    "password": {
                        "type": "string",
                        "example": "12345678"
                    },
                    "traffic": {
                        "type": "number",
                        "format": "float",
                        "example": 1
                    },
                    "del": {
                        "type": "integer",
                        "example": 0
                    },
                    "auto_update": {
                        "type": "boolean",
                        "example": true
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    },
                    "usage": {
                        "type": "integer",
                        "example": 12313
                    }
                },
                "type": "object"
            },
            "MyReferral": {
                "title": "MyReferral",
                "required": [
                    "referral_id",
                    "amount",
                    "paid_at",
                    "created_at"
                ],
                "properties": {
                    "referral_id": {
                        "type": "integer",
                        "example": 1
                    },
                    "amount": {
                        "type": "number",
                        "format": "float",
                        "example": 1.34
                    },
                    "paid_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "Setting": {
                "title": "Setting",
                "properties": {
                    "is_show": {
                        "description": "Показывать ли баннер?",
                        "type": "boolean"
                    },
                    "banner_title": {
                        "description": "Название баннера",
                        "type": "string"
                    },
                    "banner_description": {
                        "description": "Описание баннера",
                        "type": "string"
                    },
                    "banner_image": {
                        "description": "Изображение баннера",
                        "type": "string"
                    },
                    "banner_link": {
                        "description": "Ссылка на баннере",
                        "type": "string"
                    }
                },
                "type": "object"
            },
            "Transaction": {
                "title": "Order",
                "required": [
                    "id",
                    "amount",
                    "type",
                    "comment",
                    "created_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "amount": {
                        "type": "number",
                        "format": "float",
                        "example": 1.34
                    },
                    "type": {
                        "type": "string",
                        "example": "type"
                    },
                    "comment": {
                        "type": "string",
                        "example": "comment"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "Withdrawal": {
                "title": "Withdrawal",
                "required": [
                    "id",
                    "amount",
                    "status",
                    "address",
                    "created_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "amount": {
                        "type": "number",
                        "format": "float",
                        "example": 1.34
                    },
                    "address": {
                        "type": "string",
                        "example": "TBaMGHXyQ8N5mWK4G1H39po3pu9soCDgy6"
                    },
                    "status": {
                        "type": "string",
                        "example": "Успешно"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10 18:22:53"
                    }
                },
                "type": "object"
            },
            "Tariff": {
                "title": "Tariff",
                "required": [
                    "id",
                    "title",
                    "price",
                    "traffic",
                    "per_gb",
                    "ports",
                    "show",
                    "border",
                    "header_color",
                    "type",
                    "is_test",
                    "created_at",
                    "updated_at"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "title": {
                        "type": "string",
                        "example": "Nebula"
                    },
                    "price": {
                        "type": "number",
                        "format": "float",
                        "example": 10
                    },
                    "traffic": {
                        "type": "integer",
                        "example": 10
                    },
                    "per_gb": {
                        "type": "number",
                        "example": 10
                    },
                    "ports": {
                        "type": "integer",
                        "example": 100
                    },
                    "show": {
                        "type": "integer",
                        "example": 1
                    },
                    "border": {
                        "type": "string",
                        "example": "#343EF7"
                    },
                    "header_item": {
                        "type": "string",
                        "example": "Item",
                        "nullable": true
                    },
                    "header_color": {
                        "type": "string",
                        "example": "#FFFFFF"
                    },
                    "type": {
                        "type": "integer",
                        "example": 1
                    },
                    "is_test": {
                        "type": "boolean",
                        "example": true
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10T18:22:53.000000Z"
                    },
                    "updated_at": {
                        "type": "string",
                        "example": "2024-02-10T18:22:53.000000Z"
                    }
                },
                "type": "object"
            },
            "User": {
                "title": "User",
                "required": [
                    "id",
                    "name",
                    "email",
                    "role"
                ],
                "properties": {
                    "id": {
                        "type": "integer",
                        "example": 1
                    },
                    "name": {
                        "type": "string",
                        "example": "John Doe"
                    },
                    "email": {
                        "type": "string",
                        "example": "john.doe@example.com"
                    },
                    "role": {
                        "type": "integer",
                        "example": 1
                    },
                    "status": {
                        "type": "string",
                        "example": "active"
                    },
                    "telegram": {
                        "type": "string",
                        "example": "@john.doe",
                        "nullable": true
                    },
                    "invited": {
                        "type": "integer",
                        "example": 2,
                        "nullable": true
                    },
                    "ref_link": {
                        "type": "string",
                        "example": "gqiR563",
                        "nullable": true
                    },
                    "balance": {
                        "type": "number",
                        "example": 1099
                    },
                    "referral_balance": {
                        "type": "number",
                        "example": 10.1
                    },
                    "api_key": {
                        "type": "string",
                        "example": "2345ghf",
                        "nullable": true
                    },
                    "referral_reward": {
                        "type": "number",
                        "example": 10
                    },
                    "locale": {
                        "type": "string",
                        "example": "ru"
                    },
                    "created_at": {
                        "type": "string",
                        "example": "2024-02-10T18:22:53.000000Z"
                    },
                    "updated_at": {
                        "type": "string",
                        "example": "2024-02-10T18:22:53.000000Z"
                    }
                },
                "type": "object"
            }
        },
        "securitySchemes": {
            "api_key": {
                "type": "apiKey",
                "description": "API ключ для авторизации",
                "name": "api-key",
                "in": "header"
            }
        }
    },
    "tags": [
        {
            "name": "ISP",
            "description": "ISP"
        },
        {
            "name": "Residential Unlim",
            "description": "Residential Unlim"
        },
        {
            "name": "Residential",
            "description": "Residential"
        }
    ]
}
