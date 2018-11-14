-   Designs for all of the screens you plan to have.

![](media/image2.png){width="2.9375in" height="5.557292213473316in"}

![](media/image1.png){width="6.5in" height="6.0in"}

> ![](media/image3.png){width="2.0833333333333335in"
> height="4.510416666666667in"}

-   A listing of all third party libraries you plan to use.

> For searching, auto completing, filtering, and sorting:
>
> [[https://www.smashingmagazine.com/2012/04/ui-patterns-for-mobile-apps-search-sort-filter/]{.underline}](https://www.smashingmagazine.com/2012/04/ui-patterns-for-mobile-apps-search-sort-filter/)
>
> Background Fetch and Send banner notification:
>
> [[https://www.objc.io/issues/5-ios7/multitasking/]{.underline}](https://www.objc.io/issues/5-ios7/multitasking/)
>
> PermissionScope for requesting permissions from users.
>
> Hedwig for sending users emails for reminders.
>
> MGSwipeTableCell for adding buttons to table cells.
>
> Timepiece for intuitive date handling in Swift.
>
> FSCalendar for a fully customizable iOS calendar library.
>
> https://medium.com/app-coder-io/33-ios-open-source-libraries-that-will-dominate-2017-4762cf3ce449

-   Server support for your app. If you plan to roll your own server
    > support, a full listing of the APIs you plan to build.

> No server support needed. Only Local Storage.

-   A listing of all of the models you plan to include in your app

> TODO: user entered data?

1.  Storage.swift: similar to our HW.

Class Task {

var title: String

var due\_time: Date

> var details: String
>
> init()
>
> ...

}

Class Scheduler {

var tasks: \[Task\]

sort(task1 : Task, task2 : Task) // sort tasks by date in descending
order yr,month then day

> init()
>
> ...

}

(pseudocode)

> Class Date{
>
> private:
>
> Int Year;
>
> Int month;
>
> Int Day
>
> public:
>
> Date(string year, string month, string day){
>
> self.year = stoi(year)
>
> self.day = stoi(day)
>
> self.month = stoi(month)
>
> }
>
> }

-   A listing of all ViewControllers you will implement. Please include
    > how you plan to navigate to / from each ViewController and any
    > protocols / delegates / variables you plan to use for
    > ViewController / ViewController communication.

    -   Creating new event:

        -   From main menu view controller upon "+" button being pressed

        -   Segue to new event VC which allows user to enter in the name
            > of new task, description of task and when the task is due

        -   Force user to enter month,day, year in correct format i.e.
            > prevent them from entering in too many characters

        -   Event VC passes back this event which is appended to the
            > list of events in the main VC

        -   The tasks in the main VC is then resorted based on a custom
            > sort function

        -   Implement enter and cancel

Five ViewControllers: Scheduler ViewController, Details ViewController,
**[Concentrate ViewController(????? Yanxi ???????)]{.underline}**,
Daily-Planner ViewController, Add task view Controller

Draw arrows to illustrate how to navigate....

> By clicking daily planner button in the first view, users can go to
> the 4th view, daily planner, where tasks scheduled for that day will
> be shown only on the fourth view. The daily planner works as notes.
> User can click the cell on the 4th view and go to the detailed view to
> read or edit the details. I plan to filter the data in the first row
> by start time, and pass the variables with start time == today's date
> to the fourth view.
>
> By clicking add (the plus button) in the first view user can add tasks
> to the scheduler app will go to the add task VC from which it will
> allow user to enter data and send it back to parent VC and resort
> based on relative closeness of due dates

-   A list of approximately week long tasks and a timeline of when each
    > of them will be done

+-----------------------------------+-----------------------------------+
| Sunil                             | Nov 13 - Nov 20: finish add task  |
|                                   | view contoller and make sure      |
|                                   | segue is workign correctly        |
|                                   | (passing back data), also custom  |
|                                   | date sort fxn for tasks           |
|                                   |                                   |
|                                   | Nov 21 - Nov 28: work with        |
|                                   | teammates to unify all views/view |
|                                   | controllers/models; work on       |
|                                   | assigned challenges.              |
|                                   |                                   |
|                                   | Nov 29 - Dec 5: continue with     |
|                                   | assigned challenges and testing.  |
+===================================+===================================+
| Jiajun                            | Nov 13 - Nov 20: finish the main  |
|                                   | scheduler view as soon as         |
|                                   | possible so that my teammate      |
|                                   | could have the scheme to work out |
|                                   |                                   |
|                                   | Nov 21 - Nov 28: work with        |
|                                   | teammates to unify all views/view |
|                                   | controllers/models; work on       |
|                                   | assigned challenges.              |
|                                   |                                   |
|                                   | Nov 29 - Dec 5: continue with     |
|                                   | assigned challenges and testing.  |
+-----------------------------------+-----------------------------------+
|                                   |                                   |
+-----------------------------------+-----------------------------------+
| Hanxing                           | Nov 13 - Nov 20: finish the daily |
|                                   | planner view and its detailed     |
|                                   | view.                             |
|                                   |                                   |
|                                   | Nov 21 - Nov 28: work with        |
|                                   | teammates to unify all views/view |
|                                   | controllers/models; work on       |
|                                   | assigned challenges.              |
|                                   |                                   |
|                                   | Nov 29 - Dec 5: continue with     |
|                                   | assigned challenges and testing.  |
+-----------------------------------+-----------------------------------+

-   A trello board that includes all of the tasks and their state (up
    > next, in progress, blocked, done). These tasks need to include an
    > owner from the start, but the owner can change during the quarter
    > as needed

> [[https://trello.com/b/SuBG7jG6/scheduler-app]{.underline}](https://trello.com/b/SuBG7jG6/scheduler-app)

-   A github classroom project that includes all of this documentation.
    > The Readme in your project needs to include a link to your Trello
    > board and pictures of each of the team members with their name and
    > github handle

-   A testing plan. A good app should get feedback from potential users
    > early and often. List here what you plan to get other people to
    > test out.

> We plan to start to test the app once it is unified. We will ask
> friends in the class and outside the classes for testing. Some
> interesting questions we would like to ask them include: 1. Are the
> user interfaces appealing? Rate from not appealing, it is ok, it is
> appealing, and it's extremely appealing? 2. Is the app help with
> organizing one's daily tasks in any way? Rate from not helping at all,
> helps a little, helps a lot. 3. Any suggestions on the app?
