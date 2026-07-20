# Convert Timestamp to datetime and Machine to factor
X002..3.$Timestamp <- as.POSIXct(X002..3.$Timestamp)
X002..3.$Machine <- as.factor(X002..3.$Machine)

# Perform ANOVA
anova_result <- aov(PartResistance ~ Machine, data = X002..3.)

# Extract p-value
p_value <- summary(anova_result)[[1]]$'Pr(>F)'[1]

# Round p-value to 4 decimal places, use 0 if too small
if (p_value < 0.0001) {
    p_value_formatted <- '0'
} else {
    p_value_formatted <- format(round(p_value, 4), nsmall = 4)
}

# Create boxplot using ggplot2 and plotly
p <- ggplot(X002..3., aes(x = Machine, y = PartResistance, fill = Machine)) +
  geom_boxplot() +
  labs(
    title = 'Part Resistance by Machine (ANOVA)',
    x = 'Machine (Temperature, Pressure)',
    y = expression('Part Resistance ' * Omega)
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18),
    axis.title.x = element_text(size = 18),
    axis.title.y = element_text(size = 18),
    axis.text.x = element_text(size = 14),
    axis.text.y = element_text(size = 14),
    legend.position = 'none'
  ) +
  scale_fill_manual(values = c('#0072B2', '#D55E00', '#009E73'))

p_plotly <- ggplotly(p)

# Save plotly widget as HTML
htmlwidgets::saveWidget(p_plotly, 'media/plots/resistance_anova_boxplot.html', selfcontained = TRUE)

# Print p-value (for display purposes in Colab output)
cat(paste0('P-value for ANOVA: ', p_value_formatted, '
'))
