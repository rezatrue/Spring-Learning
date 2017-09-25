# Spring-Learning
Lessons from https://www.udemy.com/complete-e-commerce-course-javaspringhibernate-and-mysql

Open a project:
New -> Spring start up project

Download BootStrap
http://getbootstrap.com/docs/3.3/getting-started/#download
Pest in project folder:
src -> main -> static

Open a HTML page :
index.html

search for "bootstrap navbar template" open the source page : 
https://getbootstrap.com/docs/3.3/examples/navbar/

& repalce index page content with these source code 
open source page click on "navbar.css" copy content 
open a new css file in res -> maim -> resources -> css -> style.css
pest all contents in here & change this like 
chnage <link href="navbar.css" rel="stylesheet"> into <link href="/css/style.css" rel="stylesheet">
Change <script src="../../dist/js/bootstrap.min.js"></script> into <script src="/js/bootstrap.min.js"></script>


Open pom.xml & the dependency

<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>

Add ending / of meta tags & delete few tags

fix link for bootstrap like this :

<link href="/dist/css/bootstrap.min.css" rel="stylesheet">

Delete these lines for now :
 <!-- IE10 viewport hack for Surface/desktop Windows 8 bug -->
<link href="../../assets/css/ie10-viewport-bug-workaround.css" rel="stylesheet">

<!-- IE10 viewport hack for Surface/desktop Windows 8 bug -->
<script src="../../assets/js/ie10-viewport-bug-workaround.js"></script>

Create a Controller package & class in :
rsc -> main -> java -> com -> bookstore -> controller -> HomeController.java


write these code 

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class HomeController {
	@RequestMapping("/")
	public String index(){
		return "index";
	}
}
