
# Lem-in

  

Lem-in is a simulation tool written in Go for modeling ant movement through an anthill. The project parses a configuration file to initialize the environment and then simulates the movement of ants from a start room to an end room.

  

## Features

  

- Parse and initialize rooms and tunnels from a configuration file.

- Simulate the movement of ants through the anthill.

- Display the number of turns required for all ants to reach the end room.

  

## Installation

  

1.  **Clone the Repository:**

  

```bash

git clone https://github.com/your-username/lem-in.git

cd lem-in
```

2.  **Build the Project:**

  

```bash

go build
```
  

## Usage

Run the simulation with a configuration file using the following command:

  

```bash

./lem-in  path/to/config.txt

  ```

**Configuration File Format**

The  configuration  file  should  include  the  following  sections:

  

1.  Number  of  Ants:  An  integer  representing  the  total  number  of  ants.

2.  Start  Room:  The  starting  room  in  the  format  name  x  y.

3.  Rooms:  Definitions  of  rooms  in  the  format  name  x  y.

4.  End  Room:  The  destination  room  in  the  format  name  x  y.

5.  Tunnels:  Connections  between  rooms  in  the  format  room1-room2.

  
  

**Example Configuration:**
```
5

start  0  0

room1  1  1

room2  2  2

end 3 3

start-room1

room1-room2

room2-end
```
  
  

**Project Structure**

-  `main.go`:  Entry  point  for  the  application

-  `src/process.go`  :  Manages  the  simulation  flow

-  `src/antmethod.go`  :  Handles  ant  movement.

-  `src/anthill.go`:  Defines  the  rooms,  tunnels,  and  anthill  structure.

-  `src/utils/`:  Contains  utility  functions  for  file  handling  and  parsing.

-  `src/structs/`:  Defines  data  structures  for  ants,  rooms,  and  tunnels.

  

##License

  

This  project  is  licensed  under  the  MIT  License.  See  the  LICENSE  file  for  details.
