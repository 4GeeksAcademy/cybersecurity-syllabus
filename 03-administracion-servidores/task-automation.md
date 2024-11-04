---
title: "What is Cron and how to use it to schedule and automate Tasks"
subtitle: "Efficient Automation: Understand what cron is and how to configure it in Linux to optimize repetitive tasks and ensure server stability. Learn step by step."
tags: ["servers", "cron-jobs", "task processing", "computational task"]
authors: ["blindma1den", "lorenagubaira"]

---

Cron is a very useful tool in Linux operating systems that allows you to schedule tasks to run automatically at specific times. With cron, you can automate repetitive tasks such as making backups, updating databases, sending email reports, and much more.

Tasks in cron are configured through files called "crontabs." Each user can have their own crontab, which contains the scheduled tasks for that particular user. To edit a user's crontab, you can use the command `crontab -e`.

The format of a crontab consists of five fields separated by spaces: minutes, hours, day of the month, month, and day of the week. You can use numbers or asterisks (*) to indicate all possible values in a field.

For example, if you want a Python script to run every day at 8:00 a.m., you can set the crontab as follows:

```txt
0 8 * * * python <path to file.py>
```

In addition to numeric values, you can also use special expressions in the time fields. For example, "@daily" translates to "0 0 * * *," which means the task will run every day at midnight. Other useful expressions include "@hourly," "@weekly," and "@monthly."

```txt
@daily /path/to/script.sh
```

> 🛟 @daily does not allow specifying a specific time, as it runs automatically at midnight (00:00) each day. To run a script every day at a specific time, such as 1 PM, you must use the standard cron format as shown above.

These expressions translate as follows:

@reboot: Runs once, just after the computer starts.

| Expression | Description |
|------------|-------------|
| @yearly    | Runs once a year: 0 0 1 1 * |
| @monthly   | Runs once a month on the first day: 0 0 1 * * |
| @weekly    | Runs weekly, at the first minute of the first hour of the week: 0 0 * * 0 |
| @daily     | Runs daily at midnight: 0 0 * * * |
| @midnight  | Has the same effect as the previous one. |
| @hourly    | Runs every hour at the first minute: 0 * * * * |

We can also use some modifiers, which are special characters that give us more power to create new rules. This increases the possibilities for creating more complex and precise processes. These are:

| Modifier | Description |
|-------------|-------------|
| `*`         | Means the same as assigning all values. |
| `,`         | Gives us a list of values. |
| `-`         | Sets a range of values. |
| `/`         | Means "every." |
| `range / excep` | Creates exceptions in the rule. |

> ⚠️ It is important to note that scheduled tasks in cron run in the context of the user who scheduled them. Therefore, ensure that the user has the appropriate permissions to perform the scheduled tasks.

Some examples of tasks with modifiers:

| Task                                | Description                                                                                 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 0 8,16 * * *                        | Runs a task every day at 8 AM and 4 PM.                                                     |
| 0 0 1-7 * *                         | Runs a task every day at midnight during the first week of each month.                      |
| */15 * * * *                        | Runs a task every 15 minutes.                                                               |
| 0 5 * * 1-5                         | Runs a task at 5 AM from Monday to Friday.                                                  |

Additionally, it is advisable to redirect the output of scheduled tasks to log files to verify their execution and detect possible errors. You can do this by adding `>> path_to_file` at the end of the command line in the crontab.

To list the scheduled tasks in a crontab, you can use the command `crontab -l`. If you want to remove all scheduled tasks from a crontab, you can use the command `crontab -r`.

This helps us schedule tasks that can become repetitive, allowing system administrators to focus on other things. It provides a very efficient way to schedule the execution of various scripts, commands, and programs. Due to the high degree of customization, we can schedule practically anything necessary and beneficial for the organization and its tasks.

These systems offer several advantages at the enterprise level. The first is the ability to schedule tedious tasks so that manual intervention is not needed, saving time and reducing the risk of human errors. Common methods include backups, software updates, generating reports, or running maintenance processes. In addition to this, we also have scheduling flexibility. All the benefits previously discussed about cron and crontab are available at the enterprise level, providing abundant options for creating such automations.

## Creating and Editing Crontab Files

Creating and editing crontab files is a common task in Unix and Linux systems to schedule tasks to run automatically at specific times. A crontab file contains instructions for the cron daemon on what tasks to run and when.

To create or edit a crontab file, you can use the command `crontab -e`. This will open the crontab file in the system's default text editor, such as vi or nano. If it is your first time using `crontab -e`, you will be prompted to choose an editor.

The crontab file has a specific format consisting of five fields separated by spaces: minutes, hours, day of the month, month, and day of the week. Each field accepts numeric values or special characters. For example, if you want a task to run every day at 8:00 a.m., you can add the following line to the crontab file:

```
0 8 * * * command
```

In this line, "0" represents the minutes (in this case, 0), "8" represents the hours (8:00 a.m.), and the asterisks (*) indicate that any value is valid for the remaining fields.

In addition to numeric values, you can also use special expressions in the time fields. For example, "@daily" translates to "0 0 * * *," which means the task will run every day at midnight. Other useful expressions include "@hourly," "@weekly," and "@monthly."

After specifying the time, you must add the command you want to run. It can be any valid command on the system, such as a script, program, or command sequence. Ensure you provide the full path to the command if necessary.

It is important to note that each line in the crontab file represents a scheduled task. You can add multiple lines to schedule multiple tasks. Each line must end with a newline.

Once you have finished editing the crontab file, save the changes and close the editor. The cron daemon will read and execute the scheduled tasks as specified in the crontab file.

To list the scheduled tasks in a crontab file, you can use the command `crontab -l`. If you want to remove all scheduled tasks from a crontab file, you can use the command `crontab -r`.

Remember that scheduled tasks in a crontab file run in the context of the user who scheduled them. Ensure the user has the appropriate permissions to perform the scheduled tasks.

## Monitoring and Verifying Scheduled Tasks

Monitoring and verifying scheduled tasks are important aspects of system administration to ensure that tasks are running correctly and at the desired times. This allows you to detect and solve potential problems and ensure the system's efficiency and reliability.

A common way to monitor scheduled tasks is to review the logs generated by the system. Cron logs, for example, provide detailed information about the execution of scheduled tasks. You can find these logs in the "/var/log" directory with names like "cron.log" or "syslog."

To verify if a scheduled task has run correctly, you can review the corresponding log and look for success or error messages. If you find an error, it is important to investigate and solve the underlying cause. You can use tools like "grep" or "awk" to search for specific events in the logs.

In addition to logs, you can also receive email notifications about the status of scheduled tasks. You can configure the command or script that runs as a scheduled task to send a notification email upon completion. This allows you to receive real-time updates about the status of tasks and take quick action if necessary.

Another option is to use more advanced system monitoring tools such as Nagios, Zabbix, or Prometheus. These tools allow you to monitor and verify scheduled tasks and other aspects of the system, such as performance, availability, and resource utilization. You can set up alerts and receive notifications when problems with scheduled tasks are detected.

> ⚠️ It is important to establish a regular monitoring routine to verify the status of scheduled tasks. You can schedule daily, weekly, or monthly reviews depending on the importance and frequency of the tasks. This will help you identify problems promptly and ensure that tasks are running as planned.
