---
title: A/B Test Results
excerpt: Learn how to analyze your A/B Test results to conclude your experiments.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# A/B Test Results

The A/B Test Results feature provides valuable insights from your experiments, aiding data-driven decision-making. It offers comprehensive analysis, intuitive visualization, statistical significance assessment, and variant distributed reporting. This helps users uncover insights leading to product enhancement, improved user engagement, and overall success of the A/B test.

It utilizes advanced filtration methods to ensure accurate data assessment. It includes only data captured during the user's participation in the test, excluding any data from instances where the user enters and leaves the AB test multiple times (unless the test is marked as '[Sticky](doc:create-ab-tests#sticky-target)'). This ensures that all the available metric data available on the Results page is clean and based on user behavior.

You can view the A/B Test Results for a particular period by selecting the time range from the Calendar widget in the top right corner. This helps segment and analyze data based on when events or observations occurred for the defined timeframe. You can view results for a short interval, such as a day, a week, or a month, or a longer span, such as a year or multiple years. You define the timeframe to analyze your A/B Test as follows:

<Image alt="Calendar Widget" align="center" border={true} src="https://files.readme.io/93adf9f-in-app_calendar.png" /> Define the Time Frame using the Calendar Widget

You can further categorize your data based on platform attributes such as Operating system) and User Properties using the *Group by* option (refer to the following image):

<Image alt="Group by OS Name" align="center" border={true} src="https://files.readme.io/6727cb2-group_by_os.png" /> Group by OS Name

This helps in getting a granular view of users, allowing you to make data-driven decisions across distinct operating systems or users with different properties.

Also, hovering over the Users icon adjacent to the *Results* tab offers a high-level breakdown of actual users entering the A/B test across different Variants and the Control group (see the following image).

<Image alt="Total users entering across the variants" align="center" border={true} src="https://files.readme.io/d2fa8eb-total_users.png" /> Total users entering across the variants

Now, the available metrics in the A/B test can be categorized into Common and Goal metrics.

## Common Metrics
Common metrics are accessible for every A/B test, regardless of whether you have chosen specific Event-based Goals. The common metrics include:

