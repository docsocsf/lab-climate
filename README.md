labclimate
==========

Database Table Description (Assuming Postgresql)
------------------------------------------------

### **data** table:

| Field Name  | Field Type |
|-------------|------------|
| node\_id    | bigint     |
| timestamp   | timestamp  |
| temperature | double     |
| humidity    | double     |
| air\_qual   | double     |


### **nodes** table:

| Field Name     | Field Type   |
|----------------|--------------|
| node\_id       | bigint       |
| node\_location | varchar(256) |


API Endpoints
---------------

| Method | Endpoint         | Usage                                          |
|--------|------------------|------------------------------------------------|
| GET    | /config          | Gets the client configuration from the server. |
| POST   | /data/{id}       | Submits climate data to the server.            |
| POST   | /nodes           | Adds a new node to the server.                 |
| DELETE | /nodes/{id}      | Deletes a node from the server.                |
| PUT    | /nodes/{id}      | Updates the location of a node on the server.  |


### GET /config response (*JSON*) \*TODO\*:

time\_interval: {time\_interval} (Time interval between submissions)

### POST /data/{id} body (*JSON*):

node\_id:    {node id} 

temperature: {temperature}

humididty:   {humidity}

air\_qual:   {air quality value}

timestamp:   {timestamp}

### POST /nodes body (*JSON*):

node\_id:       {node id}

node\_location: {location}

### PUT /nodes/{id} body (*JSON*):

node\_location: {location}



