# Befor I die

Befor I die is digital version of [Before I die project](https://beforeidieproject.com). 

This board is an extension of the [lovasoa/whitebophir](https://github.com/lovasoa/whitebophir) project.

A demonstration server is available at [beforeidie.libraryofpeople.com](https://beforeidie.libraryofpeople.com).

<!-- ## Screenshots

<table>
 <tr>
  <td> The <i><a href="https://wbo.ophir.dev/boards/anonymous">anonymous</a></i> board
  <td> <img width="300" src="https://user-images.githubusercontent.com/552629/59885574-06e02b80-93bc-11e9-9150-0670a1c5d4f3.png">
  <td> collaborative diagram editing
  <td> <img alt="Screenshot of WBO's user interface: architecture" width="300" src="https://user-images.githubusercontent.com/552629/59915054-07101380-941c-11e9-97c9-4980f50d302a.png" />
  
  <tr>
   <td> teaching math on <b>WBO</b>
   <td> <img alt=wbo teaching" width="300" src="https://user-images.githubusercontent.com/552629/59915737-a386e580-941d-11e9-81ff-db9e37f140db.png" />
   <td> drawing art
   <td> <img alt="angel drawn on WBO" width="300" src="https://user-images.githubusercontent.com/552629/59914139-08404100-941a-11e9-9c29-bd2569fe4730.png"/>
</table> -->

## Running your own instance of WBO

If you have your own web server, and want to run a private instance of WBO on it, you can. It should be very easy to get it running on your own server.

### Running the code in a container (safer)

If you use the [docker](https://www.docker.com/) containerization service, you can easily run WBO as a container. 
An official docker image for WBO is hosted on dockerhub as [`lovasoa/wbo`](https://hub.docker.com/repository/docker/lovasoa/wbo).

You can run it with the following command :

```
docker run -it --publish 5001:80 --volume $(pwd)/wbo-boards:/opt/app/server-data lovasoa/wbo:latest
```

This will run WBO :
 - on port 5001
 - persisting the user data in `$(pwd)/wbo-boards`

You can then access WBO at `http://localhost:5001`.

### Running the code without a container

Alternatively, you can run the code with [node.js](https://nodejs.org/) directly, without docker.

First, download the sources:
```
git clone git@github.com:lovasoa/whitebophir.git
cd whitebophir
```

Then [install node.js](https://nodejs.org/en/download/) if you don't have it already, then install WBO's dependencies:
```
npm install
```

Finally, you can start the server:
```
PORT=5001 npm start
```

This will run WBO directly on your machine, on port 5001, without any isolation from the other services.


<small>Demonstration server hosted by [openode](https://www.openode.io/)</small>
