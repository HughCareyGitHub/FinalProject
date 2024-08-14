# FinalProject

**Hughs Arsenal Blog**

This website is a simple beginner level blog. Users can read posts which the site owner submits and then call can add comments. It is intended for Arsemal fans that want to be kept up to date with the latest team gossip/ news.

![image](https://github.com/user-attachments/assets/f2a769fc-ac24-49d7-b6fe-50c5e1581dbe)

**Locations**

GitHub repo
https://github.com/HughCareyGitHub/FinalProject/

CI Database Maker
https://dbs.ci-dbs.net/manage/COejLfuyvbphRiIi/

Heroku deployment
https://dashboard.heroku.com/apps/final-project-hc

**Features**

In the homepage there is a list of all the blog posts sorted by post submit date. The user can navigate through the site using the Previous and Next button at end of page. 

![image](https://github.com/user-attachments/assets/f6e41334-b76c-4dfc-9850-fb3dd92e004a)

When they click on the title of any of the posts they can read that post. They can then add a comment or return to the home page. They can also share this post with a friend by submitting their friends email address.

Return to Home page:
![image](https://github.com/user-attachments/assets/888773cf-92f8-4184-8691-8403620648b2)

Add a comment to a blog post:
![image](https://github.com/user-attachments/assets/c4b78515-6481-4d40-8ed3-1e87e7bacbea)

Share a Post:
![image](https://github.com/user-attachments/assets/7d990282-bf1f-4c0e-b74e-eeecf43754ff)


**UX**

**Site Goals**

The goal of the site is to give the user information on Arsenal FC insluding the latest news for their fans to keep up to date and to comment their own ideas and news on top of the existing posts or add new posts. The site tries to be easy to navigate as well as aesthetically pleasing. Administrators should be able to easily approve posts and make changes to posts and comments.

**Users Stories**

As a blog user:

* I want to be able to read blog posts
* I want to be able to share chosen posts with friends
* I want to be able to add comments to the posts

  As a site administrator:

  * I want to be able to approve posts
  * I want to be able to make changes to posts and comments

**Wireframes**

To see all wireframes created in the UX stage
![blog_wireframe](https://github.com/user-attachments/assets/71b5a7c6-93db-47d2-b453-6e68c1429815)

**Agile Development**

For the development of Hughs Arsenal Blog, I adopted an Agile methodology to ensure iterative and efficient progress throughout the project lifecycle. Central to this approach was the utilization of a Kanban board hosted on GitHub Projects. You can view the project board in GitHub.

**Kanban Board Overview**

The Kanban board served as a visual representation of the project's progress and allowed for effective task management. It consisted of the following sections:

Backlog: This section contained all the tasks and user stories that were yet to be prioritized for implementation.
Ready: Tasks and user stories ready for development were moved to this column.
In Progress: Work in progress was tracked here, indicating tasks actively being worked on.
In Review: Upon completion, tasks were moved here for review before being marked as done.
Done: Tasks that were completed successfully were moved to this column.
Future Features: Ideas and tasks earmarked for future development were kept in this section for consideration in subsequent iterations.

**User Stories Integration**

User stories played a pivotal role in shaping the development process, ensuring that features were aligned with user needs. These user stories were mapped onto the Kanban board, guiding the prioritization and implementation of tasks.

**Task Management**

In addition to tracking user stories, the Kanban board served as a comprehensive task list. I utilized it to break down user stories into smaller, actionable tasks, ensuring clear and manageable objectives for development. This granular approach facilitated efficient progress tracking and enhanced team collaboration.

By leveraging Agile principles and utilizing the Kanban board effectively, the development of Sojourn Scribbles remained focused, adaptable, and responsive to evolving requirements, resulting in a more robust and user-centric Django blog application.

**Testing**

I added some posts and comments to make sure that all the site functionality is working as planned. I also shared some posts to verift that the share this post functionality is working.
I used the dev tools on chrome to test the website for responsiveness. I captured screenshots to demonstrate responsive design across mobile, tablet and laptop based on the size configurations preset in dev tools.

**Validator Testing**

* HTML

I used the W3 HTML Validator to check the HTML on each of my site pages by Direct Input. I have resolved the necessary errors.

* CSS
No errors were found when passing through the (Jigsaw) validator

* Python
  
I used the CI Python Linter to check all my python scripts. 

**Unfixed Bugs**

There were no unfixed bugs.

**Testing Section Requirements**

**Manual Testing**

Feature                    Expect                                 Action                             Result
Next Navbar button        When clicked the next page opens        Clicked Next on the Nav bar        Next page opened when clicked
Previous Navbar button    When clicked the previous page opens    Clicked Previous on the Nav bar    Previous page opened when clicked
Home Navbar button        When clicked the Home page opens        Clicked Home on the side bar       Home page opened when clicked
Posts list                When click the title post detail opens  Clicked post title                 Post detail page opened
Comments                  When click ADD COMMENT                  Clicked the ADD COMMENT            Commnent successsfully added        
Share the post            When click Share this Post              Clicked Share this Post            Post successfully shared

**Deployment**

The site was deployed to Heroku-down menu. The steps are as follows:
1. Create an account and login to Heroku
2. Click Create an app
3. Choose a name for your app and make sure it is visible
4. Click Create App
5. Click Resources
6. Search for postgres in the search box and click on heroku postgres.
7. Select the free/hobby dev option and click provision.
8. Make sure you save your new postgres DB URL as you will need this to connect to your database locally.
9. In the workspace terminal run "python3 manage.py dumpdata --exclude auth.permission --exclude contenttypes > db.json" to backup your local database  to a db.json file
10. Install dj_database_url and psycopg2 by using the following commands in the terminal: "pip3 install dj_database_url" and "pip3 install psycopg2"
11. Add your own new database url settings to settings.py being careful not to commit any changes that may leave your database url exposed in the version control
12. Migrate your db settings using the following command "python3 manage.py migrate"
13. Load your fixtures that you exported previously into your postgres db with the following command: "python3 manage.py loaddata db.json"
14. Create a new superuser with the following command: "python3 manage.py createsuperuser"
15. Install the gunicorn web server with the following command: "pip3 install gunicorn"
16. Save a list of all the required installed plugins by using "pip3 freeze > requirements.txt"
17. Create a Procfile to tell Heroku what kind of app you are deploying by using "echo web: gunicorn your_app_name.wsgi:application > Procfile"
18. Go to your Heroku dashboard and click on your app and then click the deploy tab
19. Connect your github repo in the deployment method section and click connect
20. Enable automatic deployment under the ustomatic deploys section
21. Click the settings tab
22. Click the reveal config vars
23. Add your environment variables such as SECRET_KEY 

**Citation of sources**

**Credits**

Got the idea from the blog section in the LMS but was struggling to understabd how all the different bits ot the MVT all fit in together so rather trying to abstract or expand on the basics I thought would be valuable to try recreate something similar to reinforce what I had learned in the LMS.

**Content**

I used the code institute LMS as my learning guide to how all the elements of the MVT worked together when constructing my models

**Media**

- The Arsenal logo was taken from https://worldvectorlogo.com/logo/arsenal
- The favicon was taken from https://icon-icons.com/icon/arsenal/17024

**Future Features**

I had played around with adding tags in the blog but ran into trouble. I referred to coding coach and tutor but there was nothing obvious wrong in my code and as the error description wasnt helping I just stripped the feature out and left the basic functionality (posts with comments) instead.

**Q&A**


**Summary**
