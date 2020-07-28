# Counter_Attacks

ggplot(data, aes(x = Year, y = Conversion, group = 1)) +
geom_point(aes(size = 6), show.legend = FALSE) +
geom_line() +
labs(y = ‘Conversion (%)’, x = ‘Year’, title = ‘Figure 2’, subtitle = ‘Conversion Rate of Shots from Counter-Attacks’) +
ylim(0, 50) +
theme_bw()

ggplot(data, aes(x = Year, y = Conversion, group = 1)) +
geom_point(aes(colour = Conversion > 25, size = 6), show.legend = FALSE) +
geom_line() +
labs(y = ‘Conversion (%)’, x = ‘Year’, title = ‘Figure 3’, subtitle = ‘Conversion Rate of Shots from Counter-Attacks’) +
scale_colour_manual(values = setNames(c(‘red’, ‘black’), c(T, F))) +
ylim(0, 50) +
theme_bw()
