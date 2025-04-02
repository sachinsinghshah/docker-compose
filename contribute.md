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


 ## Docker Installation (better way)
 - ## Docker Compose installation steps -
    
