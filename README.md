Quiz Quest - Data Analysis - Power BI dashboard - A dashboard providing insights on the overall performance of the team with regards to various questions of topics such as Power BI, Power Apps, Power Automate and a few general topics. 

It has three pages - The Home Page, BT Analysis and the Overall Tracker.

# SKILLS
Power BI, DAX, Power Query, Data Modelling, Power Automate.

# Home Page - 

![image](https://github.com/user-attachments/assets/a3604687-ddf7-4abb-ba65-0e4ac4dcf4d0)

It is a landing page for the users with a pleasing appeal. It has a button that takes the user to the BT Analysis page.

It also displays the Latest Refresh Time. The refresh time signifies when the data was last refreshed or added to the fact and dimension tables. The data is refreshed every time any user in the team answers a question from the teams. This is done by a workflow created by Power Automate. When a user answers a question, the backend updates the data entry to SharePoint. When this event (adding or editing of data in SharePoint) is triggered, the data is refreshed in Power BI.


# BT Analysis Page- 

![image](https://github.com/user-attachments/assets/2e2e4ece-cba0-439f-b549-e16a39319694)

This page contains weekly performance results of the entire team as a whole. The default filters applied on the page are Question Type - All, Questions - All, date - 1 week (Relative last 1 Calendar week).

It has a question table visual which displays the questions along with the four choices and the date when the question was posted.

It has a clustered column chart named Poll Results - when no question is clicked in the question table, it displays the data for the entire week, telling what overall options were selected. But when the viewer clicks on a particular question, we can see for that particular question what all options were answered by the team.

There is a clustered column chart named % Responding By Month Name And Day - This shows the percentage of people responding on a date-to-date basis in the last 2 relative weeks, excluding Saturday and Sunday as no question is posted on those days. The color of each date’s bar is also relative to the percentage of people answering. If the percentage is more, then the color is dark for a particular bar; if the percentage is less, then the color is light. This was done using Gradient and Conditional Formatting.

Then there is a card visual showing Correct Answer - This visual does not display anything when no question is selected from the question table. When a question is selected, it displays the Correct option along with the correct answer.

Then there are two Gauge charts - %Responding and %Correct - The %Responding shows the percentage of people who responded to at least one question in the entire last week when no question is selected, but when a question is selected, then it displays the percentage of people who responded to that question. The %Correct shows the gauge as 0% when no question is selected but when the question is selected then, it displays the percentage of people who answered correctly.

There is a back arrow which takes you back to the home page.

Then there is an Overall Tracker button which we will talk about in the next section.


# Overall Tracker Button in the BT Analysis page - 

![image](https://github.com/user-attachments/assets/1355a86f-2991-4557-801e-9efbe2ec987a)

We have a few emails in the admin table. When a person who is viewing the mail has their email in the admin table, only then will this button work. Moreover, to hide the display of the button, when the person who is viewing does not have their email in the admin table, the color of the button is white. So, they do not even know that such a page also exists in the report. Only the admins can access the Overall Tracker Page. This was done by implementing security.

Note - this was done based on the needs of the manager. The general view was that the team results would be shown as a whole every week and we did not want to demotivate anyone by showing who answered wrongly every week. But at the same time, the page was created so that on an internal level, the managers may know how much knowledge their team members have regarding a particular topic.


# Overall Tracker Page- 

![image](https://github.com/user-attachments/assets/2e5f625d-69f4-49f1-9e94-0527ee7816e6)

This page is only visible to the people who have their User email in the admin table. This is a page which displays the employee-to-employee performance with filters available for changing month, year, and date.

It has a table - which displays the names of all employees. Along with the names, it displays the total number of responses, Score (Correct answers given), and the % correct response made by each employee in the specific time filter.

There is a Response Details Line Chart. This displays two lines telling the number of people responding on a particular day and the other one showing the number of people who have not responded on a particular day for the span of filter dates.

Then there are 2 list tables showing names of people who have responded once in the time period and the ones who have not responded in that time frame. We can check it on a date-to-date basis also by selecting a particular date in the Response Details Line Chart.

Then there are two cards - Top Scorer and Most Active - Top Scorer displays the name of the employee who has the most score in the given time filter. Whereas the Most Active shows the name of the person who has given the most number of responses in the given time filter. Duplicate responses are not taken into account, only the first response done by the user is taken into account.

The %Responding shows the percentage of people who responded to at least one question in the entire filter date when no date is selected, but when a date is selected then it displays the percentage of people who responded on that date.

Then there are two buttons which take us to the Home Page and the BT Analysis page.

# Learnings - 

Power BI Basics - I got to know about various visualizations and when to use them. I learned about how to create dashboards in a fast and efficient manner.

Data Modelling - The various topics which I learned were what dimension and fact tables are, how a star schema works, how to make relations between various tables and how to link them. What various types of relationships can coexist between two tables. How new columns can be made by example or by functions.

DAX and Power Query - It helps us to do conditional filtering of data, making relations between two data tables. Fetching, merging, and manipulating data. How to create measures and how to use measures.

RLS - How to implement RLS. How to make some data visible only for a few members.

Power Automate - How to create a flow and how to link that flow with Power BI.

Data Privacy - Due to privacy reasons, I could not publish companies’ data. So for publishing this report, I needed to encrypt the original databases. So how to maintain the privacy of company data was also a major learning.

# Challenges - 

I faced a challenge in figuring out how to refresh the data. One simple way was to schedule the refresh after every few hours. But I learned about Power Automate, how to link Power Apps and Power BI, and how to create a flow for the same.

In the % Responding by Month Name and Day - The challenge was to do conditional formatting, how to display data of only weekdays and not the weekends, and how to color the bars based on the gradient.

The implementation of security so that no normal user can view the Overall Tracker page was one big learning. How to use RLS and how to create user-specific displays and pages are key takeaways.











