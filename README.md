# Eos-icon![Screenshot from 2022-01-04 19-59-06](https://user-images.githubusercontent.com/94596249/148074051-50cedf94-eed0-4ff2-811c-f28004cffc2d.png)
Enhancing Backend and introduction of new features for EOS icons
## Eos-icon picker
[Open Source Love svg2](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)
![Screenshot from 2022-01-04 19-10-53](https://user-images.githubusercontent.com/94596249/148072612-edb81ce9-470b-46fd-9e1d-b383ebf90fdc.png)


### | Main changes:
The code got refactored/re-written in typescript.
The system is now depending on the Mongo database as main source of truth.
Caching layer is introduced to make the process of fetching the icons faster.
Algolia services is introduced to be used for the search queries.
A validation layer using Joi is added to validate all the incoming requests.
A unit tests using Mocha and Chai are written to ensure that all the new APIs are working as expected.
A Docker image is created to encapsulate everything for easier running and deployment process.

## Running the project

- Cloning the repo:
````
git clone https://github.com/EOS-uiux-Solutions/eos-icons-api
````
- Once the repository is cloned, You can choose the way you prfer: 


### | Technologies used in project:
Typescript, javascript,Node.js, Docker, MongoDB, Redis, Algolia, Mocha, Gitlab hooks, Github workflows.

## Installations:
  **Steps to Follow**
   Install the required python dependencies:

      - On Linux: 
        ```
        sudo apt-get install fontforge ttfautohint
        ``` 
  
   - Install MongoDB Compass:
    https://www.how2shout.com/linux/install-mongodb-compass-gui-in-ubuntu-20-04-lts-linux/
   - Install Visual Studio
    https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-18-04/
   - Install MongoDB: 
    https://linuxize.com/post/how-to-install-mongodb-on-ubuntu-20-04/
    https://www.youtube.com/watch?v=WH5GgHaEy7E&t=46s
   - Install Redis: 
    https://redis.io/download
    https://www.youtube.com/watch?v=gNPgaBugCWk
   - Install Mocha
    https://riptutorial.com/mocha/example/27433/installation-or-setup
   - Install Chai
    https://www.npmjs.com/package/chai
   - Install joi : npm install joi

### | Using Docker: 
  By using our docker image, we will take care of everything</br> 
  - **Steps**:
    - Install docker using'https://docs.docker.com/engine/install/ubuntu/'
    - Modify the `REDISCLOUD_URL` enviroment variable to `redis://redis:6379` in the environment variable folder.
    - Modify the `MongoURI` enviroment variable to `mongodb://mongo:27017/eosiconsdb` in the environment variable folder.
    - From within the cloned respository run the following command to build the image: </br>
  ````
  docker-compose up
  ````
  - Your server container will be started at `http://localhost:3131`
  - Mongo database can be accessed from MongoDB compass at `mongodb://mongo:27017/eosiconsdb`
  
 ## Running on machine:
   - - Install the dependenices and run the server: 
    1. Install dependencies using `npm install`
    2. Install grunt globally `npm install -g grunt-cli`
    3. Start the server using `npm start`
    - Your server will be started at `http://localhost:3131`
    
- Run the tests after any modification, or add new one for any addition. 
1. For `V1` APIs we're using Postman tests, which can be started using `npm run test:v1`
2. For `V2` APIs we're using Mocha tests, which can be started using `npm run test:v2`
3. Test All the APIs using `npm run test` 