* **Unique Users**: This refers to the count of individual users who have interacted with a website, application, or service during a specific period. Each user is counted only once, regardless of how often they visit or use the platform within that timeframe.
* **Returning Users**: This refers to the individuals who have visited or interacted with a website, application, or service more than once during a specific period. They are distinguished from Unique Users who have engaged with the platform on multiple occasions.
* **First-time Users**: This refers to the individuals who visit or interact with a website, application, or service for the first time during a specific period. These users are new to the platform and have not engaged with it before within the defined timeframe.
* **Sessions**: This refers to the individual visits or interactions a user has with a website, application, or service during a particular timeframe. A session starts when a user accesses the app and ends after a period of inactivity or when the user leaves the app.\
  Tracking sessions are a great way to measure engagement for certain apps, such as video or music streaming, news, etc. You must enable session tracking from the CleverTap dashboard to track user sessions. To enable session tracking, navigate to *Settings* > *Session analytics* and toggle ON the [session tracking](doc:session-analytics#session-dashboard).

<Image alt="Common Metrics View" align="center" border={true} src="https://files.readme.io/129222c-common_metrics.png" />  Common Metrics View











Listed below are some key session metrics, along with their formulas and definitions:
| Metric                          | Formula                                                                         | Definition                                                                                                       |
| :------------------------------ | :------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------- |
| Returning Users                 | 100 x [(Total Unique Users) - (Total First-time users)] / (Total Unique Users)  | The percentage of users returning to your application or website.                                                |
| Total Sessions                  | Total occurrences of **"Session Concluded"** event                              | The total number of user sessions.                                                                               |
| Total Session Length            | Sum of values for the event property  *length* of the *Session Concluded* event | Calculated using the event property *length* of the *Session Concluded* event. The total length of all sessions. |
| Average Session Length          | (Total Session Length) / (Total Sessions )                                      | The average length of a session.                                                                                 |
| Average Session Length per User | (Total Session Length) / (Total Unique Users )                                  | The average length of a user session in your application/website.                                                |
| Average Sessions per User       | (Total Session ) / (Total Unique Users )                                        | The average number of sessions for a user.                                                                       |

## Goal metrics

Goal metrics are specific to the event and properties selected in the A/B test Goals. You can find these from the *Metrics* dropdown on the left. 

<Image alt="Goal Metrics" align="center" border={true} src="https://files.readme.io/2492c9f-goal_event.png" />  Goal Metrics

Listed below are some key goal metrics, along with their formulas and definitions:
<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Metric
      </th>

      <th>
        Formula
      </th>

      <th>
        Definition
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Total &lt;Goal event&gt; occurrences
      </td>

      <td>
        Total occurrences of &lt;Goal event&gt;
      </td>

      <td>
        The total number of times the goal event was triggered.
      </td>
    </tr>

    <tr>
      <td>
        Unique profile who triggered &lt;Goal event&gt;
      </td>

      <td>
        Number of Users who triggered &lt;Goal event&gt;
      </td>

      <td>
        Total number of users who triggered the goal event.
      </td>
    </tr>

    <tr>
      <td>
        Percent of Users who triggered &lt;Goal Event&gt;
      </td>

      <td>
        Percent of users who triggered the &lt;Goal Event&gt; =\
        100 x \[(Users Who Triggered X Event) / (Total  Users)]
      </td>

      <td>
        The percentage of users in your app that triggered the goal event.
      </td>
    </tr>

    <tr>
      <td>
        Average occurrences of &lt;Goal event&gt; per Unique User
      </td>

      <td>
        (Total occurrences of &lt;GoalEvent&gt; / Total Unique Users)
      </td>

      <td>
        The average number of times a user triggers this event.
      </td>
    </tr>

    <tr>
      <td>
        Average occurrences of &lt;Goal event&gt; per Session
      </td>

      <td>
        (Total occurrences of &lt;GoalEvent&gt; / Total Sessions)
      </td>

      <td>
        The average number of times the goal event is triggered in a session.
      </td>
    </tr>

    <tr>
      <td>
        Total sum of &lt;Event Property&gt; values
      </td>

      <td>
        (Total sum of &lt;Event Property&gt; values)
      </td>

      <td>
        Total sum of all aggregate event property values associated with the goal event.
      </td>
    </tr>

    <tr>
      <td>
        Average of &lt;Event Property&gt; values
      </td>

      <td>
        (Total sum of &lt;Event Property&gt; values / Total Event occurrences)
      </td>

      <td>
        The average value of each occurrence of this event.
      </td>
    </tr>

    <tr>
      <td>
        Average of &lt;Event Property&gt; values per unique user 
      </td>

      <td>
        (Total sum of &lt;Event Property&gt; values / Unique Users)
      </td>

      <td>
        The average of &lt;Event Property&gt; values of the goal event per user.
      </td>
    </tr>
  </tbody>
</Table>
After you select the event metric of your choice from the dropdown, you can view its data in graphical and tabular format. Let us consider a sample test where an e-commerce business wants to analyze the sales. In this case, you add an event **Charged** as a Goal with aggregate property `value`. The following image shows the set of available metrics for the  **Charged** event:

<Image alt="Graphical view for the Coins Earned Event" align="center" border={true} src="https://files.readme.io/2174557-Goal_event_metrics.png" />  
Graphical Data View of Charged Event











<Image alt="Tabular view for the Coins Earned Event" align="center" border={true} src="https://files.readme.io/6a71eb5-tabular_view.png" />  
Tabular data view for the Charged Event











## All Time Performance

For a limited set of metrics (*Percent of users who triggered* the &lt;Event&gt;), you can see the *All Time Performance* section. 

This feature calculates data throughout the entire duration of the A/B Test, irrespective of the time frame selected at the top of the page. Based on all the data, each variant is analyzed to identify if it is statistically significant, and an **indicator** is displayed next to the variants that helps:

* Validate the reliability of the results. 
* Assess whether any observed differences between the control and variant groups are not merely attributable to random chance.
* Provides you confidence in the decision-making process.

> 📘 Note
>
> CleverTap uses a two-tailed Welch's t-test with a default setting of 95% confidence interval to identify the statistically significant variant.

<Image alt="All Time Performance View for Limited Set of Metrics" align="center" border={true} src="https://files.readme.io/53b013d-All_Time_Performance_Section.png" />
All Time Performance Section for a Limited Set of Metrics