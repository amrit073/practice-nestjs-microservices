Starting <br>
Step 1 <br>
-> Create servers folder<br>
-> Create nest app named: gateway<br>
-> go inside gateway
-> Generate nest app -> nest g app -> give app name -> users (service)<br>
-> Move all the files and folder from servers/gameway to servers/ and delete gateway folder<br>
-> Remove controllers files from servers/apps/gateway/src/app.controller*.ts<br>
-> Install dependencies<br>
npm i @apollo/gateway @apollo/subgraph @nestjs/apollo @nestjs/graphql graphql class-validator bcrypt @types/bcrypt express

<br><br><br>
To Push  to prisma use command -> npx prisma db push <br><br>
To use mongodb with prisma we need to create replica set. We can do that by following steps:<br>
1: Modify mongo.conf file and add replication. (/etc/mondod.conf for ubuntu)<br>
-> replication:<br>
  replSetName: "replication1"<br>
Now start mongo with --replSet like:<br>
mondod --replSet rs0<br>
set db url in .env file like:<br>
DATABASE_URL=mongodb://localhost:27017/db_name?replicaSet=replication1
