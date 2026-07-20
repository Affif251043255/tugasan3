# Create a scatter plot of PartLength vs PartResistance
p <- ggplot(X002..3., aes(x = PartLength, y = PartResistance, color = factor(Machine))) +
  geom_point(alpha = 0.6) +
  labs(
    title = 'PartLength vs PartResistance by Machine',
    x = expression('Part Length (mm)'),
    y = expression('Part Resistance (' * Omega * ')'),
    color = 'Machine'
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18),
    axis.title.x = element_text(size = 18),
    axis.title.y = element_text(size = 18),
    axis.text.x = element_text(size = 14),
    axis.text.y = element_text(size = 14),
    legend.title = element_text(size = 14),
    legend.text = element_text(size = 12),
    panel.background = element_rect(fill = 'white', colour = 'white'),
    plot.background = element_rect(fill = 'white', colour = 'white')
  ) +
  scale_color_manual(values = c('#0072B2', '#D55E00', '#009E73'))

p_plotly <- ggplotly(p)

# Save plotly widget as HTML
htmlwidgets::saveWidget(p_plotly, 'media/plots/length_vs_resistance.html', selfcontained = TRUE)
