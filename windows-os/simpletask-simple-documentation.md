# Simpletask \[Simple] Documentation

### Simpletask

Simpletask is based on the brilliant todo.txt by Gina Trapani. The goal of the application is to provide a tool to 'Getting Things Done' (GTD) without providing an overwhelming amount of options. Even though Simpletask can be customised by a fairly large amount of settings, the defaults should be sane and require no change.Simpletask can be used as a very simple todo list manager or as a more complex action manager for GTD or Manage Your Now.

### Extensions

Simpletask supports the following todo.txt extensions:

* Due date as `due:YYYY-MM-DD`
* Start/threshold date as `t:YYYY-MM-DD`
* Recurrence with `rec:\+?[0-9]+[dwmyb]` as described [here](https://updatenotes.blog/todotxt-recurring-tasks/) but with a twist.
*
  * By default Simpletask will use the date of completion for recurring as described in the link. However if the rec includes a plus (e.g. `rec:+2w`), the date is determined from the original due or threshold date.
  *
    * `rec:1b` will recur after 1 weekday (mnemonic business-day).
  * The format is described by a regular expression, so in words the syntax is `rec:` followed by an optional “+” then “1 or more” numbers and then followed by one of “day (d)”, “week (w)”, “month (m)” or “year (y)”. For example `rec:12d` sets up a 12 day recurring task.
* Hidden tasks with the specified tag `h:1`, this allows dummy tasks with predefined lists and tags so that lists and tags will be available even if the last task with the tag/list is removed from todo.txt. These tasks will not be shown by default. You can temporarily display them from the Settings.

### Commands

**The different qualifiers available are:**

| Qualifyer                                                               | "Standard"  | Description                                                            |
| ----------------------------------------------------------------------- | ----------- | ---------------------------------------------------------------------- |
| due:YYYY-MM-DD                                                          | Y           | Sets a due date for a task                                             |
| due:+Xd                                                                 | N           | Creates a due date X days in the future                                |
| due:+Xw                                                                 | N           | Creates a due date X weeks in the future                               |
| due:+Xm                                                                 | N           | Creates a due date X months in the future                              |
| due:+Xb                                                                 | N           | Creates a due date X business days in the future                       |
| due:+Xy                                                                 | N           | Creates a due date X years in the future                               |
| due:+Xp                                                                 | N           | Creates a due date a random number of days between 1-X in the future   |
| t:YYYY-MM-DD                                                            | Y           | Threshold. Hides a task until the date set                             |
| t:+Xd                                                                   | N           | Set a threshold X days in the future                                   |
| t:+Xw                                                                   | N           | Set a threshold X weeks in the future                                  |
| t:+Xm                                                                   | N           | Set a threshold X months in the future                                 |
| t:+Xb                                                                   | N           | Set a threshold X business days in the future                          |
| t:+Xy                                                                   | N           | Set a threshold X years in the future                                  |
| t:+Xp                                                                   | N           | Creates a threshold a random number of days between 1-X in the future  |
| t:+project                                                              | N           | Threshold. Hide this line until all lines with +project are done       |
| t:@context                                                              | N           | Threshold. Hide this line until all lines with @context are done       |
| rec:Xd                                                                  | N           | Recurrence. To use together with due:YYYY-MM-dd and/or t:YYYY-MM-dd.   |
| When you close this task, create a copy with due and or threshold set X | <p><br></p> | <p><br></p>                                                            |
| days in the future from today (depending on settings). If there is no   | <p><br></p> | <p><br></p>                                                            |
| due or t, one will be added (depending on settings)                     | <p><br></p> | <p><br></p>                                                            |
| rec:Xw                                                                  | N           | Recurrence. Same as rec:Xd but for weeks                               |
| rec:Xm                                                                  | N           | Recurrence. Same as rec:Xd but for months                              |
| rec:Xy                                                                  | N           | Recurrence. Same as rec:Xd but for years                               |
| rec:Xb                                                                  | N           | Recurrence. Same as rec:Xd but for business days                       |
| rec:+Xd                                                                 | N           | Recurrence. To use together with due:YYYY-MM-dd and/or t:YYYY-MM-dd.   |
| When you close this task, create a copy with due and or threshold set X | <p><br></p> | <p><br></p>                                                            |
| days in the future from the date in t: and due: (depending on settings) | <p><br></p> | <p><br></p>                                                            |
| rec:+Xw                                                                 | N           | Recurrence. Same as rec:+Xd but for weeks                              |
| rec:+Xm                                                                 | N           | Recurrence. Same as rec:+Xd but for months                             |
| rec:+Xy                                                                 | N           | Recurrence. Same as rec:+Xd but for years                              |
| rec:+Xb                                                                 | N           | Recurrence. Same as rec:+Xd but for business days                      |
| rec:+Xp                                                                 | N           | Creates a recurrence a random number of days between 1-X in the future |
