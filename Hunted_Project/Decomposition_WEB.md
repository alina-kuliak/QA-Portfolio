# 🧩 Functional Decomposition: Huntd WEB

This document provides a comprehensive breakdown of the Huntd Web Platform. Testing for the web version focused on cross-browser compatibility, responsive design, and role-based data isolation.

---

## 🗺️ High-Level Web Map
The web architecture is optimized for two distinct user funnels: "Engineers" (Candidates) and "Companies" (Recruiters).

**The user is logged out:**

1. **Main page**  
   1. For engineers  
      1. ‘’Get started’’ form  
         1. Start with social network links  
         2. ‘’Email’’ field  
         3. \[Get offers\] button  
      2. ‘’How it works’’ information  
      3. Job offers  
         1. \[Apply\] button  
      4. Got to Web3 companies  
         1. ‘’Discover’’ link  
      5. Feedback from real users  
   2. For companies  
      1. Info for recruiters about the product  
         1. \[Hire engineers\] button  
         2. Quotes from the CEO  
         3. Comparison with other resources  
         4. Logos of partners  
   3. Navigation menu  
      1. ‘’Candidates’’ link  
      2. ‘’Jobs’’ link  
      3. ‘’Sign in’’ link  
      4. ‘’Sign up’’ link

      

2. **Sign In page**  
   1. Navigation menu  
   2. ‘’Sign in’’ form  
      1. ‘‘Email’’ field  
      2. ‘‘Password’’ field  
      3. \[Sign in\] button  
   3. Sign in with social network links  
   4. ‘‘Forgot password’’ link  
   5. ‘’Don’t have an account? Sign up link  
3. **Sign Up page**  
   1. Navigation menu  
   2. ‘’Sign up’’ form  
      1. ‘‘Email’’ field  
      2. ‘‘Password’’ field  
      3. ‘‘Repeat password’’ field  
      4. \[Create an account\] button  
   3. ‘’Sign up with’’ social network links  
   4. ‘’Already have an account? Sign in’’ link  
4. **Jobs**  
   1. Navigation menu  
   2. \[Post a job\] button  
      1. Add job manually  
      2. Import jobs from ATS  
   3. ‘’Top companies’’ link  
   4. The filter bar of directions in job seeking  
   5. The table of job offers  
      1. Company/Position  
      2. Details  
      3. Status  
      4. Job offer  
      5. \[View more\] button  
   6. ‘’Job offers notification to inbox’’ form  
      1. ‘'Desired roles’’ drop down list  
      2. ‘’Your experience’’ drop down list  
      3. ‘’Salary’’ slider  
      4. ’’Email’’ field  
      5. \[Receive Jobs\] button  
5.  **Candidates**  
   1. Navigation menu  
   2. ‘’Candidates'’ sidebar  
      1. ‘’Oops\! Seems you haven’t signed up’’ notification popup  
         1. \[Free sign-up\] button  
         2. \[Sing in\] button  
   3. Footer  
6. **Web3-companies**  
   1. Navigation menu  
   2. Top 100 Web3-companies logos table  
      1. 10n/100 ‘’Company logo’’ link  
7. **Footer**  
   1. ‘’Top 100 Web3 companies’’ with a preview of the top 5 companies  
   2. ‘’View top 100’’ link  
   3. 3 columns of vacancies for web3 developers  
   4. Links to social networks   
   5. Documents links

**User Logged In As A Recruiter**

1. **Main page**   
   1. Navigation menu  
      1. ‘’For engineers’’ link  
      2. ‘’Candidates’’ link  
      3. ‘’Jobs’’ link  
      4. ‘’Chats’’ link  
      5. ‘’Profile’’ icon  
   2. For engineers  
      1. ‘’Stay in touch’’ HNTD app  
      2. ‘’How it works’’ information  
      3. Job offers  
      4. Got to Web3 companies  
      5. Feedback from real users  
   3. For companies  
      1. Info for recruiters about the product  
         1. \[Hire engineers\] button  
         2. Quotes from the CEO  
         3. Comparison with other resources  
         4. Logos of partners  
   4. Footer  
2. **Candidates page**  
   1. Navigation menu  
   2. ‘’Candidates’’ side bar  
      1. ‘’Searching first engineers’’ form  
   3. ‘’Potential candidates’’ list  
      1. ‘’Potential candidates’’ profile  
         1. Information about the candidate  
         2. \[Start chat\] button  
         3. ‘’Show experience’’ drop-down  
   4. Footer  
