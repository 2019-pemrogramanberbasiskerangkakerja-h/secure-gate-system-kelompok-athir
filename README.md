 API VIA REDIRECT
    add
        add member   
            router.post('/adduser/:nrp/:pass/:grub', myController.addsubmit_regis );
            http://localhost:3000/adduser/05111640000002/asdf/user

        add gate 
            router.post('/addgates/:name/:start/:end', myController.addsubmit_gate );

        add group  
            router.post('/addgroup/:name/:id', myController.addsubmit_group );   

    login
        router.post('/apilogin/:RegUsername/:RegPassword/:group/:gate', myController.apisubmit_login ); 
        http://localhost:3000/apilogin/05111640000000/asdf/admin/pintu 2

    logout 
        router.get('/logout/:nrp', myController.get_logout );
     
   

 API VIA BODY
    POST / : (untuk login)
    Requirement name body : RegUsername,RegPassword,group, gate 

    GET /logout/:nrp
    body Requirement -> nrp (nrp disini tu id membernya h3h3) 

    POST /user: create user
    Requirement name body ->RegUsername, RegPassword,group

    GET /users : get All User
    GET /users/:userid : Get User from userid
    DELETE /users/:userid : Delete user from userid

    POST /gates : create gates
    Requirement body -> gateName, start, end
    note: start and end format : 00:00:00

    GET /gates : get all gates
    GET /gates/:gateid : Get Gate from gateid
    DELETE /gates/:gateid : Delete Gate from gateid

