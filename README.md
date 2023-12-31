# Membuat API Contact User Management

## Requirement
1. User Management
2. Contact Management
3. Address Management


## User Management Requirement
1. Username
2. Password
3. Name

### User API
1. Register User
2. Login User
3. Update User
4. Get User
5. Logout User


## Contact Management Requirement
1. First Name
2. Last Name
3. Email
4. Phone

### Contact API
1. Create Contact
2. Update Contact
3. Get Contact
4. Search Contact
5. Remove Contact


## Contact Address Data
1. Street
2. City
3. Province
4. Country
5. Postal Code

### Contact Address API
1. Create Address
2. Update Address
3. Get Address
4. List Address
5. Remove Address



## Membuat Project
1. Buat folder belajar-nodejs-restfull-api
2. jalankan ```npm init```
3. Buka file package.json dan tambahkan type module


```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC"
}

```


## Menambah Dependensi
### Menambahkan Package Joi 
1. Untuk Validasi
2. npm install joi


```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "joi": "^17.9.2"
  }
}

```

### Menambahkan Package Express Js
1. npm install express : untuk rest api
2. npm install --save-dev @types/express : untuk autocomplete text editor kita

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.18.2",
    "joi": "^17.9.2"
  },
  "devDependencies": {
    "@types/express": "^4.17.17"
  }
}

```

### Menambahkan Package Prisma
1.  Untuk database
2.  npm install --save-dev prisma

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.18.2",
    "joi": "^17.9.2"
  },
  "devDependencies": {
    "@types/express": "^4.17.17",
    "prisma": "^4.15.0"
  }
}

```

### Menambahkan Package Winston
1. Untuk Logger
2. npm install winston

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@types/express": "^4.17.17",
    "prisma": "^4.15.0"
  }
}

```

### menambahkan Package BCrypt
1. Algoritma untuk melakukan hashing
2. Untuk menyimpan password ke database
3. npm install bcrypt
4. npm install --save-dev @types/bcrypt

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.0",
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@types/bcrypt": "^5.0.0",
    "@types/express": "^4.17.17",
    "prisma": "^4.15.0"
  }
}
```


### Menambahkan Package UUID
1. Universal Uniq Identifier
2. Untuk membuat string uniq
3. npm install uuid
4. npm install --save-dev @types/uuid


```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.0",
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "uuid": "^9.0.0",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@types/bcrypt": "^5.0.0",
    "@types/express": "^4.17.17",
    "@types/uuid": "^9.0.2",
    "prisma": "^4.15.0"
  }
}

```

## Setup Unit Test

### Menambahkan Package Jest
1. Untuk unit test
2. npm install --save-dev jest @types/jest

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.0",
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "uuid": "^9.0.0",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@types/bcrypt": "^5.0.0",
    "@types/express": "^4.17.17",
    "@types/jest": "^29.5.2",
    "@types/uuid": "^9.0.2",
    "jest": "^29.5.0",
    "prisma": "^4.15.0"
  }
}

```


### Menambahkan Package Babel
1. Karena menggunakan javascript type modul jest tidak mendukung ini.
2. Dengan demikian kita tambahkan babel untuk mentranslate ketika dijalankan oleh jest nya.
3. npm install --save-de babel-jest @babel/preset-env
4. https://babeljs.io/setup#installation

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.0",
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "uuid": "^9.0.0",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@babel/preset-env": "^7.22.5",
    "@types/bcrypt": "^5.0.0",
    "@types/express": "^4.17.17",
    "@types/jest": "^29.5.2",
    "@types/uuid": "^9.0.2",
    "babel-jest": "^29.5.0",
    "jest": "^29.5.0",
    "prisma": "^4.15.0"
  }
}

```

### Setup Babel

Tambahkan script ini ke dalam file package.json:

```json
"scripts": {
    "test": "jest"
  },
  "jest": {
    "transform": {
      "^.+\\.[t|j]sx?$": "babel-jest"
    }
  },
```

menjadi:

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "jest"
  },
  "jest": {
    "transform": {
      "^.+\\.[t|j]sx?$": "babel-jest"
    }
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.0",
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "uuid": "^9.0.0",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@babel/preset-env": "^7.22.5",
    "@types/bcrypt": "^5.0.0",
    "@types/express": "^4.17.17",
    "@types/jest": "^29.5.2",
    "@types/uuid": "^9.0.2",
    "babel-jest": "^29.5.0",
    "jest": "^29.5.0",
    "prisma": "^4.15.0"
  }
}
```

selanjutnya buat konfigurasi file ```babel.config.json``` :

```json
{
  "presets": ["@babel/preset-env"]
}
```

biasanya jest berjalan secara paralel, agar dapat berjalan secara sequential kita ubah script di package.json :

```json
"scripts": {
    "test": "jest -i"
},

```

### menambahkan Package Supertest
1. Untuk mempermudah melakukan testing express js
2. npm install --save-dev supertest @types/supertest


```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "test": "jest -i"
  },
  "jest": {
    "transform": {
      "^.+\\.[t|j]sx?$": "babel-jest"
    }
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.0",
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "uuid": "^9.0.0",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@babel/preset-env": "^7.22.5",
    "@types/bcrypt": "^5.0.0",
    "@types/express": "^4.17.17",
    "@types/jest": "^29.5.2",
    "@types/supertest": "^2.0.12",
    "@types/uuid": "^9.0.2",
    "babel-jest": "^29.5.0",
    "jest": "^29.5.0",
    "prisma": "^4.15.0",
    "supertest": "^6.3.3"
  }
}

