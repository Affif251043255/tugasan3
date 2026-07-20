library(tidyverse)
library(plotly)
library(htmlwidgets)

machine1_data <- X002..3. %>% filter(Machine == 1, Temperature == 303, Pressure == 100) %>% mutate(Timestamp = as.POSIXct(Timestamp, format = "%Y-%m-%d %H:%M:%S"))
p_machine1 <- ggplot(machine1_data, aes(x = Timestamp, y = PartResistance)) +
  geom_line(color = "#0072B2") +
  geom_point(color = "#0072B2", size = 1.5) +
  labs(title = "Machine 1 Part Resistance Over Time", x = "Timestamp", y = "Part Resistance (Ohms)") +
  theme_minimal() +
  theme(axis.title.x = element_text(size = 18), axis.title.y = element_text(size = 18), axis.text = element_text(size = 14), plot.background = element_rect(fill = "white", colour = "white"))
plotly_machine1 <- ggplotly(p_machine1)
saveWidget(plotly_machine1, file = "media/plots/machine1_part_resistance.html", selfcontained = TRUE)
