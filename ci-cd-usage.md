## How the usage of Git, Docker, Automated Testing, and Continuous Integration can improve the productivity and competitiveness of a company ?

Adopting Continuous Integration / Continuous Delivery practices enable teams to adapt their software on-demand to meet user feedback, market shifts, and any adjustments to the changing business requirements.

Continuous Integration is a software development practice where members of a team integrate their work frequently, usually each person integrates at least daily - leading to multiple integrations per day. Each integration is verified by an automated build (including test) to detect integration errors as quickly as possible. Many teams find that this approach leads to significantly reduced integration problems and allows a team to develop cohesive software more rapidly. Continuous integration removes one of the biggest barriers to frequent deployment. Frequent deployment is valuable because it allows your users to get new features more rapidly, to give more rapid feedback on those features, and generally become more collaborative in the development cycle.


### While there is no definitive Continuous Integration /Continuous Delivery pipeline structure, it is typically broken down into the following stages:

* __Commit & Build:__ When developers are finished making changes to an application, they commit their code to a shared repository like GitHub which will then integrate their snippet with the central code base. The piece of software, or the new feature, is then built from the extracted code and unit tested.

* __Automated Testing:__ Once the new piece of software is developed, it needs to be built and then thoroughly tested to ensure it meets all the initial requirements. There are various automated testing tools like Selenium ,Mocha etc that can be used to ensure an application looks and behaves as expected and covers everything from functional tests to performance tests. 

* __Deployment:__ In the final stage, the built piece of software is rolled out into production. CD requires this process to be automated, which ensures a reliable delivery to users. This is where Docker comes in, Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package.


### Here are five aspects of using Git, Docker, Automated Testing, and Continuous Integration that provides companies a competitive edge :


**1. Faster Release Cycles:** Speeding up the build and deploy cycle allows teams to get new features into production quicker, and reduce the time to market a product.

**2. Reduced Risk:** By releasing new updates or features continuously, the risk of bugs in production is also reduced dramatically.

**3. Lower Costs:** Adopting a continuous development model lowers the costs by eliminating many of the fixed costs associated with building and testing changes to the application. For example, automated environment provisioning will reduce the costs associated with maintaining your own test infrastructure. By continuously committing your code, you’ll spend less time (and therefore money) on fixing bugs.

**4. Higher Quality Products:** Continuous integration enables stronger collaboration between developers, meaning bugs are found and fixed faster earlier in the development process. Running automated regression and parallel tests will improve test coverage, ensuring your application is bug-free and works across a wider range of environments. Continuously delivering smaller updates to your software will make most changes (and bugs) undetectable to the end user, resulting in happier customers.

**5. Better Business Advantage:** Moving to a continuous development model gives your team the flexibility to make alterations to your software on-the-go to meet new market trends and user needs. You’ll be able to meet rapidly changing demands and will turn your release process into a competitive advantage.

## Source :

[Git] (https://www.freecodecamp.org/news/what-is-git-and-how-to-use-it-c341b049ae61/)

[CI & CD] (https://smartbear.com/learn/automated-testing/the-continuous-development-pipeline/ )

[Docker ] (https://opensource.com/resources/what-docker)