```


## API Spec

### 1. User API Spec

#### Register User

Endpoint: POST /api/users

Request Body:

```json
{
  "username" : "test-user",
  "password" : "rahasia",
  "name"  : "Test User"
}
```

Response Body Success:


```json
{
  "status": true,
  "data": {
      "username" : "test-user",
      "name"  : "Test User"
  }
}
```

Response Body Errors:

```json
{
  "status": false,
  "errors": "Username already registered"
}
```


#### Login User

Endpoint: POST /api/users/login

Request Body:

```json
{
  "username" : "test-user",
  "password" : "rahasia"
}
```

Response Body Success:

```json
{
  "status": true,
  "data": {
      "token" : "uniq-token"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Username or password wrong"
}
```

#### Update User

Endpoint: PATCH /api/users/current

Headers:
- Authorization : token

Request Body:

```json
{
  "name": "Test Users",           // optional
  "new_password" : "rahasia"      // optional
}
```

Response Body Success:

```json
{
  "status": true,
  "data": {
      "username" : "test-user",
      "name": "Test User"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Name length max 100"
}
```

#### Get User

Endpoint: GET /api/users/current

Headers:
- Authorization : token

Response Body Success:

```json
{
  "status": true,
  "data": {
      "username" : "test-user",
      "name": "Test User"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Unauthorized"
}
```

#### Logout User

Endpoint: DELETE /api/users/logout

Headers:
- Authorization : token

Response Body Success:

```json
{
  "status": true,
  "data": "OK"
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Unauthorized"
}
```


### 2. Contact API Spec

#### Create Contact API

Endpoint: POST /api/contacts

Headers:
- Authorization : token


Request Body:

```json
{
  "first_name": "test-name",
  "last_name": "test-name",
  "phone_number":"1234565767",
  "email": "test@email.com"
}
```

Response Body Success:

```json
{
  "status": true,
  "data": {
    "id":1,
    "first_name": "test-name",
    "last_name": "test-name",
    "phone_number":"1234565767",
    "email": "test@email.com"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Email is not valid format"
}
```

#### Update Contact API

Endpoint: PUT /api/contacts/:id

Headers:
- Authorization : token


Request Body:

```json
{
  "first_name": "test-name",
  "last_name": "test-name",
  "phone_number":"1234565767",
  "email": "test@email.com"
}
```

Response Body Success:

```json
{
  "status": true,
  "data": {
    "id":1,
    "first_name": "test-name",
    "last_name": "test-name",
    "phone_number":"1234565767",
    "email": "test@email.com"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Email is not valid format"
}
```

#### Get Contact API

Endpoint: GET /api/contacts

Headers:
- Authorization : token

Response Body Success:

```json
{
  "status": true,
  "data": {
    "id":1,
    "first_name": "test-name",
    "last_name": "test-name",
    "phone_number":"1234565767",
    "email": "test@email.com"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Contact is not found"
}
```

#### Search Contact API

Endpoint: GET /api/contacts

Headers:
- Authorization : token

Query params:
- name: Search by first_name or last_name, using like, optional
- email: Search by email, using like, optional
- phone: Search by phone, using like, optional
- page: number of page, default 1
- size: size of page, default 10

Response Body Success:

```json
{
  "status": true,
  "data": [{
    "id":1,
    "first_name": "test-name",
    "last_name": "test-name",
    "phone_number":"1234565767",
    "email": "test@email.com"
  }, {
    "id":2,
    "first_name": "test-name",
    "last_name": "test-name",
    "phone_number":"1234565767",
    "email": "test@email.com"
  }, {
    "id":3,
    "first_name": "test-name",
    "last_name": "test-name",
    "phone_number":"1234565767",
    "email": "test@email.com"
  }],
  "page": 1,
  "total_page": 3,
  "total_item": 30
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Email is not valid format"
}
```

#### Remove Contact API


Endpoint: DELETE /api/contacts/:id

Headers:
- Authorization : token


Response Body Success:

```json
{
  "status": true,
  "data": "OK"
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Contact is not found"
}
```



### 3. Address API Spec
#### Create Address API

Endpoint: POST /api/contacts/:contactId/addresses

Headers:
- Authorization : token


Request Body:

```json
{
  "street": "Jl. Cibarusa",
  "city": "Bandung",
  "province":"Jawa Barat",
  "country": "Indonesia",
  "postal_code": "551234"
}
```

Response Body Success:

```json
{
  "status": true,
  "data": {
    "id":1,
    "street": "Jl. Cibarusa",
    "city": "Bandung",
    "province":"Jawa Barat",
    "country": "Indonesia",
    "postal_code": "551234"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Coutry is required"
}
```

#### Update Address API

Endpoint: PUT /api/contacts/:contactId/addresses/:addressId

Headers:
- Authorization : token


Request Body:

```json
{
  "street": "Jl. Cibarusa",
  "city": "Bandung",
  "province":"Jawa Barat",
  "country": "Indonesia",
  "postal_code": "551234"
}
```

Response Body Success:

```json
{
  "status": true,
  "data": {
    "id":1,
    "street": "Jl. Cibarusa",
    "city": "Bandung",
    "province":"Jawa Barat",
    "country": "Indonesia",
    "postal_code": "551234"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Coutry is required"
}
```

#### Get Address API

Endpoint: GET /api/contacts/:contactId/addresses/:addressId

Headers:
- Authorization : token

Response Body Success:

```json
{
  "status": true,
  "data": {
    "id":1,
    "street": "Jl. Cibarusa",
    "city": "Bandung",
    "province":"Jawa Barat",
    "country": "Indonesia",
    "postal_code": "551234"
  }
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Contact is not found"
}
```

#### List Address API

Endpoint: GET /api/contacts/:contactId/addresses

Headers:
- Authorization : token

Response Body Success:

```json
{
  "status": true,
  "data": [{
      "id":1,
      "street": "Jl. Cibarusa",
      "city": "Bandung",
      "province":"Jawa Barat",
      "country": "Indonesia",
      "postal_code": "551234"
    },{
      "id":2,
      "street": "Jl. Cibarusa",
      "city": "Bandung",
      "province":"Jawa Barat",
      "country": "Indonesia",
      "postal_code": "551234"
    },{
      "id":3,
      "street": "Jl. Cibarusa",
      "city": "Bandung",
      "province":"Jawa Barat",
      "country": "Indonesia",
      "postal_code": "551234"
    }]
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Contact is not found"
}
```

#### Remove Address API


Endpoint: GET /api/contacts/:contactId/addresses/:addressId

Headers:
- Authorization : token

Response Body Success:

```json
{
  "status": true,
  "data": "OK"
}
```

Response Body Error:

```json
{
  "status": false,
  "errors": "Contact is not found"
}
```


## Prisma

### Setup Prisma
1. Jalankan perintah: ```npx prisma init```
2. Setup .env :
   
  ```env
  DATABASE_URL="mysql://root:12345@localhost:3306/restful_api_db"
  ```

### User Model

```prisma
// This is your Prisma schema file,
// learn more about it in the docs: https://pris.ly/d/prisma-schema

generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

model User {
  username String  @id @db.VarChar(100)
  password String  @db.VarChar(100)
  name     String  @db.VarChar(100)
  token    String? @db.VarChar(100)

  @@map("users")
}

```


Misal kita lupa, kita dapat melakukan ini:

```bash
$ npx prisma --help

◭  Prisma is a modern DB toolkit to query, migrate and model your database (https://prisma.io)

Usage

  $ prisma [command]

Commands

            init   Set up Prisma for your app
        generate   Generate artifacts (e.g. Prisma Client)
              db   Manage your database schema and lifecycle
         migrate   Migrate your database
          studio   Browse your data with Prisma Studio
        validate   Validate your Prisma schema
          format   Format your Prisma schema

Flags

     --preview-feature   Run Preview Prisma commands

Examples

  Set up a new Prisma project
  $ prisma init

  Generate artifacts (e.g. Prisma Client)
  $ prisma generate

  Browse your data
  $ prisma studio

  Create migrations from your Prisma schema, apply them to the database, generate artifacts (e.g. Prisma Client)
  $ prisma migrate dev
  
  Pull the schema from an existing database, updating the Prisma schema
  $ prisma db pull

  Push the Prisma schema state to the database
  $ prisma db push

  Validate your Prisma schema
  $ prisma validate

  Format your Prisma schema
  $ prisma format
```


```bash
$ npx prisma migrate --help

Update the database schema with migrations
  
Usage

  $ prisma migrate [command] [options]

Commands for development

         dev   Create a migration from changes in Prisma schema, apply it to the database
               trigger generators (e.g. Prisma Client)
       reset   Reset your database and apply all migrations, all data will be lost

Commands for production/staging

      deploy   Apply pending migrations to the database 
      status   Check the status of your database migrations
     resolve   Resolve issues with database migrations, i.e. baseline, failed migration, hotfix

Command for any stage

        diff   Compare the database schema from two arbitrary sources

Options

  -h, --help   Display this help message
    --schema   Custom path to your Prisma schema

Examples

  Create a migration from changes in Prisma schema, apply it to the database, trigger generators (e.g. Prisma Client)
  $ prisma migrate dev

  Reset your database and apply all migrations
  $ prisma migrate reset

  Apply pending migrations to the database in production/staging
  $ prisma migrate deploy

  Check the status of migrations in the production/staging database
  $ prisma migrate status

  Specify a schema
  $ prisma migrate status --schema=./schema.prisma

  Compare the database schema from two databases and render the diff as a SQL script
  $ prisma migrate diff \
    --from-url "$DATABASE_URL" \
    --to-url "postgresql://login:password@localhost:5432/db" \
    --script
```

```bash
$ npx prisma migrate dev --help

🏋️  Create a migration from changes in Prisma schema, apply it to the database, trigger generators (e.g. Prisma Client)
 
Usage

  $ prisma migrate dev [options]

Options

       -h, --help   Display this help message
         --schema   Custom path to your Prisma schema
       -n, --name   Name the migration
    --create-only   Create a new migration but do not apply it
                    The migration will be empty if there are no changes in Prisma schema
  --skip-generate   Skip triggering generators (e.g. Prisma Client)
      --skip-seed   Skip triggering seed

Examples

  Create a migration from changes in Prisma schema, apply it to the database, trigger generators (e.g. Prisma Client)
  $ prisma migrate dev

  Specify a schema
  $ prisma migrate dev --schema=./schema.prisma

  Create a migration without applying it
  $ prisma migrate dev --create-only

```


Mari kita jalankan migration tanpa eksekusi ke database: 

```bash
$ npx prisma migrate dev --create-only
Environment variables loaded from .env
Prisma schema loaded from prisma/schema.prisma
Datasource "db": MySQL database "restful_api_db" at "localhost:3306"

MySQL database restful_api_db created at localhost:3306

✔ Enter a name for the new migration: … first_migrate
Prisma Migrate created the following migration without applying it 20230614094418_first_migrate

You can now edit it and apply it by running prisma migrate dev.
```

Hasil migrasi dapat di lihat di folder ```prisma/migrations/``` , kita bisa cek di file .sql nya:

```mysql
-- CreateTable
CREATE TABLE `users` (
    `username` VARCHAR(100) NOT NULL,
    `password` VARCHAR(100) NOT NULL,
    `name` VARCHAR(100) NOT NULL,
    `token` VARCHAR(100) NULL,

    PRIMARY KEY (`username`)
) DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

```


Ketika hasil migrasi sudah sesuai, mari kita lakukan migrasi ke database, dengan perintah:

```bash
$ npx prisma migrate dev

Environment variables loaded from .env
Prisma schema loaded from prisma/schema.prisma
Datasource "db": MySQL database "restful_api_db" at "localhost:3306"

Applying migration `20230614094418_first_migrate`

The following migration(s) have been applied:

migrations/
  └─ 20230614094418_first_migrate/
    └─ migration.sql

Your database is now in sync with your schema.

Running generate... (Use --skip-generate t
o skip the generators)
(⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂) ⠦ idealTree:restful-c(⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂) ⠦ idealTree:restful-c(⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂) ⠦ idealTree:restful-c(#########⠂⠂⠂⠂⠂⠂⠂⠂⠂) ⠇ idealTree: timing i

added 2 packages, and audited 542 packages in 25s

42 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

✔ Generated Prisma Client (4.15.0 | librar
y) to ./node_modules/@prisma/client in 484
ms
```




### Contact Model

```prisma
// This is your Prisma schema file,
// learn more about it in the docs: https://pris.ly/d/prisma-schema

generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "mysql"
  url      = env("DATABASE_URL")
}

model User {
  username String    @id @db.VarChar(100)
  password String    @db.VarChar(100)
  name     String    @db.VarChar(100)
  token    String?   @db.VarChar(100)
  contacts Contact[]

  @@map("users")
}

model Contact {
  id         Int     @id @default(autoincrement())
  first_name String  @db.VarChar(100)
  last_name  String? @db.VarChar(100)
  email      String? @db.VarChar(200)
  phone      String? @db.VarChar(20)
  username   String  @db.VarChar(100)
  user       User    @relation(fields: [username], references: [username])

  @@map("contacts")
}

```

```mysql
-- CreateTable
CREATE TABLE `contacts` (
    `id` INTEGER NOT NULL AUTO_INCREMENT,
    `first_name` VARCHAR(100) NOT NULL,
    `last_name` VARCHAR(100) NULL,
    `email` VARCHAR(200) NULL,
    `phone` VARCHAR(20) NULL,
    `username` VARCHAR(100) NOT NULL,

    PRIMARY KEY (`id`)
) DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- AddForeignKey
ALTER TABLE `contacts` ADD CONSTRAINT `contacts_username_fkey` FOREIGN KEY (`username`) REFERENCES `users`(`username`) ON DELETE RESTRICT ON UPDATE CASCADE;


```


### Address Model


```prisma
// This is your Prisma schema file,
// learn more about it in the docs: https://pris.ly/d/prisma-schema

generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "mysql"
  url      = env("DATABASE_URL")
}

model User {
  username String    @id @db.VarChar(100)
  password String    @db.VarChar(100)
  name     String    @db.VarChar(100)
  token    String?   @db.VarChar(100)
  contacts Contact[]

  @@map("users")
}

model Contact {
  id         Int       @id @default(autoincrement())
  first_name String    @db.VarChar(100)
  last_name  String?   @db.VarChar(100)
  email      String?   @db.VarChar(200)
  phone      String?   @db.VarChar(20)
  username   String    @db.VarChar(100)
  user       User      @relation(fields: [username], references: [username])
  addresses  Address[]

  @@map("contacts")
}

model Address {
  id          Int     @id @default(autoincrement())
  street      String? @db.VarChar(255)
  city        String? @db.VarChar(100)
  province    String? @db.VarChar(100)
  country     String? @db.VarChar(100)
  postal_code String? @db.VarChar(10)
  contact_id  Int
  contact     Contact @relation(fields: [contact_id], references: [id])
}

```

```mysql
-- CreateTable
CREATE TABLE `Address` (
    `id` INTEGER NOT NULL AUTO_INCREMENT,
    `street` VARCHAR(255) NULL,
    `city` VARCHAR(100) NULL,
    `province` VARCHAR(100) NULL,
    `country` VARCHAR(100) NULL,
    `postal_code` VARCHAR(10) NULL,
    `contact_id` INTEGER NOT NULL,

    PRIMARY KEY (`id`)
) DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- AddForeignKey
ALTER TABLE `Address` ADD CONSTRAINT `Address_contact_id_fkey` FOREIGN KEY (`contact_id`) REFERENCES `contacts`(`id`) ON DELETE RESTRICT ON UPDATE CASCADE;

```


## Setup Project

### Setup Prisma
Mari kita buat file database.js di folder src/application :

```js
// Singleton
import { PrismaClient } from "@prisma/client";

export const prismaClient = new PrismaClient()
```


### Setup Winston

Mari kita buat file logging.js di folder src/application :

```js
import winston from "winston/lib/winston/config";

export const logger = winston.createLogger({
    level: "info",
    format: winston.format.json(),
    transports:[
        new winston.transports.Console({})
    ]
}) 
```

### Setup Express

Mari kita buat file web.js di folder src/application :

```js
import express from "express"

export const web = express()
web.use(express.json())
```


### Setup Prisma Logging

dokumentasi: https://www.prisma.io/docs/concepts/components/prisma-client/working-with-prismaclient/logging


Secara default log prisma akan dikirimkan ke stdout.

```js
const prisma = new PrismaClient({
  log: ['query', 'info', 'warn', 'error'],
})
```


```js
const prisma = new PrismaClient({
  log: [
    {
      emit: 'stdout',
      level: 'query',
    },
    {
      emit: 'stdout',
      level: 'error',
    },
    {
      emit: 'stdout',
      level: 'info',
    },
    {
      emit: 'stdout',
      level: 'warn',
    },
  ],
})

```

Kita bisa ganti dari stdout ke tempat lain, kita bisa ganti yang default nya ```stdout``` kita ganti menjadi ```event```:

```js
const prisma = new PrismaClient({
  log: [
    {
      emit: 'event',
      level: 'query',
    },
    {
      emit: 'stdout',
      level: 'error',
    },
    {
      emit: 'stdout',
      level: 'info',
    },
    {
      emit: 'stdout',
      level: 'warn',
    },
  ],
})

prisma.$on('query', (e) => {
  console.log('Query: ' + e.query)
  console.log('Params: ' + e.params)
  console.log('Duration: ' + e.duration + 'ms')
})

```

Ubah di file database.js

```js
import { PrismaClient } from "@prisma/client";
import {logger} from "./logging.js"


export const prismaClient = new PrismaClient({
  log: [
    {
      emit: 'event',
      level: 'query',
    },
    {
      emit: 'event',
      level: 'error',
    },
    {
      emit: 'event',
      level: 'info',
    },
    {
      emit: 'event',
      level: 'warn',
    },
  ],
})


prismaClient.$on('error', (e)=>{
    logger.error(e);
})

prismaClient.$on('warn', (e)=>{
    logger.warn(e);
})

prismaClient.$on('info', (e)=>{
    logger.info(e);
})

prismaClient.$on('query', (e)=>{
    logger.info(e);
})
```


## Register User API

### Membuat Validation

Mari kita buat file ```user-validation.js``` di folder ```src/validation/``` :

```js

import Joi from "joi"

const registerUserValidation = Joi.object({
    username: Joi.string().max(100).required(),
    password: Joi.string().max(100).required(),
    name: Joi.string().max(100).required(),
});

export {
    registerUserValidation
}
```

Mari kita buat file  ```validation.js``` di folder ```src/validation/``` :


```js
import { ErrorHandling } from "../error/error-handling.js"

const validate = (schema, request)=>{
    const result = schema.validate(request, {
        abortEarly: false
    })
    if(result.error){
        throw new ErrorHandling(400, result.error.message)
    } else {
        return result.value
    }
}

export {
    validate
}
```


### Membuat User Service

Mari kita buat file  ```error-handling.js``` di folder ```src/error/``` :

```js

class ErrorHandling extends Error{

    constructor(status, message){
        super(message)
        this.status = status
    }
}

export{
    ErrorHandling
}

```

Mari kita buat file  ```user-service.js``` di folder ```src/service/``` :

```js
import { registerUserValidation } from "../validation/user-validation.js"
import { validate } from "./../validation/validation.js"
import {prismaClient} from "./../application/databases.js"
import { ErrorHandling } from "../error/error-handling.js"
import bcrypt from "bcrypt"
import { logger } from "../application/logging.js"

const register = async (request)=>{
    try{
        // validate
        const user = validate(registerUserValidation, request)

        // check user
        const countUser = await prismaClient.user.count({
            where:{
                username: user.username
            }
        })

        if(countUser===1){
            throw new ErrorHandling(400, "Username already exist")
        }

        // hashing password
        user.password = await bcrypt.hash(user.password, 10)


        // query ke database

        return await prismaClient.user.create({
            data: user,
            select:{
                username: true, 
                name: true
            }
        })

    } catch(error){
        if(process.env.DEBUG){
            logger.error("error user service register", error)
        }
        throw new ErrorHandling(400, "error user service register")
    }
}

export default {
    register
}
```


### Membuat User Controller

Mari kita buat file  ```user-controller.js``` di folder ```src/controller/``` :

```js
import userService from "../service/user-service.js"


const register = async(req, res, next)=>{
    try{
        const result = await userService.register(req.body)
        res.status(200).json({
            data: result
        })
    } catch(error){
        next(error)
    }
}

export default {
    register
}
```


Mari kita buat file  ```public-api.js``` di folder ```src/route/``` :


```js
import express from "express"
import userController from "../controller/user-controller.js"


const publicRouter = new express.Router();
publicRouter.post('/api/users', userController.register)

export {
    publicRouter
}
```

Tambahkan di file ```src/application/web.js``` menjadi seperti ini:

```js
import express from "express"
import { publicRouter } from "../route/public-api.js"

export const web = express()
web.use(express.json())

web.use(publicRouter)

```

Tambahkan di file ```src/middleware/error-middleware.js``` menjadi seperti ini:

```js
import { ErrorHandling } from "../error/error-handling.js"
import {ValidationError} from "joi"

const errorMiddleware = async (error, req, res, next)=>{

    if(!error){
        next()
        return
    }

    if(error instanceof ErrorHandling){
        res.status(error.status).json({
            status: false,
            errors: error.message
        }).end()
    } else if(error instanceof ValidationError){
        res.status(400).json({
            status: false,
            errors: error.message
        }).end()
    } else{
        res.status(500).json({
            status: false,
            errors: error.message
        }).end()
    }

}

export {
    errorMiddleware
}
```


Tambahkan di file ```src/application/web.js``` menjadi seperti ini:

```js
import express from "express"
import { publicRouter } from "../route/public-api.js"
import { errorMiddleware } from "../middleware/error-middleware.js"

export const web = express()
web.use(express.json())
web.use(publicRouter)
web.use(errorMiddleware)

```


### Membuat Main Javascript File


Tambahkan di file ```src/main.js``` menjadi seperti ini:

```js
import {web} from "./application/web.js"
import { logger } from "./application/logging.js"

const port = process.env.PORT || 3000

web.listen(port, ()=>{
    logger.info(`Restful start in port ${port}`)
})
```

Tambahkan di file ```.env``` menjadi seperti ini:

```env
DEBUG=true
PORT=3000
DATABASE_URL="mysql://root:12345@localhost:3306/restful_api_db"

```

Tambahkan di file ```package.json``` menjadi seperti ini:

```json
{
  "name": "restful-contact-management",
  "version": "1.0.0",
  "description": "Node Js Restful API",
  "main": "src/main.js",
  "scripts": {
    "start": "node src/main.js",
    "dev": "nodemon src/main.js",
    "test": "jest -i"
  },
  "jest": {
    "transform": {
      "^.+\\.[t|j]sx?$": "babel-jest"
    }
  },
  "type": "module",
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "@prisma/client": "^4.15.0",
    "bcrypt": "^5.1.0",
    "express": "^4.18.2",
    "joi": "^17.9.2",
    "uuid": "^9.0.0",
    "winston": "^3.9.0"
  },
  "devDependencies": {
    "@babel/preset-env": "^7.22.5",
    "@types/bcrypt": "^5.0.0",
    "@types/express": "^4.17.17",
    "@types/jest": "^29.5.2",
    "@types/supertest": "^2.0.12",
    "@types/uuid": "^9.0.2",
    "babel-jest": "^29.5.0",
    "jest": "^29.5.0",
    "nodemon": "^2.0.22",
    "prisma": "^4.15.0",
    "supertest": "^6.3.3"
  }
}
```


### Unit Test

Buat file user.test.js di folder test/ :

user.test.js

 ```js
import { prismaClient } from "../src/application/databases.js"
import supertest from "supertest"
import {web} from "../src/application/web.js"
import {logger} from "../src/application/logging.js"

describe('POST /api/users', ()=>{

    // Setelah test selesai, hapus data nya
    afterEach(async ()=>{
        await prismaClient.user.deleteMany({
            where:{
                username: 'test'
            }
        });
    })

    it('should can register new user', async ()=>{

        const result = await supertest(web).post('/api/users').send({
            username: 'test',
            password: 'rahasia',
            name:'test'
        });

        expect(result.status).toBe(200);
        expect(result.body.data.username).toBe('test');
        expect(result.body.data.name).toBe('test');
        expect(result.body.data.password).toBeUndefined();

    });

    it('should reject if request is invalid', async ()=>{

        const result = await supertest(web).post('/api/users').send({
            username: '',
            password: '',
            name:''
        });

        logger.info(result.body)

        expect(result.status).toBe(400);
        expect(result.body.errors).toBeDefined();

    })


    it('should reject if username already registered', async ()=>{

        let result = await supertest(web).post('/api/users').send({
            username: 'test',
            password: 'rahasia',
            name:'test'
        });

        expect(result.status).toBe(200);
        expect(result.body.data.username).toBe('test');
        expect(result.body.data.name).toBe('test');
        expect(result.body.data.password).toBeUndefined();


        result = await supertest(web).post('/api/users').send({
            username: 'test',
            password: 'rahasia',
            name:'test'
        });

        logger.info(result.body)

        expect(result.status).toBe(400);
        expect(result.body.errors).toBeDefined();

    });
    
})

 ```



## API Login

### Tambahkan Validation

```user-validation.js```

```js
import Joi from "joi"

const registerUserValidation = Joi.object({
    username: Joi.string().max(100).required(),
    password: Joi.string().max(100).required(),
    name: Joi.string().max(100).required(),
});

const loginUserValidation = Joi.object({
    username: Joi.string().max(100).required(),
    password: Joi.string().max(100).required()
});

export {
    registerUserValidation, 
    loginUserValidation
}
```

validation.js

```js

import { ErrorHandling } from "../error/error-handling.js"

const validate = (schema, request)=>{
    const result = schema.validate(request, {
        abortEarly: false,      // dicek semua field
        allowUnknown: false     // field yang tak diketahui
    })
    if(result.error){
        throw new ErrorHandling(400, result.error.message)
    } else {
        return result.value
    }
}

export {
    validate
}

```

### Tambahkan di user-service.js

user-service.js

```js
import { loginUserValidation, registerUserValidation } from "../validation/user-validation.js"
import { validate } from "./../validation/validation.js"
import {prismaClient} from "./../application/databases.js"
import { ErrorHandling } from "../error/error-handling.js"
import bcrypt from "bcrypt"
import { logger } from "../application/logging.js"
import {v4 as uuid} from "uuid"


const register = async (request)=>{
    try{
        // validate
        const user = validate(registerUserValidation, request)

        // check user
        const countUser = await prismaClient.user.count({
            where:{
                username: user.username
            }
        })

        if(countUser===1){
            throw new ErrorHandling(400, "Username already exist")
        }

        // hashing password
        user.password = await bcrypt.hash(user.password, 10)


        // query ke database

        return await prismaClient.user.create({
            data: user,
            select:{
                username: true, 
                name: true
            }
        })

    } catch(error){
        if(process.env.DEBUG){
            logger.error("error user service register", error)
        }
        throw new ErrorHandling(400, "error user service register")
    }
}

const login = async(request)=>{
    try{
        const loginRequest = validate(loginUserValidation, request);

        // check user
        const user = await prismaClient.user.findUnique({
            where: {
                username: loginRequest.username
            },
            select:{
                username: true,
                password: true
            }
        });


        if(!user){
            throw new ErrorHandling(401, "Username or password wrong");
        }

        // check password
        const isPasswordValid = await bcrypt.compare(loginRequest.password, user.password);
        if(!isPasswordValid){
            throw new ErrorHandling(401, "Username or password wrong");
        }

        // membuat token
        const token = uuid().toString

        return prismaClient.user.update({
            data:{
                token: token
            }, 
            where:{
                username: user.username
            },
            select: {
                token: true
            }
        });



    }catch(error){
        if(process.env.DEBUG){
            logger.error("error user service login", error);
        }
        throw new ErrorHandling(400, "error user service login");
    }
}

export default {
    register, login
}
```


### Tambahkan di file user-controller.js

user-controller.js

```js
import userService from "../service/user-service.js"


const register = async(req, res, next)=>{
    try{
        const result = await userService.register(req.body)
        res.status(200).json({
            data: result
        })
    } catch(error){
        next(error)
    }
}

const login = async(req, res, next)=>{
    try{
        const result = await userService.login(req.body)
        res.status(200).json({
            data: result
        })
    } catch(error){
        next(error)
    }
}


export default {
    register, login
}
```

public-api.js


```js
import express from "express"
import userController from "../controller/user-controller.js"


const publicRouter = new express.Router();
publicRouter.post('/api/users', userController.register)
publicRouter.post('/api/users/login', userController.login)

export {
    publicRouter
}

```

### Unit Test
 
user.test.js


 ```js
import { prismaClient } from "../src/application/databases.js"
import supertest from "supertest"
import {web} from "../src/application/web.js"
import {logger} from "../src/application/logging.js"
import { createTestUser, removeTestUser } from "./test-util.js"

describe('POST /api/users', ()=>{

    // Setelah test selesai, hapus data nya
    afterEach(async ()=>{
        await removeTestUser()
    })

    it('should can register new user', async ()=>{

        const result = await supertest(web).post('/api/users').send({
            username: 'test',
            password: 'rahasia',
            name:'test'
        });

        expect(result.status).toBe(200);
        expect(result.body.data.username).toBe('test');
        expect(result.body.data.name).toBe('test');
        expect(result.body.data.password).toBeUndefined();

    });

    it('should reject if request is invalid', async ()=>{

        const result = await supertest(web).post('/api/users').send({
            username: '',
            password: '',
            name:''
        });

        logger.info(result.body)

        expect(result.status).toBe(400);
        expect(result.body.errors).toBeDefined();

    })


    it('should reject if username already registered', async ()=>{

        let result = await supertest(web).post('/api/users').send({
            username: 'test',
            password: 'rahasia',
            name:'test'
        });

        expect(result.status).toBe(200);
        expect(result.body.data.username).toBe('test');
        expect(result.body.data.name).toBe('test');
        expect(result.body.data.password).toBeUndefined();


        result = await supertest(web).post('/api/users').send({
            username: 'test',
            password: 'rahasia',
            name:'test'
        });

        logger.info(result.body)

        expect(result.status).toBe(400);
        expect(result.body.errors).toBeDefined();

    });
    
});

describe('POST /api/users/login', ()=>{

    beforeEach(async ()=>{
        await createTestUser();
    });

    afterEach(async ()=>{
        await removeTestUser();
    });


    it('should can login', async()=>{
        const result = await supertest(web).post('/api/users/login').send({
            username: 'test',
            password: 'rahasia'
        });

        logger.info(result);

        expect(result.status).toBe(200);
        expect(result.body.data.token).toBeDefined();
        expect(result.body.data.token).not.toBe('test');
    });


    it('should reject login if request is invalid', async()=>{
        const result = await supertest(web).post('/api/users/login').send({
            username: '',
            password: ''
        });

        logger.info(result);

        expect(result.status).toBe(400);
        expect(result.body.errors).toBeDefined();
    });

    it('should reject login if password is wrong', async()=>{
        const result = await supertest(web).post('/api/users/login').send({
            username: 'test',
            password: 'salah'
        });

        logger.info(result);

        expect(result.status).toBe(401);
        expect(result.body.errors).toBeDefined();
    });


    it('should reject login if username is wrong', async()=>{
        const result = await supertest(web).post('/api/users/login').send({
            username: 'salah',
            password: 'rahasia'
        });

        logger.info(result);

        expect(result.status).toBe(401);
        expect(result.body.errors).toBeDefined();
    });


})

 ```


test-utils.js

```js
import { prismaClient } from "../src/application/databases.js";
import bcrypt from 'bcrypt';

const removeTestUser = async() =>{
    await prismaClient.user.deleteMany({
        where:{
            username: 'test'
        }
    });
}


const createTestUser = async() =>{
    await prismaClient.user.create({
        data:{
            username: 'test',
            password: await bcrypt.hash('rahasia',10),
            name: 'test',
            token: 'test'
        }
    })
}

export{
    removeTestUser, createTestUser
}
```



## Get User API

### Validation

user-validation.js

```js
import Joi from "joi"

const registerUserValidation = Joi.object({
    username: Joi.string().max(100).required(),
    password: Joi.string().max(100).required(),
    name: Joi.string().max(100).required(),
});

const loginUserValidation = Joi.object({
    username: Joi.string().max(100).required(),
    password: Joi.string().max(100).required()
});


const getUserValidation = Joi.string.max(100).required();

export {
    registerUserValidation, 
    loginUserValidation,
    getUserValidation
}

```


### Services

user-service.js

```js

import { getUserValidation, loginUserValidation, registerUserValidation } from "../validation/user-validation.js"
import { validate } from "./../validation/validation.js"
import {prismaClient} from "./../application/databases.js"
import { ErrorHandling } from "../error/error-handling.js"
import bcrypt from "bcrypt"
import { logger } from "../application/logging.js"
import {v4 as uuid} from "uuid"


const register = async (request)=>{
    // validate
    const user = validate(registerUserValidation, request)

    // check user
    const countUser = await prismaClient.user.count({
        where:{
            username: user.username
        }
    })

    if(countUser===1){
        throw new ErrorHandling(400, "Username already exist")
    }

    // hashing password
    user.password = await bcrypt.hash(user.password, 10)


    // query ke database

    return await prismaClient.user.create({
        data: user,
        select:{
            username: true, 
            name: true
        }
    })
}

const login = async(request)=>{
    const loginRequest = validate(loginUserValidation, request);

    // check user
    const user = await prismaClient.user.findUnique({
        where: {
            username: loginRequest.username
        },
        select:{
            username: true,
            password: true
        }
    });


    if(!user){
        throw new ErrorHandling(401, "Username or password wrong");
    }

    // check password
    const isPasswordValid = await bcrypt.compare(loginRequest.password, user.password);
    if(!isPasswordValid){
        throw new ErrorHandling(401, "Username or password wrong");
    }

    // membuat token
    const token = uuid().toString()

    return prismaClient.user.update({
        data:{
            token: token
        }, 
        where:{
            username: user.username
        },
        select: {
            token: true
        }
    });
}


const getUser = async(username)=>{
    username = validate(getUserValidation, username);

    const user = await prismaClient.user.findUnique({
        where:{
            username: username
        },
        select:{
            username: true, 
            name: true
        }
    });

    if(!user){
        throw new ErrorHandling(404, "User is not found");
    }

    return user;

}

export default {
    register,
    login, 
    getUser
}

```


### Controller

```js
import userService from "../service/user-service.js"

const test = async (req, res, next)=>{
    try{
        res.status(200).json({
            data: "test"
        })
    } catch(error){
        next(error)
    }
}

const register = async(req, res, next)=>{
    try{
        const result = await userService.register(req.body)
        res.status(200).json({
            data: result
        })
    } catch(error){
        next(error)
    }
}

const login = async(req, res, next)=>{
    try{
        const result = await userService.login(req.body)
        res.status(200).json({
            status: true,
            data: result
        })
    } catch(error){
        next(error)
    }
}


const getUser = async(req, res, next)=>{
    try{
        const username = req.user.username;
        const result = await userService.getUser(username);
        res.status(200).json({
            status: true,
            data: result
        })

    } catch(error){
        next(error);
    }
}


export default {
    register, login, test
}

```

auth-middleware.js

```js
import { prismaClient } from "../application/databases";

export const authMiddleware = async(req, res, next)=>{
    const token = req.get('Authorization');

    if(!token){
        res.status(401).json({
            status: false,
            errors: 'Unauthorized'
        }).end();
    } 

    const user = await prismaClient.user.findFirst({
            where:{
                token:token
            }
        });

    if(!user){
        res.status(401).json({
            status: false,
            errors: 'Unauthorized'
        }).end();
    }

    req.user = user;
    next();
}
```


api.js

```js

import express from "express"
import userController from "../controller/user-controller.js"
import { authMiddleware } from "../middleware/auth-middleware.js";


const userRouter = new express.Router();
userRouter(authMiddleware);
userRouter.get('/api/users/current', userController.getUser)


export {
    userRouter
}

```

web.js

```js
import express from "express"
import { publicRouter } from "../route/public-api.js"
import { errorMiddleware } from "../middleware/error-middleware.js"
import { userRouter } from "../route/api.js"

export const web = express()
web.use(express.json())
web.use(publicRouter)
web.use(errorMiddleware)
web.use(userRouter)

```


### Unit Test

```js


```




## Reference:

https://www.youtube.com/watch?v=6v8JXecArqE