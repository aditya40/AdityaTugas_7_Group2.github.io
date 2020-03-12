# AdityaTugas_7_Group2.github.io

FORMAT: 1A
HOST: https://polls.apiblueprint.org/

# Photo Gallery API

Simple API allowing consumers to view photos, comments and contact persons.

## Photo [/photo]

### List All Photos [GET]

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "caption": "caption 1",
                "url": "photos.com/gallery/1",
                "contact_id": "1"
            },
            {
                "id": "2",
                "caption": "caption 2",
                "url": "photos.com/gallery/2",
                "contact_id": "2"
            },
            {
                "id": "3",
                "caption": "caption 3",
                "url": "photos.com/gallery/3",
                "contact_id": "3"
            }
        ]

### Create New Photo [POST]

+ Request (application/json)

        {
            "caption": "caption 4",
            "url": "photos.com/gallery/4",
            "contact_id": "3"
        }

+ Response 201 (application/json)

    + Headers

            Location: /photo/4

    + Body

            {
                "id": "4",
                "caption": "caption 4",
                "url": "photos.com/gallery/4",
                "contact_id": "3"
            }
            
## Photos Resource [/photo/{id}]

+ Parameters
    + id : 1 (number, required) - An unique identifier of the message

### List Photo with ID [GET]


+ Response 200 (application/json)

        [
            {
                "id": "1",
                "caption": "caption 1",
                "url": "photos.com/gallery/1",
                "contact_id": "1"
            }
        ]

### Edit a Photo [PATCH]


+ Request (application/json)

        {
            "caption": "caption 1a"
        }

+ Response 201 (application/json)

        [
            {
                "id": "1",
                "caption": "caption 1a",
                "url": "photos.com/gallery/1",
                "contact_id": "1"
            }
        ]
        
### Delete a Photo [DELETE]

+ Response 204


## Photo Comments [/comment]

### List All Photo Comments [GET]


+ Response 200 (application/json)

        [
            {
                "id": "1",
                "content": "content 1",
                "photo_id": "1",
                "contact_id": "1"
            },
            {
                "id": "2",
                "content": "content 2",
                "photo_id": "2",
                "contact_id": "2"
            },
            {
                "id": "3",
                "content": "content 3",
                "photo_id": "3",
                "contact_id": "3"
            }
        ]

### Create New Photo Comment [POST]

+ Request (application/json)

        {
            "content": "content 4",
            "photo_id": "3",
        }

+ Response 201 (application/json)

    + Headers

            Location: /comment/4

    + Body

            {
                "id": "4",
                "content": "content 4",
                "photo_id": "3",
                "contact_id": "3"
            }
            
## Photo Comments Resource [/comment/{id}]

+ Parameters
    + id : 1 (number, required) - An unique identifier of the message

### List Photo Comment with ID [GET]


+ Response 200 (application/json)

        [
            {
                "id": "1",
                "content": "content 1",
                "photo_id": "1",
                "contact_id": "1"
            }
        ]

### Edit a Photo Comment [PATCH]


+ Request (application/json)

        {
            "content": "content 1a"
        }

+ Response 201 (application/json)

        [
            {
                "id": "1",
                "content": "content 1",
                "photo_id": "1",
                "contact_id": "1"
            }
        ]
        
### Delete a Photo Comment [DELETE]


+ Response 204


## Contacts [/contact]

### List All Contacts [GET]


+ Response 200 (application/json)

        [
            {
                "id": "1",
                "username": "absalim",
                "password": "absalim12345",
                "email": "absalim@gmail.com",
                "full_name": "Abdul Salim"
            },
            {
                "id": "2",
                "username": "nadyarich",
                "password": "nadya12345",
                "email": "nadyarich@gmail.com",
                "full_name": "Nadya Richna"
            },
            {
                "id": "3",
                "username": "tjahtjah",
                "password": "tjahtjah12345",
                "email": "tjahtjah@gmail.com",
                "full_name": "Indra Tjahyadi"
            }
        ]

### Create New Contact [POST]


+ Request (application/json)

        {
            "username": "fahmi_nur",
            "password": "fahmi12345",
            "email": "fahmi@gmail.com",
            "full_name": "Fahmi Nur"
        }

+ Response 201 (application/json)

    + Headers

            Location: /contact/4

    + Body

            {
                "id": "4",
                "username": "fahmi_nur",
                "password": "fahmi12345",
                "email": "fahmi@gmail.com",
                "full_name": "Fahmi Nur"
            }
            
## Contacts Resource [/contact/{id}]

+ Parameters
    + id : 1 (number, required) - An unique identifier of the message

### List Post with ID [GET]

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "username": "absalim",
                "password": "absalim12345",
                "email": "absalim@gmail.com",
                "full_name": "Abdul Salim"
            }
        ]

### Edit a Contact [PATCH]

+ Request (application/json)

        {
            "email": "abdsalim@gmail.com"
        }

+ Response 201 (application/json)

        [
            {
                "id": "1",
                "username": "absalim",
                "password": "absalim12345",
                "email": "abdsalim@gmail.com",
                "full_name": "Abdul Salim"
            }
        ]
        
### Delete a Contact [DELETE]


+ Response 204
