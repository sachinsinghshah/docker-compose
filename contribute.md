## Manual installation 
 - Install nodejs locally ()
 - clone the repo
 - Install dependencies  (`npm install`)
 - Start the DB locally 
    - `docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres`
    - or else  get it from neon.tech
 - change the .env file and update your DB Creds
 - `npx prisma migrate`
 - `npx prisma generate`
 - `npm run build`
 - `npm run start`


 ## Docker Installation (Better way)
 - Install docker
 - Create a network - `docker network create user_project`

 - Start postgres
    - `docker run --network user_project --name postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres`
 - Build the image - `docker build --network=host -t user-project .` 
 - start the image - `docker run -e DATABASE_URL="postgresql://postgres:mysecretpassword@postgres:5432/postgres" --network user_project -p 3000:3000 user-project`
 
 
 ## Docker Compose installation steps (Best Way)
 - Install docker, docker-compose
 - Run it `docker-compose up`

