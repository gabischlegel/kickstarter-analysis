# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends - Module 1 
![Parent Category Outcomes](https://user-images.githubusercontent.com/110864175/183732952-b1703628-084d-41f9-a660-6056a8df660c.png)
![Outcomes Based on Launch Date](https://user-images.githubusercontent.com/110864175/183732872-927667ed-a9ed-4dd0-90a2-c932ecbf78b4.png)
Louise should launch in May or June --- She should have around $3168 pledged and should aim for a goal of $1500 - $5000
# Kickstarting with Excel
## Overview
### The purpose was to see how other campaigns did due to their launch date and funding goals so Louise could compare her campaign to them.
## Analysis and Challenges
### Analysis Based on Launch Date
#### I performed my analysis based on Launch Date by creating a pivot table based on the "years" column I created in the Kickstarter sheet using =YEAR(S2) for cell U2 and copying it down. I then filtered my pivot table to hide the "active" column. Finally I created the following line chart to show the relationship between outcomes and launch month.
![Theater_Outcomes_vs_Launch png](https://user-images.githubusercontent.com/110864175/185228222-19c99544-8c8d-409a-bd06-c64b9e6513f7.png)
### Analysis Based on Goals 
#### I performed my analysis based on Goals by creating a new sheet where I used the COUNTIFS function to learn how many sucessful, failed, and canceled projects there were for plays based on the goal dollar-amount. I created a column using incriments of $5000 - ranging from less than $1000 to $50000 and up. I used the =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"Successful",Kickstarter!$R:$R,"Plays") to calculate "Number Successful", =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"Failed",Kickstarter!$R:$R,"Plays") to calculate "Number Failed", and =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"Canceled",Kickstarter!$R:$R,"Plays") to calculate "Number Canceled" for the plays that had a goal less tyhan $1000. I double checked to make sure I changed the valued based on the goal number I was calculating. Then I summed the total projects and calculated the "Percentage Successful" =B2/E2, "Percentage Failed" =C2/E2, and "Percentage Cancelled" =D2/E2. From all these values, I created a line chart to display my findings which is displayed below. 
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/110864175/185228158-9d00e754-2768-42c6-87f0-9354b2a0e996.png)
### Challanges
#### The biggest challenge I faced was with the COUNTIFS function. I could not manage to get the function to run without getting a error button. When I finally did figure it out I used =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"Successful") which left out the "Plays" filter. After realizing my error, I went back to edit the entire chart so it was just filtered by "Plays"I also doubted my formula when "Number Canceled" kept coming out as 0. After triple checking, I realized it was actually supposed to come out as 0.
## Results
### We can conclude that campaigns that have the most success are launched in May and June based on Theater Outcomes by Launch date. We can also conclude there were almost as many campaings that failed as successful campaigns in October
### We can conclude that the "Percentage Successful" and "Percentage Fail" campaigns are inversely related based on the dollar goal. As one goes up the other goes down. The most succesful campaigns had the goal of $0 - 1500 and $35000 to $45000.
### The data is limited because there were no plays that were cancelled. 
### We could create a table and graph that compares the country to the success of the play. This was Louise could know which countrys had the most success. We could also compare the amount of backers to if the play was successful or not.
