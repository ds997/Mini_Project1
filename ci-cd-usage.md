## How the usage of Git, Docker, Automated Testing, and Continuous Integration can improve the productivity and competitiveness of a company ?

Adopting Continuous Integration / Continuous Delivery practices enable teams to adapt their software on-demand to meet user feedback, market shifts, and any adjustments to the changing business requirements.

Continuous Integration is a software development practice where members of a team integrate their work frequently, usually each person integrates at least daily - leading to multiple integrations per day. Each integration is verified by an automated build (including test) to detect integration errors as quickly as possible. Many teams find that this approach leads to significantly reduced integration problems and allows a team to develop cohesive software more rapidly. Continuous integration removes one of the biggest barriers to frequent deployment. Frequent deployment is valuable because it allows your users to get new features more rapidly, to give more rapid feedback on those features, and generally become more collaborative in the development cycle.


### While there is no definitive Continuous Integration /Continuous Delivery pipeline structure, it is typically broken down into the following stages:

* __Commit & Build:__ When developers are finished making changes to an application, they commit their code to a shared repository like GitHub which will then integrate their snippet with the central code base. The piece of software, or the new feature, is then built from the extracted code and unit tested.

* __Automated Testing:__ Once the new piece of software is developed, it needs to be built and then thoroughly tested to ensure it meets all the initial requirements. There are various automated testing tools like Selenium ,Mocha etc that can be used to ensure an application looks and behaves as expected and covers everything from functional tests to performance tests. 

* __Deployment:__ In the final stage, the built piece of software is rolled out into production. CD requires this process to be automated, which ensures a reliable delivery to users. This is where Docker comes in, Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package.
