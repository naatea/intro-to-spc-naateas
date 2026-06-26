# Load necessary libraries
library(ggplot2)
library(plotly)

# Filter the data for Machine == 1 only
df_machine1 <- subset(X024, Machine == 1)

# Treat Pressure and Temperature as factors for plotting
df_machine1$Pressure <- as.factor(df_machine1$Pressure)
df_machine1$Temperature <- as.factor(df_machine1$Temperature)

# Plot for Pressure
p_pressure <- ggplot(df_machine1, aes(x = Pressure, y = PartResistance, fill = Pressure)) +
  geom_boxplot() +
  labs(
    title = "Part Resistance by Pressure",
    x = "Pressure",
    y = "Part Resistance"
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18, face = "bold"),
    axis.title = element_text(size = 18),
    axis.text = element_text(size = 14),
    legend.position = "none"
  )

# Plot for Temperature
p_temperature <- ggplot(df_machine1, aes(x = Temperature, y = PartResistance, fill = Temperature)) +
  geom_boxplot() +
  labs(
    title = "Part Resistance by Temperature",
    x = "Temperature",
    y = "Part Resistance"
  ) +
  theme_minimal() +
  theme(
    plot.title = element_text(size = 18, face = "bold"),
    axis.title = element_text(size = 18),
    axis.text = element_text(size = 14),
    legend.position = "none"
  )

# Combine plots using plotly subplots for a single interactive widget
combined_plot <- subplot(ggplotly(p_pressure), ggplotly(p_temperature), nrows = 1, shareY = TRUE) %>% 
  layout(title = list(text = 'Part Resistance Distribution by Pressure and Temperature (Machine 1)', font = list(size = 20)),
         annotations = list(
           list(x = 0.22, y = 1.0, text = "By Pressure", showarrow = F, xref='paper', yref='paper', font = list(size = 16)),
           list(x = 0.78, y = 1.0, text = "By Temperature", showarrow = F, xref='paper', yref='paper', font = list(size = 16))
         ))

# Save the combined interactive plot as an HTML widget
htmlwidgets::saveWidget(combined_plot, "media/plots/resistance_boxplots.html", selfcontained = TRUE)
