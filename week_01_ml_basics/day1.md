📊 Matplotlib – Core Plotting Functions
Matplotlib is a low-level plotting library. Most plots use plt from matplotlib.pyplot.

📌 1. Figure Setup

plt.figure(figsize=(8, 6))
plt.subplot(1, 2, 1)  # (rows, columns, index)
📌 2. Line and Scatter Plots

plt.plot(x, y)             # Line plot
plt.scatter(x, y)          # Scatter plot
plt.bar(x, height)         # Vertical bar chart
plt.barh(x, height)        # Horizontal bar chart
📌 3. Histograms & Boxplots

plt.hist(data, bins=10)    # Histogram
plt.boxplot(data)          # Boxplot
📌 4. Labels & Titles

plt.title("Title")
plt.xlabel("X-axis label")
plt.ylabel("Y-axis label")
📌 5. Legends & Grid

plt.legend(["label1", "label2"])
plt.grid(True)
📌 6. Customization

plt.xticks(rotation=45)
plt.yticks(fontsize=12)
plt.style.use('ggplot')   # or 'seaborn', 'dark_background', etc.
📌 7. Show or Save

plt.show()
plt.savefig("plot.png")

🖼️ Seaborn – High-Level Statistical Visualizations
Seaborn is built on top of Matplotlib and pandas. It handles DataFrames directly and looks better by default.

📌 1. Distribution Plots

sns.histplot(data=df, x="age", kde=True)
sns.kdeplot(data=df["age"])
sns.boxplot(x="class", y="age", data=df)
sns.violinplot(x="class", y="fare", data=df)
sns.ecdfplot(data=df["fare"])
📌 2. Categorical Plots

sns.countplot(x="class", data=df)
sns.barplot(x="class", y="fare", data=df)
sns.stripplot(x="class", y="age", data=df)
sns.swarmplot(x="class", y="age", data=df)
📌 3. Matrix & Heatmap Plots

sns.heatmap(df.corr(), annot=True, cmap="coolwarm")
sns.clustermap(df.corr(), cmap="viridis")
📌 4. Relational Plots

sns.scatterplot(x="age", y="fare", data=df)
sns.lineplot(x="age", y="fare", data=df)
sns.relplot(x="age", y="fare", hue="class", data=df)
📌 5. Multi-Feature / High-Level

sns.pairplot(df, hue="survived")
sns.jointplot(x="age", y="fare", kind="scatter", data=df)
📌 6. Themes & Style

sns.set_style("whitegrid")  # Options: darkgrid, white, ticks, etc.
sns.set_palette("pastel")   # or "muted", "deep", etc.