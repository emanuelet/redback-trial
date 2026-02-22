# Background

Redback is a rapid application development (RAD) platform specifically designed for business applications. It offers a collection of business services that can be configured individually and then deployed as a single monolithic application.

Redback runs on Firebus, a distributed service bus aimed at managing auto-discovery and load balancing transparently. 

Redback and Firebus currently have very little documentation for developers

# Objective

The objective of this repo is to test a candidate's ability to:
1. Work with and understand Redback's architecture and patterns
2. Reverse engineer the code to understand how an application is configured
3. Be independent and driven in working through hard technical problems

Start by forking this repo to your account.  You should then work through the 3 milestones below, which go in increasing order of difficulty. You may or may not be able to finish milestone 3.

Once finished, push all your changes to your forked repo and send through the link to the new repo for review.

You can ask questions and clarifications, this can help unblock you and will help me understand your thought process. The instructions are often left vague on purpose, this helps me understand your ability to work through very patchy instructions and requirements.

# Milestone 1 - Get the basic application running

You will notice this application has dependencies to Redback and Firebus bundles which may not be published on Maven central. The easiest way will be to clone the repos of these dependencies and install the maven packages locally.

https://github.com/ngrondin/redback<br>
https://github.com/ngrondin/firebus<br>

You will also need to setup a local MongoDB, whose details will need to be updated in the properties file.

You will also notice the application will connect to redback.io's live IDM as all application require authentication. You can use the following credentials to log in:<br>
***username:*** trial@redback.io<br>
***password:*** password<br>

Once the application is up and running and you can access the screens, you have completed Milestone 1.

# Milestone 2 - Simple configurations

The default application is a very simple ticketing screen. 

The next milestone aims at implementing a few simple configuration changes to the basic application. You will need to extrapolate and/or reverse engineer the source code to figure out how to do this.

1. Add the following fields to the ticket: Assignee, Ticket classification
2. Add lookup values for classifications and assignees as these should be drop down input fields
3. Add a simple screen to allow to manage the status, classifications and user values.
4. Add a "log" component to the ticket screen so users can record the progress of their work on the ticket.

# Milestone 3 - Complex configuration

In this phase, you will continue developing the application by adding features for the following requirements: Implement a workflow between the requestor and the assignee.

1. The requester chooses the assignee and then submits the request. 
2. The assignee can then work on the ticket or return it to the requester for clarification. 
3. Once the work is done the ticket is archived. All activities should be recorded.

