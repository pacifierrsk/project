# project
plot-1
hist(data$Global_active_power,	hist(data$Global_active_power,
     xlab = "Global Active Power (kilowatts)",	     xlab = "Global Active Power (kilowatts)",
     col  = "red",	     col  = "red",
     main = "Global Active Power")	     main = "Global Active Power")
# Save Plot ---------------------------------------------------------------	# Save Plot ---------------------------------------------------------------
dev.copy(png, "plot1.png",	dev.copy(png, "plot1.png",
         width  = 480,	         width  = 480,
         height = 480)	         height = 480)
dev.off()	dev.off()
rm(list = ls())
plot-2
plot(Global_active_power ~ datetime, data, type = "l",	plot(Global_active_power ~ datetime, data, type = "l",
     ylab = "Global Active Power (kilowatts)",	     ylab = "Global Active Power (kilowatts)",
     xlab = NA)	     xlab = NA)
# Save Plot ---------------------------------------------------------------	# Save Plot ---------------------------------------------------------------
dev.copy(png, "plot2.png",	dev.copy(png, "plot2.png",
         width  = 480,	         width  = 480,
         height = 480)	         height = 480)
dev.off()	dev.off()
rm(list = ls())
plot-3
plot(Sub_metering_1 ~ datetime, data, type = "l",	plot(Sub_metering_1 ~ datetime, data, type = "l",
     ylab = "Energy sub metering",	     ylab = "Energy sub metering",
     xlab = NA)	     xlab = NA)
lines(Sub_metering_2 ~ datetime, data, type = "l", col = "red")	lines(Sub_metering_2 ~ datetime, data, type = "l", col = "red")
lines(Sub_metering_3 ~ datetime, data, type = "l", col = "blue")	lines(Sub_metering_3 ~ datetime, data, type = "l", col = "blue")
legend("topright",	legend("topright",
       col = c("black",	       col = c("black",
               "red",	               "red",
               "blue"),	               "blue"),
       legend = c("Sub_metering_1",	       legend = c("Sub_metering_1",
                  "Sub_metering_2",	                  "Sub_metering_2",
                  "Sub_metering_3"),	                  "Sub_metering_3"),
       lty = 1)	       lty = 1)
dev.off()	dev.off()
rm(list = ls())
plot-4
plot(Global_active_power ~ datetime, data, type = "l",	plot(Global_active_power ~ datetime, data, type = "l",
     ylab = "Global Active Power (kilowatts)",	     ylab = "Global Active Power (kilowatts)",
     xlab = NA)	     xlab = NA)
# Plot 2: Top Right	# Plot 2: Top Right
plot(Voltage ~ datetime, data, type = "l")	plot(Voltage ~ datetime, data, type = "l")
# Plot 3: Bottom Left	# Plot 3: Bottom Left
plot(Sub_metering_1 ~ datetime, data, type = "l",	plot(Sub_metering_1 ~ datetime, data, type = "l",
     ylab = "Energy sub metering",	     ylab = "Energy sub metering",
     xlab = NA)	     xlab = NA)
lines(Sub_metering_2 ~ datetime, data, type = "l", col = "red")	lines(Sub_metering_2 ~ datetime, data, type = "l", col = "red")
lines(Sub_metering_3 ~ datetime, data, type = "l", col = "blue")	lines(Sub_metering_3 ~ datetime, data, type = "l", col = "blue")
legend("topright",	legend("topright",
       col = c("black",