3. **Chats page**  
   1. Navigation menu  
   2. ‘’All chats’’ link  
      1. Chats list  
         1. User name  
         2. Position  
         3. \[Delete\]/\[Archive\] buttons  
      2. Conversation history  
      3. Status  
         1. ‘’Hire’’  
         2. ‘’Reject’’  
      4. ‘’Type a message’’ field  
         1. \[Sent\] button  
   3. ‘’Archive’’ link  
   4. Footer

4. **Profile**   
   1. Created account  
      1. Navigation menu   
      2. Preview profile  
         1. \[Deactivate profile\] button  
         2. \[Edit\] button  
      3. Edit profile  
         1. Company details  
         2. Contacts  
      4. Hiring management  
         1. Hirings  
         2. Connections  
         3. Subscriptions  
         4. Message templates  
      5. Account settings  
         1. Social profiles  
         2. Change password  
      6. Sign out  
   2. Creating an account  
      1. ‘’Profile’’ header  
      2. \[Sign out\] button  
      3. ‘’I am… ‘’Candidate/Recruiter’’ link  
         1. Company details  
         2. Contact information  
         3. ‘’Searching for first engineers’’ form  
         4. ‘’Searching results’’ pop-up 

**User Logged In As A Candidate**

5. **Main page**   
   1. Navigation menu  
      1. ‘’For engineers’’ link  
      2. ‘’Candidates’’ link  
      3. ‘’Jobs’’ link  
      4. ‘’Chats’’ link  
      5. ‘’Profile’’ icon  
   2. For engineers  
      1. ‘’Stay in touch’’ HNTD app  
      2. ‘’How it works’’ information  
      3. Job offers  
      4. Got to Web3 companies  
      5. Feedback from real users  
   3. For companies  
      1. Info for recruiters about the product  
         1. \[Hire engineers\] button  
         2. Quotes from the CEO  
         3. Comparison with other resources  
         4. Logos of partners  
   4. Footer  
6. **Candidates page**  
   1. Navigation menu  
   2. ‘’Candidates’’ side bar  
      1. ‘’Searching first engineers’’ form  
   3. ‘’Potential candidates’’ list  
      1. ‘’Potential candidates’’ profile  
         1. Information about the candidate  
         2. \[Start chat\] button  
         3. ‘’Show experience’’ drop-down  
   4. Footer  
7. **Chats page**  
   1. Navigation logged  
   2. ‘’All chats’’ link  
      1. Chats list  
         1. User name  
         2. Position  
         3. \[Delete\]/\[Archive\] buttons  
      2. Conversation history  
      3. Status  
         1. ‘’Hire’’  
         2. ‘’Reject’’  
      4. ‘’Type a message’’ field  
         1. \[Sent\] button  
   3. ‘’Archive’’ link  
   4. Footer  
8. **Profile**  
   1. Created profile  
      1. Navigation menu   
      2. Preview profile  
         1. \[Deactivate profile\] button  
         2. \[Edit\] button  
      3. Edit profile  
         1. Role  
         2. Expectations  
         3. Experience  
         4. Bio   
         5. Contact Information  
      4. Account settings  
         1. Social profiles  
         2. Change password  
      5. Sign out  
   2. Creating a profile  
      1. Role  
      2. Expectations  
      3. Experience  
         1. \[Upload from LinkedIn\] button  
         2. \[Add manually\] button  
      4. Bio   
         1. ‘’Profile examples’’ links  
         2. ‘’Achievements / Key results’’ textbox  
         3. ‘’Expectations from work (optional)’’ textbox  
         4. \[Save and continue\]  
      5. ‘’Contact Information’’ form  
9. **Footer**  
   1. ‘’Top 100 Web3 companies’’ with a preview of the top 5 companies  
      2. ‘’View top 100’’ link  
      3. 3 columns of vacancies for web3 developers  
      4. Links to social networks   
      5. Documents links  
10. **Jobs**  
    1. Navigation menu  
    2. ‘’Top companies’’ link  
    3. The filter bar of directions in job seeking  
    4. The table of job offers  
       1. Company/Position  
       2. Details  
       3. Status  
       4. Job offer  
       5. \[View more\] button  
    5. ‘’Job offers notification to inbox’’ form  
       1. ‘'Desired roles’’ drop down list  
       2. ‘’Your experience’’ drop down list  
       3. ‘’Salary’’ slider  
       4. ’’Email’’ field  
       5. \[Receive Jobs\] button  
11. **Web3-companies**  
    1. Navigation menu  
    2. Top 100 Web3-companies logos table  
       1. 10n/100 ‘’Company logo’’ link

