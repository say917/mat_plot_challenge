# Generate a bar plot showing the total number of rows (Mouse ID/Timepoints) for each drug regimen using Pandas.
#https://www.educative.io/answers/how-to-make-bar-graphs-using-pandas
total_rows = merge_data.groupby(['Drug Regimen'])['Mouse ID'].count()
total_rows
bar_graph = total_rows.plot.bar(x='Drug Regimen',y=total_rows, color='g', align='center', fontsize=8)
plt.xlabel('Drug Regimen')
plt.ylabel('Mice Count')
plt.title('Mouse Regimen')
# Make the x-axis labels tight so they do not get cut off
#https://stackoverflow.com/questions/60658321/how-to-stop-the-x-axis-labels-from-getting-cut-off-from-the-bottom-of-the-bar-gr
plt.tight_layout()

plt.savefig("./Figures/Regiment_Treatment.png")
total_rows
