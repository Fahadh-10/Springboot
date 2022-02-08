# Springboot
Assignment given by cliff.ai
Name        :    Mohamed Fahadh N
Date        :    02/07/2022
Location    :    Bangalore



Summary
•	To create REST API's using SpringBoot
•	To create REST API's for two models Team and Player. These models have one to many relationship.
•	Basically, a team has many players (one to many). You have to create (CRUD) endpoints in spring boot


                              Team                                                            Player
                                       
                               id                                                              id
                              name                                                            name
                             location                                                          age
                            created_at                                                       created_at
                            updated_at                                                       updated_at
                                                                                              team_id


Endpoints
1.	Create - Team , Player
2.	Find by Id - Team, Player
3.	update - Team , Player
4.	delete - Team , Player
5.	List - Team , Player add pagination
6.	Find players by team id and Find team by player id


Introduction
•	 To create a REST API using Spring Boot, need to download a Maven project from the chrome browser. 
•	By using Eclipse(IDE) and import the project.
•	Run using java application and check whether the build is success or not, if it is success we can proceed to the next step.
•	 Open pom.xml and check the dependency, if we need to add the dependency we can add additional dependency.
•	Need to add the package and class and should perform the respective operation.
•	Need to do coding for the team and player.
•	By opening the Postman we can add the request and click on send.
•	By performing CRUD operation in Postman we will get unique URL for every resourse.
•	After that convert Java object to JDBC Library and need to initialize then we can perform any of the database language.
 

Tools used
•	Eclipse
•	SpringBoot
•	Postman

Spring Boot Download
           Open chrome browser----->Search for Spring Initializer---->project(Maven project)------>Language(Java)----->Spring Boot(2.6.3)---->In Project Metabase fill the required fields----->Add dependencies(Spring web)----->Explore---->Generate------>Extract the file.

Eclipse
•	Open eclipse-->import the project---->go to pom.xml---->run the java application---->see the result in console---->build success.
•	Click on src/main/java---->create a package(com.demo.api)---->create a class(SpringBootApplication)
•	Add a controller
                      @org.springframework.boot.autoconfigure.SpringBootApplication; com.demo.api.controller
•	Create a package(com.demo.api.controller)---->create a class(PlayerController) & (TeamController)

PlayerController
•	Controllers used in this package are 
                            @RequestMapping
                            @RestController
                            @Autowired
                            @GetMapping
                            @PostMapping
•	By using these controllers we import
              import com.demo.api.repository.PlayerRepository;
              import com.demo.db.dto.PlayerDto;
              import org.springframework.beans.factory.annotation.Autowired;
              import org.springframework.web.bind.annotation.*;
              import java.util.List;
•	By using the controllers here we perform POST and GET operation which is create and read the operations.

TeamController
•	Controllers used in this package are
                             @RequestMapping
                             @RestController
                             @Autowired
                             @GetMapping
                             @PostMapping
                             @PathVariable
•	By using these controllers we import
            import com.demo.api.repository.TeamRepository;
•	By using the controllers here we perform POST and GET operation which is create and read the operations.
•	By using these controllers we can read the team and we can create the team.

Com.demo.api.repository
•	Create a package(com.demo.api.repository)---->create a class(PlayerRepository) & (TeamRepository)

PlayerRepository
•	Controllers used in this package are
                               @Component
•	By using this controller we import
                    import com.demo.db.dto.PlayerDto;
                    import org.springframework.stereotype.Component;
                    import java.util.ArrayList;
                    import java.util.List;
                    import java.util.Map;
                    import java.util.concurrent.ConcurrentHashMap;
                    import java.util.concurrent.atomic.AtomicInteger;
•	Here we can add a player, update a player, get a player

TeamRepository
•	Controllers used in this package are
                      @Component
•	By using this controller we import
                    import com.demo.db.dto.TeamDto;
                    
•	Here we can add a team, update a team, get a team

Com.demo.db.dto
•	Create a package(com.demo.db.dto)---->create a class(PlayerDto) & (TeamDto)

PlayerDto
•	In a PlayerDto class create
                      private Integer id;
                      private Integer teamId;
                      private String name;
•	Then select getters and setters.

TeamDto
•	In a TeamDto class create
                      private Integer id;
                      private String name;
•	Then select getters and setters.

REST API (Postman)
TeamAndPlayers
•	Create Player (POST) ----->URL: http://localhost:8080/player/create
•	Create Team (POST) ------>URL: http://localhost:8080/team/create
•	List Teams (GET) ------->URL : http://localhost:8080/team/list
•	List Player (GET) ------->URL : http://localhost:8080/player/list
•	Get Player (GET) ------->URL : http://localhost:8080/player/1
•	Get Team (GET) -------->URL : http://localhost:8080/team/1 

GIT HUB
         Open GITHUB---->Signup---->Create Repository---->Name:Springboot--------->Description: Assignment given by cliff.ai----->Check on the README file------->set the path and upload the file(Springbootrestdemo)---->create accounts for collaborators----->add the document---->add the screenshot on successfully testing endpoint on postman.
