# MyCapstone
Installation of softwares and running my capstone project.
First install XAMPP software from site
 https://www.apachefriends.org/download.html
Then follow instructions. Once installed run Apache Server. By opening Xampp Control Panel in Windows and manager.os in Mac Osx
Then, open terminal to set all the required updates need to be done in terminal. Follow file:///Applications/XAMPP/xamppfiles/htdocs/dashboard/jp/faq.html

Just follow exact things in terminal as shown in above file.
Now Install Netbeans IDE select last one which install all components. Then open the project ORUTA. Then add missing libraries mail.jar and commons-code-1.5.jar.
And add by resolving by selecting the location downloads.
Then, you right click on project and maximize it it will don’t have errors but there are still some missing libraries in source package related to Upload.java class. There download tomcat-coyote.jar and org.apache.commons.fileupload.jar. But, still we find errors. Then relace “import org.apache.tomcat.util.http.fileupload.FileItem;
import org.apache.tomcat.util.http.fileupload.disk.DiskFileItemFactory;
import org.apache.tomcat.util.http.fileupload.servlet.ServletFileUpload;”
with 
 “import org.apache.commons.fileupload.FileItem;
import org.apache.commons.fileupload.disk.DiskFileItemFactory;
import org.apache.commons.fileupload.servlet.ServletFileUpload;”
Now, Clean and build and then run the code.
It works.
Now, enter PhpMyAdmin with your username and password for logging into PhpMyAdmin. There import the database files which are located in code-->database folder, file name is "oruta Project 20141106 1338". This step will import all the tables which we need for our code.
Then open code of Dbcon.java, con = DriverManager.getConnection("jdbc:mysql://localhost:3306/privacy", "<yourusername>", "<yourpassword>");
Change password.
Within the project in the services open database, there check wether the server is running as localhost or not. Then connect with the database. Under services we can find our service as "dbc:mysql://localhost:3306/privacy?zeroDateTimeBehavior=convertToNull". Thats the exact link of our server. 
