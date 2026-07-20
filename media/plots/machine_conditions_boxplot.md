# Convert Machine to factor with custom labels to include Temperature and Pressure
X002..3.$Machine_Label <- factor(X002..3.$Machine,
                                 levels = c(1, 2, 3),
                                 labels = c("Machine 1 (303 K, 100 kPa)",
                                            "Machine 2 (338 K, 200 kPa)",
                                            "Machine 3 (373 K, 300 kPa)"))

# Create boxplot using ggplot2 and plotly
p <- ggplot(X002..3., aes(x = Machine_Label, y = PartResistance, fill = Machine_Label)) +
  geom_boxplot() +
  labs(
    title = 'Part Resistance by Machine Operating Conditions',
    x = 'Machine Operating Conditions',
    y = expression('Part Resistance ' * Omega)
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18),
    axis.title.x = element_text(size = 18),
    axis.title.y = element_text(size = 18),
    axis.text.x = element_text(size = 14, angle = 45, hjust = 1),
    axis.text.y = element_text(size = 14),
    legend.position = 'none',
    panel.background = element_rect(fill = 'white', colour = 'white'),
    plot.background = element_rect(fill = 'white', colour = 'white')
  ) +
  scale_fill_manual(values = c('#0072B2', '#D55E00', '#009E73'))

p_plotly <- ggplotly(p)

# Save plotly widget as HTML
htmlwidgets::saveWidget(p_plotly, 'media/plots/machine_conditions_boxplot.html', selfcontained = TRUE)
