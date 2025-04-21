Direct Explanation of R Code
read.csv("appointments.csv")
→ Loads the dataset from a CSV file.

as.POSIXct(data$ScheduledDay)
→ Converts the scheduled date to proper datetime format.

as.Date(data$AppointmentDay)
→ Converts the appointment date to date format.

data[data$Age >= 0 & data$Age < 120, ]
→ Removes rows with unrealistic ages (less than 0 or over 120).

ifelse(data$No_show == "No", 0, 1)
→ Converts "No" (patient showed up) to 0, and "Yes" (no-show) to 1.

na.omit(data)
→ Deletes rows with missing values.

data$WaitingDays <- as.integer(...)
→ Adds a new column that calculates how many days a patient waited for the appointment.

write.csv(data, "appointments_clean.csv")
→ Saves the cleaned dataset to a new CSV file.
